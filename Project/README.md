# In-Ear ECG Signal Enhancement using a Denoising Convolutional Autoencoder

This repository contains the implementation of my final project for Data Science 2025, reproducing the work from Occhipinti et al. (arXiv:2409.05891v1). The project focuses on enhancing the quality of Electrocardiogram (ECG) signals recorded from in-ear sensors, a promising platform for continuous, unobtrusive health monitoring.

**The Challenge:** In-ear ECG signals have an amplitude approximately 100x smaller than standard chest ECGs, making them highly susceptible to contamination from physiological noise (EEG, EOG, EMG) and motion artifacts. This results in a very low Signal-to-Noise Ratio (SNR), often making the signal resemble brain activity more than a heart signal.

**The Solution:** A **Denoising Convolutional Autoencoder (DCAE)** was developed to map noisy in-ear ECG signals to clean, clinical-grade Lead I ECG traces. The model was trained to separate the underlying cardiac signal from noise without relying on rigid frequency-based filters, instead learning the intrinsic manifold of clean ECG waveforms.

**Key Achievements:**
*   **Significant SNR Improvement:** Achieved a median SNR boost of **+10 dB**.
*   **Accurate Heart Rate Estimation:** Reduced the Mean Absolute Error (MAE) in heart rate estimation by **75%** using a Matched Filter Hilbert Transform (MFHT) algorithm.
*   **Waveform Preservation:** The model successfully preserves the clinically critical P-QRS-T complex morphology, even showing robustness in cases of mild arrhythmias and motion artifacts.

**Repository Contents:**
*   PyTorch implementation of the DCAE architecture.
*   Code for data augmentation using synthetic pink noise on the PTB-XL dataset.
*   Training scripts with MSE loss.
*   Evaluation metrics code (SNR calculation, HR estimation with MFHT).
*   Jupyter notebooks for result visualization.

This project demonstrates the potential of deep learning to enable high-quality cardiac monitoring through everyday hearable devices.

**Link to Original Paper:** [https://arxiv.org/abs/2409.05891](https://arxiv.org/abs/2409.05891)
