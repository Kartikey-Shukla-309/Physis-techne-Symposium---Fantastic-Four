# Physis-techne-Symposium---Fantastic-Four

# Project Overview

This project focuses on recovering a weak, deeply buried signal from noisy telemetry data using advanced Digital Signal Processing (DSP) techniques. The challenge involves data reconstruction, carrier and timing recovery, demodulation, and bit extraction.

# Objective:

Parse and reconstruct IQ data from hexadecimal text files.

Detect and extract a weak communication signal from high noise.

Implement carrier frequency and symbol timing recovery.

Demodulate the signal to extract transmitted bits.

# Dataset

Source: https://huggingface.co/datasets/AkshatRai07/PhysisTechne26Electronics
Format: 300 hexadecimal text files representing raw telemetry data.

Data Size: ~186 million samples (after reconstruction).

IQ samples are represented in interleaved real and imaginary format.

# Workflow
# 1. Signal Characteristics

Specify modulation type (BPSK, QPSK, etc.) if known.

Mention carrier frequency range and expected bandwidth.

Note the duration of signal versus noise segments.

# 2. Noise Analysis

SNR estimates before and after filtering.

Noise type (white Gaussian, thermal, interference, etc.).

Techniques used for noise suppression (bandpass filters, moving average, etc.).

# 3. Pre-processing Steps

DC offset removal.

Normalization of IQ samples.

Windowing or averaging applied before FFT.

# 4. Algorithm Choices & Justifications

Why K-means was chosen for demodulation.

Why Gardner or autocorrelation timing recovery was used.

Any alternative methods considered and why they were rejected.

# 5. Performance Metrics

Bit error rate (BER) if you compared extracted bits with ground truth.

Constellation diagram clarity before and after phase correction.

Carrier frequency estimation error.

# 6. Visualization

Spectrograms showing signal over time.

FFT plots showing carrier peak.

Constellation plots before and after clustering.

Timing error plots for symbol synchronization.

# 7. Optimizations

Memory-efficient parsing for large datasets.

Batch processing to handle huge IQ arrays.

Use of vectorized operations in numpy for speed.

# 8. Tools & Environment

Python version, OS, hardware specs (especially if large datasets).

Any Jupyter notebooks for interactive exploration.

Optional: GPU usage if FFT or clustering was accelerated.

# 9. Known Limitations

Uncertainty in phase offset for unsupervised demodulation.

Sensitivity to extreme frequency drift.

Signal detection may fail if SNR drops below a threshold.

# 10. Acknowledgements

Dataset provider or hackathon organizers.

Any libraries, frameworks, or mentors that helped.

# Report link
https://drive.google.com/file/d/1sYnyF3yrYjXH2HzWZ7mspeqqyFxemvCS/view?usp=sharing

# Video link
