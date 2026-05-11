# Land Cover Classification using CNN and Sentinel-2 Satellite Imagery

This project focuses on land cover classification from Sentinel-2 satellite imagery using a Convolutional Neural Network (CNN) implemented in PyTorch. The goal of the project is to classify satellite image patches into different land cover categories.

## Dataset

Official GitHub Repository: [EuroSAT GitHub Repository](https://github.com/phelber/EuroSAT)
Dataset Download (Zenodo): [EuroSAT Dataset Download](https://zenodo.org/records/7711810)


The project uses the EuroSAT RGB dataset, which contains Sentinel-2 satellite image patches grouped into 10 land cover classes:

- AnnualCrop
- Forest
- HerbaceousVegetation
- Highway
- Industrial
- Pasture
- PermanentCrop
- Residential
- River
- SeaLake


Reference:
Helber, P., Bischke, B., Dengel, A. and Borth, D. (2019) *EuroSAT: A Novel Dataset and Deep Learning Benchmark for Land Use and Land Cover Classification*.

---

## Technologies Used

- Python
- PyTorch
- NumPy
- Matplotlib
- scikit-learn

---

## CNN Architecture

A custom CNN architecture was implemented in PyTorch. The architecture is inspired by VGG-style CNN networks, using stacked convolutional layers with ReLU activations and max pooling operations for hierarchical spatial feature extraction.

The model consists of:
- 3 convolutional blocks
- ReLU activation functions
- MaxPooling layers
- Fully connected classifier layers
- Dropout regularization

Satellite image patches were resized to 64×64 pixels before training.

---

## Workflow

### 1. Data Preparation
- Loaded EuroSAT RGB dataset
- Applied image preprocessing and normalization
- Split dataset into training and testing sets

### 2. Model Training
- Trained CNN using CrossEntropyLoss and Adam optimizer
- Evaluated performance using:
  - Accuracy
  - Classification report
  - Confusion matrix

### 3. Prediction
- Saved trained model weights
- Loaded trained model for inference
- Performed predictions on random unseen satellite images
- Visualized predicted and true classes

---

## Results

The CNN demonstrated strong performance in distinguishing visually distinct land cover classes such as:
- Forest
- Industrial
- SeaLake
- Pasture

The project also highlighted challenges in differentiating visually similar classes such as:
- Highway
- Residential
- PermanentCrop

This demonstrates the importance of spatial feature extraction in satellite image classification tasks.

---
