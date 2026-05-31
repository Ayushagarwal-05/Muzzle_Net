# 🐄 Muzzle_Net: Cattle Identification Using Muzzle Biometrics

## Overview

Muzzle_Net is a deep learning-based cattle identification system that uses unique muzzle patterns as a biometric identifier. The project combines object detection, metric learning, and similarity search to identify cattle from images.

The system performs:

1. Muzzle Detection using YOLOv8
2. Feature Extraction using ArcFace + ResNet50
3. Similarity Search using FAISS
4. Known / Unknown Cattle Identification

---

## Motivation

Traditional cattle identification methods such as ear tags, RFID chips, and branding can be lost, damaged, duplicated, or tampered with.

Similar to human fingerprints, cattle muzzle patterns are unique and remain relatively stable over time. This project leverages muzzle biometrics to create a non-invasive identification system.

---

## System Architecture

```text
Cow Image
    ↓
YOLOv8 Muzzle Detector
    ↓
Muzzle Crop
    ↓
ArcFace Feature Extractor
    ↓
512-D Embedding
    ↓
FAISS Similarity Search
    ↓
Known / Unknown Cow
```

---

## Technologies Used

### Deep Learning

* PyTorch
* Torchvision
* ResNet50
* ArcFace Metric Learning

### Object Detection

* YOLOv8
* Ultralytics

### Similarity Search

* FAISS

### Data Processing

* OpenCV
* NumPy
* Pandas
* Albumentations

### Visualization

* Matplotlib
* Seaborn

---

## Project Workflow

### Dataset Preparation

* Dataset analysis
* Dataset cleaning
* Identity-based train/validation split
* Data augmentation

### Embedding Learning

* ResNet50 backbone
* ArcFace loss
* 512-dimensional feature embeddings

### Retrieval System

* FAISS vector database
* Cosine similarity search
* Top-K cattle retrieval

### Real-World Inference

* YOLOv8 muzzle localization
* Automatic muzzle cropping
* Embedding generation
* Identity prediction

---

## Repository Structure

```text
Muzzle_Net/
│
├── notebooks/
│   ├── 01_environment_test.ipynb
│   ├── 02_dataset_analysis.ipynb
│   ├── 03_dataset_cleaning.ipynb
│   ├── 04_dataset_split.ipynb
│   ├── 05_create_dataset_splits.ipynb
│   ├── 06_pytorch_dataset_and_augmentation.ipynb
│   ├── 07_resnet50_embedding_model.ipynb
│   ├── 08_arcface_metric_learning.ipynb
│   ├── 09_arcface_retrieval_evaluation.ipynb
│   ├── 10_faiss_vector_search.ipynb
│   ├── 11_yolo_label_generation.ipynb
│   ├── 12_train_yolo_detector.ipynb
│   ├── 13_test_yolo_detector.ipynb
│   ├── 14_train_yolo_manual.ipynb
│   ├── 15_identity_recognition_pipeline.ipynb
│   ├── 16_real_world_cattle_identification.ipynb
│   └── 17_evaluation_and_metrics.ipynb
│
├── requirements.txt
├── .gitignore
└── README.md
```

---

## Experimental Results

### Identification Performance

| Metric         | Value  |
| -------------- | ------ |
| Top-1 Accuracy | 65.27% |
| Top-5 Accuracy | 98.09% |
| Precision      | 67.15% |
| Recall         | 99.76% |
| F1 Score       | 80.27% |

### Similarity Statistics

| Metric                        | Value  |
| ----------------------------- | ------ |
| Mean Same-Cow Similarity      | 0.9269 |
| Mean Different-Cow Similarity | 0.6016 |

---

## Example Results

### Known Cow

```text
Cow ID: 9
Similarity: 0.9708
Status: Known Cow
```

### Unknown Cow

```text
Similarity: 0.3747
Status: Unknown Cow
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/Ayushagarwal-05/Muzzle_Net.git
cd Muzzle_Net
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Running the Project

### Identity Recognition

```text
15_identity_recognition_pipeline.ipynb
```

### Real-World Identification

```text
16_real_world_cattle_identification.ipynb
```

### Evaluation Metrics

```text
17_evaluation_and_metrics.ipynb
```

---

## Future Work

* Streamlit web application
* Mobile deployment
* Multi-view cattle recognition
* Larger cattle datasets
* Real-time farm monitoring
* Edge AI deployment

---

## Author

Ayush Agarwal

B.Tech Computer Science & Engineering

Interests:

* Computer Vision
* Deep Learning
* Machine Learning
* AI Research

GitHub:
https://github.com/Ayushagarwal-05

---

## License

This project is intended for academic and research purposes.
