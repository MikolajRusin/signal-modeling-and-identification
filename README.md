# Laboratory Tasks

---

# Laboratory 1

### 1.1 Frequency Resolution 📏
In this task, we created a signal `y` consisting of two sinusoids at frequencies of 30 Hz and 30.5 Hz. We then calculated the Fourier Transform of the signal using FFT and plotted its amplitude-frequency spectrum. The task involved analyzing the relationship between signal length and frequency resolution by adjusting the signal length until both frequency components were clearly distinguishable. 

### 1.2 Spectral Leakage and Windowing 🪟
We created a signal consisting of a 7 Hz sine wave and a 20 Hz cosine wave. We calculated the Fourier Transform of this signal and analyzed the spectrum using a logarithmic scale. The task also included exploring the effects of changing the number of samples on spectral leakage. We applied a Hanning window to the signal to reduce spectral leakage and compared the resulting frequency spectrum with the original signal.

### 1.3 Sampling Frequency Change 📉
Here, we created a signal consisting of two cosines at frequencies of 125 Hz and 375 Hz and explored the effect of downsampling the signal by keeping every second sample. We compared the frequency spectra and time-domain signals of the original and downsampled signals, and analyzed the impact of downsampling on the frequency spectrum and resolution.

---

# Laboratory 2 🎶

## 1. Signal Correlation 📡

### 1.1 Signal Generation and Correlation
In this task, we created a signal `y` with a sampling frequency of 2000 Hz and a length of 2000 samples. An empty signal vector was initialized, followed by the creation of a second chirp signal `yp` with a frequency range from 10 Hz to 300 Hz. The chirp signal was multiplied by a Hanning window of the same length. The signal `yp` was added to `y` starting from the 500th sample. Next, we calculated the correlation between `y` and `yp` using the `correlate` function and plotted the results in the time domain. We also compared the results using the convolution function (`convolve`) and discussed the differences in their implementation.

### 1.2 Correlation with Varying Parameters
We performed correlation on signals with different frequency parameters:
- The length of `yp` was 200 samples with different values for `f2` (100 Hz, 200 Hz, 500 Hz) while `f1` remained 30 Hz.
- The second set of tests used `f1 = 500 Hz` and `f2 = 500 Hz`.

We plotted the correlation results for each combination and analyzed the relationship between the time width of the correlation result and the frequency bandwidth of the signal `yp`.

### 1.3 Impulse Detection in Signal with Multiple Instances
We added a signal `yp` with a length of 1000 samples (starting at 500th and 750th samples with amplitudes of 1 and 0.5, respectively) to `y`. We then calculated the correlation between the newly created signal `y` and `yp` and analyzed the detected impulses. We calculated the time intervals between the impulses and discussed how their locations relate to the positions of `yp` within `y`.

### 1.4 Signal Correlation with Noise 🌫️
We added white noise with varying standard deviations (0.5, 1, and 2) to the signal `y` created in task 1.3. We performed correlation between the noisy signal and `yp`, and plotted the results in the time domain for each noise level. The task involved analyzing how noise levels affected the visibility of correlation peaks in the signal.

---

## 2. Matched Filtering 🎯

### 2.1 Signal Detection in Audio Recording
In this task, we analyzed an audio recording containing synthetic signals in both channels with increasing frequencies. The goal was to locate the impulses within the audio recording. The reference impulse was provided in the file `pulse.csv`. The audio to analyze is provided in the file `audio.wav`. Using matched filtering, we detected the impulses and identified the exact locations and channels where the signal appeared.

### 2.2 Frequency Domain Signal Processing
We repeated the analysis from task 2.1 in the frequency domain. We performed the conjugate multiplication of the Fourier transform of the reference pulse `ypf` and the Fourier transform of the audio signal `yf`. Zero-padding was applied to the pulse signal to match the length of the audio signal's Fourier transform. We then used the inverse FFT (`ifft`) to compute the correlation in the time domain and compared the results with the time-domain correlation. The task involved visualizing the time-domain signals, comparing them with the frequency-domain filtering, and discussing the results.

---

