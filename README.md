EXP 4C # Design-of-FIR-Filters-using-rectangular-window
#          DESIGN OF LOW PASS FIR DIGITAL FILTER 

# AIM: 
          
  To generate design of low pass FIR digital filter using SCILAB 

# APPARATUS REQUIRED: 

  PC Installed with SCILAB 

# PROGRAM 

clc;
clear;
close;

N = 51;
wc = 0.4*%pi;

n = 0:N-1;
hn_ideal = sin(wc*(n-(N-1)/2)) ./ ( %pi*(n-(N-1)/2) );
hn_ideal((N+1)/2) = wc/%pi;

w_rect = ones(1, N);
h_rect = hn_ideal .* w_rect;

figure(3);
plot(n, h_rect);
title("FIR Filter Impulse Response (Rectangular Window)");

[H2,f2] = frmag(h_rect, 512);
figure(4);
plot(f2, abs(H2));
title("Magnitude Response (Rectangular Window)");


# OUTPUT

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/cfcbae0b-d1bf-4ba3-81e4-7f21c4268237" />


# RESULT
Thus, we generated design of low pass FIR digital filter using rectangular window in SCILAB and the output is verified. 
