ConvNeXt-Powered Lung Sound Classification for Early COPD Detection
Overview

Chronic Obstructive Pulmonary Disease (COPD) is one of the leading causes of morbidity and mortality worldwide, with a disproportionate burden in low- and middle-income countries. Early diagnosis remains challenging due to reliance on resource-intensive clinical procedures such as spirometry and imaging.

This project presents a non-invasive, deep learning–based approach for early COPD detection using lung sound recordings. By converting respiratory audio signals into visual representations and leveraging a ConvNeXt (Convolutional Neural Network for the 2020s) architecture, the system aims to accurately classify lung sounds across multiple COPD severity levels.

Key Contributions

Audio-to-Image Diagnostic Pipeline
Lung sound recordings are segmented into fixed 600 ms intervals and transformed into Mel spectrograms, preserving both temporal and frequency-domain characteristics crucial for respiratory pattern analysis.

Robust Preprocessing Framework
The pipeline includes audio quality checks, redundancy reduction, normalization, and standardized spectrogram generation to ensure dataset integrity and consistency across patients and recording channels.

ConvNeXt-Based Transfer Learning
A pre-trained ConvNeXt model is fine-tuned on lung sound spectrograms to classify five COPD severity levels (COPD0 to COPD4), enabling automated severity assessment rather than binary detection.

Scalable and Non-Invasive Screening
By relying solely on lung sound analysis, the approach demonstrates the feasibility of low-cost, scalable respiratory screening systems suitable for deployment in resource-constrained environments.

Methodology

Dataset

Multi-channel lung sound recordings

Each recording ≥ 17 seconds

Annotated across five COPD severity levels

Preprocessing

Fixed-length segmentation (600 ms windows)

Noise filtering and quality validation

Mel spectrogram generation

Dataset split into training, validation, and testing sets

Model Architecture

ConvNeXt-base architecture

Input resolution: 224 × 224

Transfer learning with task-specific classification head

Training Strategy

Cross-entropy loss

Adam optimizer

Data augmentation to improve generalization

GPU-accelerated training

Results

Achieved high training accuracy (~98%), demonstrating strong learning capability on lung sound spectrograms

Effective differentiation between varying COPD severity levels

Highlights the promise of deep learning–driven audio diagnostics in respiratory healthcare

Applications

Early-stage COPD screening

Assistive diagnostic tools for clinicians

Remote and telemedicine-based respiratory monitoring

Foundation for future multi-disease lung sound classification systems

Future Work

Expansion to larger and more diverse datasets

Improved generalization through advanced augmentation and regularization

Integration of explainable AI techniques for clinical interpretability

Real-time inference for edge or mobile deployment

Tech Stack

Language: Python

Framework: PyTorch

Model: ConvNeXt

Audio Processing: Librosa

Visualization: Matplotlib, NumPy
