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

![image](https://github.com/user-attachments/assets/4f659202-dd0c-4f9e-94e3-ee6ca01fb4e2)
![image](https://github.com/user-attachments/assets/d4dee778-6738-4072-a25a-7da1b54572a7)
![image](https://github.com/user-attachments/assets/0213785f-32a0-4baf-b2c9-e5aa21515543)



RESULT :
The Construction and Re-construction of impulse or ideal sampling using python are verified.
