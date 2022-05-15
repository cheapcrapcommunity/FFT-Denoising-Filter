

# De-noising with FFT (practice)

### How the code works

1. Add noise to a simple signal given by a sum of two sine waves. Plot the spectrograms for the clean and noisy signals to campare.

![Untitled](De-noising%20with%20FFT%2014c6892dc04a47eda0f31e80b14fc012/Untitled.png)

1. Compute FFT and plot the power spectral density(PSD) of the noisy signal. Find the dominant peaks in the Fourier domain. Zero out the components below a threshhold and use fft.ifft to inverse transforming the filtered signal.

![Untitled](De-noising%20with%20FFT%2014c6892dc04a47eda0f31e80b14fc012/Untitled%201.png)

1. Compare the waveforms, magnitudes and specgrams of the clean and filtered signals. If the similarity is high, it means success.

### Which points it illustrates

1. Pure sine waves with noise will form distinct peaks in the PSD and magitude spectrum, but it’s very difficult to see in the specgram.
2. The Fourier transform is reversible. That’s why after finding the threshold and zero out the less powerful components in the PSD, we can remove the noise and get a clean, filtered signal.
3. I applied this method on real world signals, and it didn’t give a good result as same as sinewaves. I think the reason is that this method relies on steady frequency and less time sensitive data. 

### How well it works

For pure digital sine waveforms it works very well. However, for real-world sounds, it is able to capture the frequencies of sources with a more pronounced frequency distribution, but does not work well for more complex sounds. Also, for sounds that are always changing, its time localisation is not accurate.

### Improved the implementation based on peers’ input

They thought the method was amazing because the sine wave in the noise could not be distinguished in the human ear. 

But as a tool, it was really cumbersome to run the code block by block, so they suggested that I improve it so that the person testing it could just change the frequency and run all the code at once. And it is better to place all the figures as close to each other as possible to help comparison.
