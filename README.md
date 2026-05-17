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