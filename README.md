# EEG-Based Universal and Privacy-Preserving Authentication System

**Original Paper:** [Towards a universal and privacy preserving EEG-based authentication system](https://www.nature.com/articles/s41598-022-06527-7)
**Kaggle Notebook:** [ EEG-based authentication system](https://www.kaggle.com/code/gamalasran/eeg-authentication-system)

## 1. Introduction
This notebook implements the methodology proposed by Bidgoly et al. in the paper linked above (Scientific Reports, 2022). The system addresses three critical challenges in EEG biometrics:

1.  **Universality:** Capable of authenticating completely new users without retraining the model.
2.  **Privacy:** Stores an irreversible "fingerprint" vector instead of raw brainwaves, preventing the leakage of sensitive health information.
3.  **Ease of Use:** Reduces the required hardware to just three electrodes (Oz, T7, Cz) using Gram-Schmidt orthogonalization.

### Methodology Overview
We utilize a **Convolutional Neural Network (CNN)** not as a classifier, but as a feature extractor to generate unique "brain fingerprints." These fingerprints are authenticated using **Cosine Distance**. The system is tested on a dataset of 109 subjects, split into "Alpha" (known/training) and "Beta" (unknown/testing) groups to demonstrate universality.

![EEG authentication system](Images/EEG%20authentication%20system.png)

## System Components

### CNN Model Architecture
![CNN Model Architecture](Images/CNN%20Model%20Architecture.png)

### EEG Electrodes (Oz, T7, Cz)
![EEG Electrodes](Images/EEG%20%5B'Oz',%20'T7',%20'Cz'%5D.png)

### Sliding Window Approach
![Sliding Window](Images/sliding%20window.png)
