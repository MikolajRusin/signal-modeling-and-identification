# Laboratory Tasks

## Laboratory 1

### 1.1 Frequency Resolution
In this task, we created a signal `y` composed of two sinusoids at frequencies of 30 Hz and 30.5 Hz. We calculated the Fourier Transform of the signal using FFT and displayed its amplitude-frequency spectrum. The task involved analyzing the relationship between signal length and frequency resolution by adjusting the signal length until the two frequency components were clearly distinguishable.

### 1.2 Spectral Leakage and Windowing
This task focused on understanding spectral leakage and the effects of windowing. We created a signal consisting of a 7 Hz sine wave and a 20 Hz cosine wave, and then calculated and plotted its Fourier Transform on a logarithmic scale. We also explored the effects of changing the number of samples and compared the results. Next, we applied a Hanning window to the signal to reduce spectral leakage and compared the resulting frequency spectrum to the original signal without windowing.

### 1.3 Sampling Frequency Change
Here, we created a signal consisting of two cosines at frequencies of 125 Hz and 375 Hz and analyzed the effect of downsampling the signal by keeping every second sample. The task involved comparing the frequency spectra and time-domain signals of the original and downsampled signals. We further explored the effects of downsampling on the frequency spectrum, particularly in terms of aliasing and frequency resolution.

## Laboratory 2

### 1.1 Signal Correlation
In this task, we generated a signal `y` with a sampling frequency of 2000 Hz and length of 2000 samples. We then created a chirp signal `yp` with a variable frequency, starting at 10 Hz and ending at 300 Hz. Using correlation (`xcorr`) and convolution (`conv`), we compared the results and analyzed the differences in the time-domain plots. We also experimented with different parameter combinations for the chirp signal to observe how the time-domain width of the correlation result depends on the signal’s frequency bandwidth.

### 1.2 Matched Filtering
We applied matched filtering to detect impulses in an audio recording containing synthetic signals in the form of sinusoids with increasing frequency. We used the provided reference pulse to perform matched filtering and detect the impulses in both channels of the audio signal. The task involved working in both the time and frequency domains using FFT and inverse FFT to improve the detection accuracy.

### 1.3 Signal Detection with Noise
This task extended the previous impulse detection exercise by introducing white noise with varying amplitudes into the signal. We performed correlation analysis on the noisy signal and observed the effects of noise on the detection of the impulse. We analyzed how the correlation results varied with different levels of noise and assessed the effectiveness of matched filtering in identifying the signal amidst the noise.

### 1.4 Frequency Domain Signal Processing
In this task, we processed the audio signal in the frequency domain by multiplying the Fourier transform of the reference pulse with the Fourier transform of the noisy signal. We performed zero-padding to match the length of the signals before applying inverse FFT to get the correlation result in the time domain. The task involved comparing time-domain results with those obtained from direct correlation and discussing the differences.
