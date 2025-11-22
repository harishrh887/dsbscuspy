# DSBSC USING PYTHON
DSB-SC-AM MODULATOR AND DEMODULATOR

AIM:

To write a program to perform DSBSC modulation and demodulation using COLAB and study its spectral characteristics

EQUIPMENTS REQUIRED

•	Computer with i3 Processor
•	GOOGLE COLAB

Note: Keep all the switch faults in off position

Algorithm:

1.	Define Parameters:
•	Fs: Sampling frequency.
•	T: Duration of the signal.
•	Fc: Carrier frequency.
•	Fm: Frequency of the message signal.
•	Amplitude: Maximum amplitude of the message signal.
2.	Generate Signals:
•	Message Signal: A sinusoidal signal that will be modulated.
•	Carrier Signal: A high-frequency sinusoidal signal used for modulation.
3.	DSBSC Modulation:
•	Modulated Signal: Multiply the message signal by the carrier signal to produce the DSBSC signal.
4.	DSBSC Demodulation:
•	Multiplication: Multiply the modulated signal by the carrier signal to get the product of the message signal with itself (i.e., the original message signal plus high-frequency components).
•	Low-pass Filtering: Apply a Butterworth low-pass filter to remove the high- frequency components and recover the original message signal.
5.	Visualization:
Plot the message signal, carrier signal, DSBSC modulated signal, and the recovered signal after demodulation.
PROCEDURE

•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
 
•	Execute the code
•	If any Error, correct it in code and execute again
•	Verify the generated waveform using Tabulation and Model Waveform

Model Waveform

<img width="703" height="679" alt="image" src="https://github.com/user-attachments/assets/e7c7c7f8-ccf2-41ac-b1f3-325989941a6f" />

Program
import numpy as np  
import matplotlib.pyplot as plt  

am = 6.5
fm = 504  
ac = 13  
fc = 5040  
fs = 50400  
t = np.arange(0, 2/fm, 1/fs)  

m = am * np.cos(2 * np.pi * fm * t)  
plt.subplot(3, 1, 1)  
plt.plot(t, m)  


c = ac * np.cos(2 * np.pi * fc * t)  
plt.subplot(3, 1, 2)  
plt.plot(t, c)  


dsbsc_signal = m * c  
plt.subplot(3, 1, 3)  
plt.plot(t, dsbsc_signal)  
plt.tight_layout()  
plt.show()  

Output Graph

<img width="705" height="511" alt="Screenshot 2025-11-22 122455" src="https://github.com/user-attachments/assets/05215cc1-a6c5-40b7-b56f-2591db4311a6" />


Tablular Column

<img width="1280" height="980" alt="image" src="https://github.com/user-attachments/assets/d2a77726-16c4-460f-988b-9b76cffe6b9b" />



Result

Thus the DSB-SC-AM Modulation and Demodulation is generated.

