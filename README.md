# 🩺 Medical Image Classification with CNN & Transfer Learning

This project was completed as part of **GR5074: Projects in Advanced Machine Learning** at Columbia University. It explores the use of convolutional neural networks (CNNs) and transfer learning to classify chest X-ray images for detecting COVID-19, normal lungs, viral pneumonia, and lung opacity.

---

## 📂 Project Overview

The goal of this project is to build and compare multiple deep learning models that can classify chest X-ray images. The project follows a structured machine learning pipeline:

- Exploratory Data Analysis (EDA)
- Baseline CNN Model
- Transfer Learning using ResNet50
- Additional Architectures: VGG16, DenseNet121, EfficientNetB0
- Data Augmentation
- Performance Evaluation
- Interpretability & Practical Implications

---

## 📊 Dataset

- **Name**: COVID-19 Radiography Dataset  
- **Source**: [arXiv:2003.13145](https://arxiv.org/abs/2003.13145)  
- **Classes**:  
  - COVID-19  
  - NORMAL  
  - Viral Pneumonia  
  - Lung Opacity  
- **Preprocessing**: Images resized to 224x224 and normalized

---

## 🧠 Models Implemented

| Model           | Description                              |
|----------------|------------------------------------------|
| CNN (baseline)  | Custom 2-layer CNN from scratch          |
| ResNet50        | Pre-trained on ImageNet + fine-tuning    |
| VGG16           | Transfer learning with frozen backbone   |
| DenseNet121     | Deep network with feature reuse          |
| EfficientNetB0  | Lightweight and accurate modern model    |

All models were trained and evaluated on the same splits to ensure fair comparison.

---

## 🛠️ Augmentation Techniques

- Horizontal Flip  
- Random Rotation (±15°)  
- Width/Height Shift (±10%)  
- Zoom (up to 20%)  

These were applied using `ImageDataGenerator` in Keras and showed improvement in validation accuracy and generalization.

---

## 📈 Performance Summary

| Model           | Accuracy | F1-Score | Notes                         |
|----------------|----------|----------|-------------------------------|
| CNN (baseline)  | ~        | ~        | Tended to overfit             |
| ResNet50        | ~        | ~        | Improved generalization       |
| VGG16           | ~        | ~        | Higher parameter count        |
| DenseNet121     | ~        | ~        | Slow but stable               |
| EfficientNetB0  | ✅ Highest | ✅ Highest | Best overall performance      |

*Replace "~" with your actual results if available.*

---

## 📌 Real-World Impact

- Helps radiologists screen for COVID-19 and pneumonia.
- Beneficial for rural or resource-limited hospitals.
- Can be used in AI-assisted triage tools.

---

## 📁 Project Structure

```bash
📦 GR5074-Project2/
├── Project2_Medical_Image_Classification.ipynb
├── Project2_Medical_Image_Classification.pdf
├── images/                        # Visuals & plots
├── README.md                     # This file
└── data/                         # Not included in repo
