# ConvNeXt-Powered Lung Sound Classification for Early COPD Detection

## Overview
Chronic Obstructive Pulmonary Disease (COPD) is a major global health concern, particularly in low- and middle-income countries where access to advanced diagnostic tools is limited. Early diagnosis is critical, yet traditional methods such as spirometry and imaging are resource-intensive and often unavailable at scale.

This project proposes a **non-invasive, deep learning–based framework for early COPD detection using lung sound recordings**. Respiratory audio signals are converted into Mel spectrograms and analyzed using a **ConvNeXt (Convolutional Neural Network for the 2020s)** architecture to classify lung sounds across multiple COPD severity levels.

---

## Key Contributions
- Developed an end-to-end pipeline for automated lung sound analysis using deep learning.
- Converted multi-channel lung sound recordings into fixed-length Mel spectrogram representations to preserve temporal–frequency patterns.
- Fine-tuned a ConvNeXt-based transfer learning model for multi-class COPD severity classification (COPD0–COPD4).
- Demonstrated the feasibility of scalable, low-cost respiratory screening using audio-based diagnostics.

---

## Methodology

### Dataset
- Multi-channel lung sound recordings  
- Minimum duration: 17 seconds per recording  
- Five COPD severity levels:
  - COPD0: No Disease  
  - COPD1: Mild  
  - COPD2: Moderate  
  - COPD3: Severe  
  - COPD4: Very Severe  

---

### Preprocessing Pipeline
1. Audio quality validation and noise filtering  
2. Fixed-window segmentation (600 ms intervals)  
3. Redundancy control to preserve data diversity  
4. Mel spectrogram generation  
5. Normalization and resizing to 224 × 224  

---

### Model Architecture
- Backbone: ConvNeXt-Base  
- Input: Mel spectrogram images  
- Transfer learning with pre-trained weights  
- Task-specific classification head for COPD severity prediction  

---

### Training Strategy
- Loss Function: Cross-Entropy Loss  
- Optimizer: Adam  
- Data Augmentation for improved generalization  
- GPU-accelerated training  
- Training and validation monitoring across epochs  

---

## Results
- Achieved high training accuracy (~98%), indicating effective feature learning from lung sound spectrograms  
- Successfully differentiated between multiple COPD severity levels  
- Validated the suitability of ConvNeXt for audio-to-image medical classification tasks  

---

## Applications
- Early COPD screening and risk stratification  
- Assistive clinical decision-support systems  
- Remote respiratory health monitoring  
- Deployment in low-resource and rural healthcare settings  

---

## Future Work
- Expansion to larger and more diverse patient cohorts  
- Improved generalization using advanced augmentation techniques  
- Integration of explainable AI (XAI) for clinical interpretability  
- Real-time inference for edge and mobile healthcare devices  

---

## Tech Stack
- Programming Language: Python  
- Deep Learning Framework: PyTorch  
- Model Architecture: ConvNeXt  
- Audio Processing: Librosa  
- Visualization and Analysis: NumPy, Matplotlib  

---

## Acknowledgements
This project is part of ongoing research into automated respiratory disease detection using machine learning and deep learning techniques.
