# Physis-techne-Symposium---Fantastic-Four

Project Overview

This project focuses on recovering a weak, deeply buried signal from noisy telemetry data using advanced Digital Signal Processing (DSP) techniques. The challenge involves data reconstruction, carrier and timing recovery, demodulation, and bit extraction.

Objective:

Parse and reconstruct IQ data from hexadecimal text files.

Detect and extract a weak communication signal from high noise.

Implement carrier frequency and symbol timing recovery.

Demodulate the signal to extract transmitted bits.

Dataset

Source: [Provide Dataset Link or Location]

Format: 300 hexadecimal text files representing raw telemetry data.

Data Size: ~186 million samples (after reconstruction).

IQ samples are represented in interleaved real and imaginary format.

Workflow
Stage 0: Data Reconstruction

Convert hexadecimal text files into complex floating-point IQ samples.

Implement memory-efficient parsing using batch or streaming processing.

Save reconstructed IQ samples as .npy files for easier processing.

Stage I: Signal Detection

Perform spectral analysis to confirm signal presence.

Estimate carrier frequency and frequency drift.

Tools: FFT, periodogram, and signal averaging techniques.

Stage II: Carrier & Timing Recovery

Lock onto drifting carrier using frequency correction techniques.

Recover symbol clock using methods like Gardner Timing Error Detector or autocorrelation.

Adjust sampling to one sample per symbol for accurate demodulation.

Stage III: Demodulation

Apply phase correction and symbol alignment.

Use K-means clustering for constellation demodulation (for BPSK/QPSK).

Extract raw bits from demodulated symbols.

Stage IV: Bit Extraction & Analysis

Convert symbol sequence into binary bits.

Validate extracted bits using checksum or known patterns.

Optionally, reconstruct transmitted messages or telemetry info.
