# Ideal-Sampling
AIM : 
To perform Construction and Re-contruction of impluse or ideal sampling using python.

TOOLS REQUIRED : 
Softare: Google Colab 
Python libraries: NumPy, Matplotlib

PROGRAM :
~~~~
import numpy as np
import matplotlib.pyplot as plt
from scipy.signal import resample
fs = 100
t = np.arange(0, 1, 1/fs) 
f = 5
signal = np.sin(2 * np.pi * f * t)
plt.figure(figsize=(10, 4))
plt.plot(t, signal, label='Continuous Signal')
plt.title('Continuous Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()
t_sampled = np.arange(0, 1, 1/fs)
signal_sampled = np.sin(2 * np.pi * f * t_sampled)
plt.figure(figsize=(10, 4))
plt.plot(t, signal, label='Continuous Signal', alpha=0.7)
plt.stem(t_sampled, signal_sampled, linefmt='r-', markerfmt='ro', basefmt='r-', label='Sampled Signal (fs = 100 Hz)')
plt.title('Sampling of Continuous Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()
reconstructed_signal = resample(signal_sampled, len(t))
plt.figure(figsize=(10, 4))
plt.plot(t, reconstructed_signal, 'r--', label='Reconstructed Signal (fs = 100 Hz)')
plt.title('Reconstruction of Sampled Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()
~~~~
OUTPUT WAVEFORM :
![WhatsApp Image 2025-03-22 at 16 10 19_36e17a3c](https://github.com/user-attachments/assets/df1f220c-db6d-4ec7-bab0-b1a236dfa358)
![WhatsApp Image 2025-03-22 at 16 10 32_252217db](https://github.com/user-attachments/assets/9342c791-374f-4f81-8ba3-19c4a112a7e6)
![WhatsApp Image 2025-03-22 at 16 10 44_fcc42b58](https://github.com/user-attachments/assets/dc7c8d0d-174e-461e-ac64-21b366945358)


RESULT :
The Construction and Re-construction of impulse or ideal sampling using python are verified.
