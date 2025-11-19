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


Am = 5.4
fm = 457
fs = 45700
t = np.arange(0, 2/fm, 1/fs)

m = Am * np.cos(2 * np.pi * fm * t)
plt.subplot(3, 1, 1)
plt.plot(t, m)

Ac = 10.7
fc = 4570
c = Ac * np.cos(2 * np.pi * fc * t)
plt.subplot(3, 1, 2)
plt.plot(t, c)

B = 4.2
s = Ac * np.cos(2 * np.pi * fc * t + B * np.sin(2 * np.pi * fm * t))
plt.subplot(3, 1, 3)
plt.plot(t, s)

plt.tight_layout()
```
Output Waveform

<img width="787" height="583" alt="image" src="https://github.com/user-attachments/assets/c9e9b1a1-3c31-407d-a23b-0e5bb09cbd5d" />


Tabular Column

<img width="665" height="953" alt="image" src="https://github.com/user-attachments/assets/cc4f3993-dbc4-44e9-b61b-be4abb8922fd" />



Calculation

<img width="628" height="952" alt="image" src="https://github.com/user-attachments/assets/46b0f0ec-53b0-44b0-97b4-dc57f07c1674" />



Result


The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
