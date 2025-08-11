# handwriting-prediction
# 📝 Handwriting Prediction Using Machine Learning

## 📘 Project Overview
This project aims to build a machine learning system that can accurately recognize handwritten characters and words from images. In Week 1, the focus is on building a baseline CNN model using the MNIST dataset for digit recognition. Future weeks will extend this to word-level prediction using advanced architectures and datasets.

---

## 📅 Week 1: Baseline Character Recognition

### 🧠 Objective
Develop a Convolutional Neural Network (CNN) to classify handwritten digits (0–9) using the MNIST dataset.

### 📊 Dataset
- **MNIST**: 70,000 grayscale images of handwritten digits
- Image size: 28×28 pixels
- Format: Single-channel grayscale

### 🧪 Preprocessing
- Normalized pixel values to range [0, 1]
- Reshaped input to (28, 28, 1)
- Applied data augmentation: rotation, zoom, shift

### 🧠 Model Architecture
```text
Input: (28, 28, 1)
↓
Conv2D (32 filters, 3x3) + ReLU
↓
MaxPooling2D (2x2)
↓
Conv2D (64 filters, 3x3) + ReLU
↓
MaxPooling2D (2x2)
↓
Flatten
↓
Dense (128 units) + ReLU
↓
Dense (10 units) + Softmax
