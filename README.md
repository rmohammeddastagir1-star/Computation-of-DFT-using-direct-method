# EXPT 1: Computation-of-DFT-using-direct-method

## AIM
To perform and verify DFT using direct method by SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM 
```
clc; 
clear; 

xn = [1 4 1 4 1 4 1 4]; 

n1 = 0:1:length(xn)-1; 
subplot(3,1,1); 
plot2d3(n1, xn); 
xlabel('Time n'); 
ylabel('Amplitude xn'); 
title('Input Sequence'); 

j = sqrt(-1); 
N = length(xn); 
Xk = zeros(1, N); 

for k = 0:N-1 
    for n = 0:N-1 
        Xk(k+1) = Xk(k+1) + xn(n+1)*exp((-j*2*%pi*k*n)/N); 
    end 
end 

disp(Xk); 

K1 = 0:1:length(Xk)-1; 
magnitude = abs(Xk); 

subplot(3,1,2); 
plot2d3(K1, magnitude); 
xlabel('frequency(Hz)'); 
ylabel('magnitude(gain)'); 
title('magnitude spectrum'); 

angle = atan(imag(Xk), real(Xk)); 

subplot(3,1,3); 
plot2d3(K1, angle); 
xlabel('frequency(Hz)'); 
ylabel('Phase'); 
title('Phase spectrum');
```
## CALCULATIONS:
<img width="1008" height="1600" alt="image" src="https://github.com/user-attachments/assets/9fa24d62-576c-4df8-8acc-f18f8a4c0a43" />
<img width="981" height="1600" alt="image" src="https://github.com/user-attachments/assets/b35cec87-1ecb-48dc-ba72-974e929e380c" />
<img width="960" height="1600" alt="image" src="https://github.com/user-attachments/assets/6a95902f-f418-4345-b265-814399236287" />


## SAMPLE OUTPUT:
<img width="1600" height="1000" alt="image" src="https://github.com/user-attachments/assets/c264b591-8e57-47e8-ba28-cc11fff6c784" />



## RESULT:
Thus,  DFT using direct method for two given sequences were performed and its result was verified.

