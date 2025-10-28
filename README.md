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


Am = 6.8
fm = 532
fs = 53200
t = np.arange(0, 2/fm, 1/fs)

m = Am * np.cos(2 * np.pi * fm * t)
plt.subplot(3, 1, 1)
plt.plot(t, m)

Ac = 13.6
fc = 5320
c = Ac * np.cos(2 * np.pi * fc * t)
plt.subplot(3, 1, 2)
plt.plot(t, c)

B = 6.9
s = Ac * np.cos(2 * np.pi * fc * t + B * np.sin(2 * np.pi * fm * t))
plt.subplot(3, 1, 3)
plt.plot(t, s)

plt.tight_layout()
```
Output Waveform

<img width="712" height="545" alt="image" src="https://github.com/user-attachments/assets/c37a602f-1952-4c43-8ba2-559370717f57" />


Tabular Column

![WhatsApp Image 2025-10-28 at 10 36 44_97d8ca82](https://github.com/user-attachments/assets/8b19cd38-4229-443b-9ccc-25b60e09be1f)



Calculation

![WhatsApp Image 2025-10-28 at 10 36 49_4cc62f3a](https://github.com/user-attachments/assets/1183c324-ce73-4a06-b088-a552890c1159)



Result


The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
