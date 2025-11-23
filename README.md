# Digital-Signal-Processing--FIR-BAND-STOP-FILTER-DESIGN
## AIM:
To generate design of Band Stop FIR digital filter using Window.
## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the Band Stop filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
```
clc; % clear screen
clear all; % clear screen
close all; % close all figure windows
Wc1=input('enter the value of Wc1='); 
Wc2=input('enter the value of Wc2='); 
N=input('enter the value of N=');
alpha=(N-1)/2; 
eps=0.001;
%Band stop
n=0:1:N-1
hd=(sin(Wc1*(n-alpha+eps))+sin(pi*(n-alpha+eps))-sin(Wc2*(n-alpha+eps)))./(pi*(n-alpha+eps))
%Blackman Window Sequence 
n=0:1:N-1; 
wh=0.42-0.5*cos((2*pi*n)/(N-1))+0.08*cos((4*pi*n)/(N-1))
hn=hd.*wh 
% Plot the Band stop Filter with Blackman Window Technique
w=0:0.01:pi; 
h=freqz(hn,1,w);
plot(w/pi,abs(h),'blue');
```

## OUTPUT:
<img width="695" height="622" alt="Screenshot 2025-11-19 161225" src="https://github.com/user-attachments/assets/de7e9a80-2cf2-4063-85e2-490c715b3db6" />


## RESULT:
![5](https://github.com/user-attachments/assets/c772a58c-c010-4c03-bce0-8979ace3abca)

