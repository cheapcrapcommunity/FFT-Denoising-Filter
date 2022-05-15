
# De-noising with FFT (practice)

### How the code works

1. Add noise to a simple signal given by a sum of two sine waves. Plot the spectrograms for the clean and noisy signals to campare.

![Untitled](https://user-images.githubusercontent.com/76624368/168489003-bf755b80-4281-453d-a779-5b81dc8cf2cc.png)

1. Compute FFT and plot the power spectral density(PSD) of the noisy signal. Find the dominant peaks in the Fourier domain. Zero out the components below a threshhold and use fft.ifft to inverse transforming the filtered signal.

![Untitled 1](https://user-images.githubusercontent.com/76624368/168489009-d96c6545-352b-4e2b-83cf-864781302bb8.png)

1. Compare the waveforms, magnitudes and specgrams of the clean and filtered signals. If the similarity is high, it means success.

### Which points it illustrates

1. Pure sine waves with noise will form distinct peaks in the PSD and magitude spectrum, but it’s very difficult to see in the specgram.
2. The Fourier transform is reversible. That’s why after finding the threshold and zero out the less powerful components in the PSD, we can remove the noise and get a clean, filtered signal.
3. I applied this method on real world signals, and it didn’t give a good result as same as sinewaves. I think the reason is that this method relies on steady frequency and less time sensitive data. 

### How well it works

For pure digital sine waveforms it works very well. However, for real-world sounds, it is able to capture the frequencies of sources with a more pronounced frequency distribution, but does not work well for more complex sounds. Also, for sounds that are always changing, its time localisation is not accurate.


