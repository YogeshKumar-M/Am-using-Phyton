# Am-using-Phyton

# AIM:

To generate and detect the amplitude modulation and demodulation using python code and to calculate modulation index of AM.

# EQUIPMENTS REQUIRED

• Computer with i3 Processor

• colab

# THEORY:

Modulation can be defined as the process by which the characteristics of carrier wave are varied in accordance with the modulating wave (signal). Modulation is performed in a transmitter by a circuit called a modulator. Need for modulation is as follows: • Avoid mixing of signals • Reduction in antenna height • long distance communication • Multiplexing • Improve the quality of reception • Ease of radiation. Amplitude Modulation is the process of changing the amplitude of a relatively high frequency carrier signal in proportion with the instantaneous value of the modulating signal. The output waveform contains all the frequencies that make up the AM signal and is used to transport the information through the system. Therefore the shape of the modulated wave is called the AM envelope. With no modulating signal the output waveform is simply the carrier signal. Coefficient of modulation is a term used to describe the amount of amplitude change present in an AM waveform. There are three degrees of modulation available based on value of modulation index.

Under modulation : m<1, Em < Ec
Critical modulation: m-1, Em = Ec
Over modulation: m>1, Em > Ec

# Algorithm:

Define Parameters First, define the parameters for your signals: • Carrier frequency (fc) • Modulating signal frequency (fm) • Sampling frequency (Fs) • Duration of the signal (T)

Create a time vector based on the sampling frequency and duration.

Create Modulating Signal Define the modulating signal (message signal).

Create Carrier Signal Define the carrier signal.

Perform Amplitude Modulation Multiply the carrier signal by the modulating signal plus 1 (to ensure the modulation depth).

Plot the Signals Visualize the modulating, carrier, and modulated signals.

Demodulate the AM Signal To demodulate, you can use envelope detection. One way is to rectify the signal and then apply a low-pass filter.

Plot the Demodulated Signal Visualize the demodulated signal.

Compare Signals Compare the original modulating signal with the demodulated signal. PROCEDURE • Refer Algorithms and write code for the experiment. • Open colab in System • Type your code in New Editor • Save the file • Execute the code • If any Error, correct it in code and execute again • Verify the generated waveform using Tabulation and Model Waveform


# Program:
```asm
import numpy as np
import matplotlib.pyplot as plt
Am = 5.1
Ac = 10.2
fm = 447
fc = 4470
fs = 44700
t = np.arange(0, 2/fm, 1/fs)
m = Am * np.cos(2 * np.pi * fm * t)
plt.subplot(3, 1, 1)
plt.plot(t, m)
c = Ac * np.cos(2 * np.pi * fc * t)
plt.subplot(3, 1, 2)
plt.plot(t, c)
s = (Ac + m) * np.cos(2 * np.pi * fc * t)
plt.subplot(3, 1, 3)
plt.plot(t, s)


```
# model graph
<img width="919" height="1290" alt="474555463-55326c5b-7dd5-4873-aaf6-d219bb7c4420" src="https://github.com/user-attachments/assets/6f90cf04-bfad-494d-8ad9-b30b28b439a9" />


# Output
<img width="817" height="585" alt="image" src="https://github.com/user-attachments/assets/2068f280-58e8-4372-89c5-3cde9d0551cb" />



# calculation

ma (Theory) = am/ac =0.5
ma(Practical) = (Emax-Emin)/(Emax+Emin) =0.5

# Result
 Thus the amplitude modulation and demodulation is experimentally done and the output is verified.
