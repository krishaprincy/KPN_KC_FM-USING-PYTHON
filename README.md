# FM-using-Python

Aim


To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries. 

Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
Theory

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier wave is varied according to the instantaneous amplitude of the message signal. The general form of an FM signal is:



Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

Program
```
import numpy as np
import matplotlib.pyplot as plt

Am=2.8
Ac=5.6
fm=174
fc=1740
fs=17400
t=np.arange(0,3/fm,1/fs)
m=Am*np.cos(2*np.pi*fm*t)
c=Ac*np.cos(2*np.pi*fc*t)
b=4.7
eFM =Ac*np.cos(2 * np.pi * fc * t + b * np.sin(2 * np.pi * fm * t))
plt.subplot(3,1,1)
plt.plot(t,m)
plt.grid()
plt.subplot(3,1,2)
plt.plot(t,c)
plt.grid()
plt.subplot(3,1,3)
plt.plot(t,eFM)
plt.grid()

plt.tight_layout()
plt.show()

```
Output Waveform

<img width="1349" height="957" alt="image" src="https://github.com/user-attachments/assets/9c96f7b7-f967-48e9-b5c6-f946c3464d1f" />


Tabular Column

![WhatsApp Image 2025-12-04 at 15 38 34_d6af8f5a](https://github.com/user-attachments/assets/4f97a091-1f39-4df4-a5c6-b216cb17e9d4)


Calculation




Result


The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
