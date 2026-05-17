# Blood Cell Anomaly Detection using Deep Learning & Digital Image Processing

<div align="center">

## White Blood Cell Classification Pipeline  
### CLAHE • FFT • Custom Otsu • CNN Feature Extraction • LBP • GLCM • Machine Learning

</div>

---

## 📌 Project Overview

This project presents a complete **blood cell anomaly detection and white blood cell (WBC) classification pipeline** combining:

- Classical **Digital Image Processing**
- **Frequency Domain Enhancement**
- **Custom Image Segmentation**
- **Deep Learning Feature Extraction**
- **Handcrafted Texture Features**
- **Machine Learning Classification**

The system classifies white blood cells into four categories:

- Eosinophil
- Lymphocyte
- Monocyte
- Neutrophil

The project was developed for the **Digital Image Processing (DIP) Spring 2026** course.

---

# 🧠 Project Pipeline

```text
Raw Blood Cell Image
        │
        ▼
CLAHE Contrast Enhancement
        │
        ▼
Median Noise Filtering
        │
        ▼
Butterworth High-Pass Filter (FFT)
        │
        ▼
Custom Otsu Segmentation
        │
        ▼
Feature Extraction
 ┌─────────────────────────────┐
 │  CNN Features               │
 │  • VGG16                    │
 │  • ResNet50                 │
 │  • EfficientNetB0           │
 └─────────────────────────────┘
                +
 ┌─────────────────────────────┐
 │ Handcrafted Features        │
 │ • Local Binary Pattern      │
 │ • GLCM Haralick Features    │
 └─────────────────────────────┘
        │
        ▼
Feature Fusion
        │
        ▼
PCA + SelectKBest
        │
        ▼
Classification
(SVM / KNN / Random Forest)

# 📂 Dataset

This project uses the **Blood Cell Images Dataset** available on Kaggle.

## 🔗 Dataset Link

https://www.kaggle.com/datasets/paultimothymooney/blood-cells

---

## 📊 Dataset Information

The dataset contains approximately **12,500 microscopic blood cell images** divided into four white blood cell categories:

| Class | Number of Images |
|---|---|
| EOSINOPHIL | ~2497 |
| LYMPHOCYTE | ~2483 |
| MONOCYTE | ~2478 |
| NEUTROPHIL | ~2499 |

The images are already organized into folders for training and testing.

---

## 📁 Dataset Structure

```text
dataset/
└── dataset2-master/
    └── dataset2-master/
        └── images/
            ├── TRAIN/
            │   ├── EOSINOPHIL/
            │   ├── LYMPHOCYTE/
            │   ├── MONOCYTE/
            │   └── NEUTROPHIL/
            │
            ├── TEST/
            └── TEST_SIMPLE/
