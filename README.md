
[poster_EEG_MDD.pdf](https://github.com/user-attachments/files/18317105/poster_EEG_MDD.pdf)
# EEG-based Multimodal Classification of Major Depressive Disorder (MDD)

This repository contains the implementation and results of a research project aimed at developing a robust multimodal diagnostic pipeline for Major Depressive Disorder (MDD). By combining EEG and audio data, this project leverages advanced signal processing and deep learning techniques to improve the detection and classification of MDD.

---

## Overview

### Problem Statement
Depression, a prevalent mental illness, often goes undiagnosed due to subjective diagnostic methods. While neuroimaging techniques like fMRI and PET exist, they have limitations, such as invasiveness or high cost. EEG, being non-invasive, cost-effective, and high in temporal resolution, presents a promising alternative for studying depression. Combining EEG with audio data provides complementary insights, enhancing diagnostic accuracy.

### Objective
To classify MDD using EEG and audio data by:
1. Developing a robust EEG preprocessing pipeline.
2. Extracting meaningful features from EEG data (Power Spectral Density and Event-Related Potentials).
3. Exploring advanced fusion techniques for multimodal analysis.
4. Implementing deep learning models for classification.

---

## Methodology

### Dataset
- **Participants**: 53 subjects (24 MDD patients and 29 healthy controls).
- **EEG Data**: Resting state and dot-probe task data collected using a 128-channel HydroCel Geodesic Sensor Net.
- **Audio Data**: Collected through interviews, reading tasks, and picture descriptions.

### Data Preprocessing
**EEG Processing**:
1. **Import and Rereference**: Raw EEG data rereferenced to the average of all channels.
2. **Bandpass Filtering**: FIR filter applied (0.5-40 Hz) to remove noise.
3. **Artifact Removal**:
   - Automatic rejection using spectrum thresholding.
   - Manual inspection to remove residual artifacts.
4. **Independent Component Analysis (ICA)**:
   - Automatic component labeling using ICLabel.
   - Manual re-evaluation for ambiguous components.

### Feature Extraction
**EEG Features**:
- **Power Spectral Density (PSD)**:
  - Band power (Alpha: 8-13 Hz, Beta: 13-30 Hz).
  - Spectral entropy for alpha and beta bands.
- **Event-Related Potentials (ERP)**:
  - Features like peak amplitude, latency, mean absolute amplitude, and zero-crossing rate.

**Audio Features**:
- Acoustic, linguistic, and paralinguistic features from speech tasks (e.g., interviews, reading).

---

## Results
- **EEG Analysis**:
  - Significant differences in alpha and beta band powers between MDD and healthy subjects.
  - Resting state data showed more pronounced differences than task state data.
- **Hypothesis**: Resting state EEG features are likely more effective for future multimodal classification.

---

## Skills and Tools Utilized
- **Tools**:
  - [EEGLAB](https://sccn.ucsd.edu/eeglab/index.php) (MATLAB) for preprocessing and ICA.
  - [MNE-Python](https://mne.tools/stable/index.html) for PSD and ERP feature extraction.
- **Techniques**:
  - Advanced signal processing.
  - ICA for artifact removal and neural source separation.
  - Interpretation of EEG topographical maps and spectral characteristics.

---

## Future Directions
1. **Multimodal Fusion**:
   - Implement deep learning-based fusion techniques to integrate EEG and audio features.
2. **Deep Learning Models**:
   - Train CNN and RNN architectures for MDD classification.
3. **Biomarker Identification**:
   - Use feature selection methods to identify key markers of MDD.
4. **Real-Time Pipelines**:
   - Develop pipelines for real-time EEG and audio analysis.
5. **Generalization**:
   - Apply methodologies to other neurological and psychiatric disorders.

---

## How to Use This Repository

1. **Clone the Repository**:
   ```bash
   git clone <repository_url>
   ```

2. **Dependencies**:
   Install the required libraries:
   ```bash
   pip install -r requirements.txt
   ```

3. **Data Preprocessing**:
   - EEG preprocessing scripts are in the `preprocessing` directory.
   - Feature extraction scripts for PSD and ERP are in the `features` directory.

4. **Analysis**:
   - Explore the results in the `results` directory, including topographical maps and feature distributions.

---



## Contact
For any queries or collaborations, reach out to [Stuti Wadhwa](mailto:stuti.wadhwa1@gmail.com).

