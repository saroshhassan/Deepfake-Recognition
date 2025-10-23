# Deepfake Recognition
This project explores deepfake detection using CNN models trained on a subset of the Real and Synthetic Faces Dataset (Mendeley Data). It includes end-to-end preprocessing with feature extraction (Color Histogram, LBP, Edge Density), model tuning with Keras Tuner, and evaluation with recall-based early stopping. Visual analyses are also provided.

# Deepfake Detection using CNN and ResNet Architectures

This repository presents a deep learning approach to **deepfake face detection**, combining **Convolutional Neural Networks (CNN)** and **ResNet-style architectures**.  
The models were trained on a subset of the *Comprehensive Deepfake Detection Dataset * from Mendeley Data.  
Due to hardware constraints, the dataset was downsampled while preserving class balance between real and fake images.

---

## Overview

Deepfakes pose a growing threat to digital trust, driven by advances in AI-generated imagery.
This project develops a deepfake detection pipeline that integrates **feature extraction** (Color Histograms, Local Binary Patterns, and Edge Density) with CNN-based architectures.  
Two models are trained and compared:
1. **Baseline CNN** — A lightweight convolutional model with varying kernel sizes (3×3, 5×5, 7×7) for low- and high-level feature capture.  
2. **ResNet-style Model** — Incorporates progressive filter growth (32→64→128→256) for deeper representation learning.

The final model achieves **over 97% recall** using Keras Tuner–optimized hyperparameters and recall-based early stopping.

---

## Features

- **Dataset**: Comprehensive Deepfake Detection Dataset: Real and Synthetic Frames from Roop and Akool AI Technologies  
- **EDA**:  
  - Color Histogram similarity  
  - Local Binary Pattern (LBP) texture analysis  
  - Edge density mapping  
-  **Preprocessing Pipeline**:  
  - Normalization  
  - Stratified 80/20 split  
  - Data augmentation and feature concatenation  
- **Models**:  
  - Custom CNN with variable kernel filters  
  - ResNet-style model with progressive filter growth  
- **Hyperparameter Optimization**:  
  - Keras Tuner Random Search  
  - Early stopping at recall > 98%  
- **Evaluation**:  
  - Accuracy,, Recall, F1-score  
  - Confusion Matrix (heatmap)  
  - Visualization of first 5 misclassified samples  

---

## Dataset

**Source:**  
[Mendeley Data – Real and Synthetic Faces Dataset](https://data.mendeley.com/datasets/pdcp9mjy3z/1)

**Citation DOI:** 10.17632/pdcp9mjy3z.1
**Description:** 110,694 labeled frames extracted from real and deepfake videos.  
For this project, a subset of over 8,000 images was used due to hardware limitations.

---

## Installation

Clone the repository:
```bash

git clone https://github.com/saroshhassan/deepfake-detection-cnn.git

cd deepfake-detection-cnn

jupyter notebook Deepfake_Detection.ipynb
```

