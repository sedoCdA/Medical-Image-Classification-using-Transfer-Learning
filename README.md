# Medical Image Classification using Transfer Learning

## Overview

This project builds a medical image classification system using transfer learning.

A pre-trained deep learning model is used to classify chest X-ray conditions.

---

## Dataset

File: medical_imaging_meta.csv

Contains:
- Image metadata
- Condition labels

Note:
Images are simulated for demonstration.

---

## Workflow

### 1. Data Analysis
- Checked label distribution
- Identified class imbalance

---

### 2. Feature Extraction

Used MobileNetV2:
- Pre-trained on ImageNet
- Frozen layers
- Added custom classification head

---

### 3. Fine-Tuning

- Unfroze last layers
- Used low learning rate
- Improved model performance

---

### 4. Evaluation

Used:
- Classification report
- Per-class performance

Important:
Some classes perform worse due to fewer samples

---

### 5. Model Explainability

Used saliency maps:
- Highlight important regions in image
- Helps doctors understand predictions

---

### 6. Unlabeled Prediction

- Predicted last 30 samples
- Assigned confidence scores

---

## Theory

### Transfer Learning

Using knowledge from a pre-trained model.

Advantages:
- Requires less data
- Faster training

---

### Feature Extraction

- Freeze base model
- Train only new layers

---

### Fine-Tuning

- Unfreeze some layers
- Adjust model for new dataset

---

### Why Not Train from Scratch

Dataset is small:
- Training from scratch leads to overfitting

---

### Class Imbalance

Some classes have fewer samples:
- Model may ignore them
- Important in medical tasks

---

### Saliency Maps

Used for explainability:
- Shows which part of image influenced prediction

---

## How to Run

1. Open Google Colab
2. Upload dataset
3. Run all cells

---

## Requirements

pip install pandas numpy matplotlib scikit-learn tensorflow

---

## Key Learnings

- Transfer learning is powerful for small datasets
- Fine-tuning improves performance
- Explainability is critical in healthcare
- Class imbalance must be handled carefully
