# -Frequency-Modulation-and-Demodulation-using-NumPy-and-Matplotlib-

__Aim:__

To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries.

__Apparatus Required:__ 

1. Software: Python with NumPy and Matplotlib libraries
   
2. Hardware: Personal Computer

 
__Theory:__

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its 
frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier 
wave is varied according to the instantaneous amplitude of the message signal.

__Algorithm:__

1. Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and 
   frequency deviation.
   
2. Generate Time Axis: Create a time vector for the signal duration.
    
3. Generate Message Signal: Define the message signal as a cosine wave.
    
4. Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
    
5. Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
 
6. Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

__Programme:__

```
import numpy as np 
import matplotlib.pyplot as plt 
Am = 16.1
Fm = 550
B = 6.3 
Ac = 32.2 
Fc = 5500 
Fs = 3150000 
t = np.arange(0, 2/Fm, 1/Fs) 
em = Am * np.sin(2 * np.pi * Fm * t) 
plt.subplot(3, 1, 1) 
plt.plot(t, em) 
plt.grid() 
ec = Ac * np.sin(2 * np.pi * Fc * t) 
plt.subplot(3, 1, 2) 
plt.plot(t, ec) 
plt.grid() 
efm = Ac * np.cos((2*np.pi*Fc*t) + ( B*np.sin(2*np.pi*Fm*t))) 
plt.subplot(3, 1, 3) 
plt.plot(t, efm) 
plt.grid() 
plt.tight_layout() 
plt.show()
```

__Output:__

<img width="630" height="469" alt="image" src="https://github.com/user-attachments/assets/800c4e73-9b58-4bed-bff7-a02271bfe461" />


__Result:__

The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
