# EEG Classification Model

### Project Overview
This project focuses on building a machine learning model to classify EEG data to assist in diagnosing neurological disorders, particularly epilepsy. The goal is to distinguish between seizure and non-seizure EEG data using advanced machine learning and deep learning techniques, specifically Decision Trees and Convolutional Neural Networks (CNNs).

### Table of Contents
1. [Introduction](#introduction)
2. [Objective](#objective)
3. [Datasets](#datasets)
4. [Methodology](#methodology)
5. [Modeling](#modeling)
6. [Results](#results)
7. [Conclusion](#conclusion)
8. [References](#references)

---

### Introduction
EEG data plays a crucial role in understanding brain activity and diagnosing neurological conditions such as epilepsy. Epilepsy is a disorder in which brain activity becomes abnormal, causing seizures. This project aims to improve the classification of EEG data to aid in the early detection and treatment of epilepsy.

---

### Objective
The primary objective of this project is to develop a robust EEG classification model that can distinguish between different types of seizure data and normal brain activity. The key goals are:
1. Data preprocessing and cleaning.
2. Feature extraction using time and frequency domain techniques.
3. Model development using Decision Trees and CNNs.
4. Model validation and testing.
5. Comparative analysis of model performance.

---

### Datasets
This project leverages two EEG datasets:
1. **CHB-MIT EEG Database**: A pediatric EEG dataset used to study epilepsy.
2. **Bonn EEG Dataset**: A specialized dataset focusing on epileptic seizure-related EEG data.

Both datasets include a mix of seizure and non-seizure data, providing a comprehensive base for training and testing the classification models.

---

### Methodology
#### Data Preprocessing
1. **Data Loading**: EEG data is loaded using Python libraries such as `pyedflib` and `mne`.
2. **Bandpass Filtering**: Applied to retain frequencies between 1-50 Hz, removing noise.
3. **Feature Extraction**:
   - **Basic Features**: Statistical measures like mean, standard deviation, and entropy.
   - **Advanced Features**: Using Short-Time Fourier Transform (STFT) to capture spectral features.
4. **Data Splitting**: Using SMOTE for data balancing and dividing data into training, validation, and test sets.

---

### Modeling
Two models were implemented:
1. **Decision Tree**:
   - Easily interpretable, capable of handling non-linear relationships in EEG data.
   - Utilized features extracted from EEG data without extensive preprocessing.
   
2. **Convolutional Neural Network (CNN)**:
   - Automatically learns spatial and temporal features from EEG data.
   - The model architecture included convolutional layers, pooling layers, and fully connected layers for classification.

---

### Results
1. **Decision Tree**:
   - Accuracy: 89.34%
   - F1 Score: 89.49%
   - AUC: 0.55 (indicating moderate classification performance)

2. **CNN**:
   - Accuracy: 67.68%
   - F1 Score: 69.61%
   - AUC: 0.70 (demonstrating better capability in distinguishing between seizure and non-seizure events)

#### Visualizations
- **Training vs Validation Metrics**: Accuracy and loss plots to monitor model performance.
- **Comparative ROC Curve**: Displaying AUC for both Decision Tree and CNN models.

---

### Conclusion
The CNN model outperformed the Decision Tree in classifying EEG data, especially in capturing complex patterns in the data. The project shows the potential for deep learning models in medical data analysis. Future work should explore further optimization of model parameters and more advanced architectures to improve classification accuracy.

---

### References
- CHB-MIT EEG Dataset: [Link](https://physionet.org/content/chbmit/1.0.0/)
- Bonn EEG Dataset: [Link](https://epilepsy.uni-freiburg.de/)

