EuroSAT-ML-CNN

Classification of EuroSAT RGB satellite images using classical ML models, ensemble methods, and CNNs.

Table of Contents

Overview

Dataset

Project Structure

Setup

Models & Methods

Results

Visualization

License

Overview

This repository provides a complete workflow for classifying the EuroSAT RGB dataset using:

Classical ML models (Logistic Regression, SVM, KNN)

Voting Ensembles (with and without SMOTE)

Convolutional Neural Networks (CNN)

It includes data preprocessing, feature extraction, model training, hyperparameter tuning, evaluation, and comparison.

Dataset

The EuroSAT RGB dataset consists of 27,000 labeled satellite images across 10 classes.

RGB images (64×64)

Classes include: AnnualCrop, Forest, HerbaceousVegetation, Highway, Industrial, Pasture, PermanentCrop, Residential, River, SeaLake

Source: EuroSAT GitHub

Project Structure
.
├── data/               # Dataset (if downloaded locally)
├── notebooks/          # Jupyter notebooks for experiments
├── src/                # Scripts for preprocessing, feature extraction, and training
├── models/             # Saved models (optional)
├── README.md
└── requirements.txt

Setup

Install the required packages:

pip install tensorflow scikit-learn opencv-python matplotlib scikit-image imbalanced-learn seaborn pandas


Optional (if using Google Colab):

from google.colab import drive
drive.mount('/content/drive')

Models & Methods

Classical ML Models

Logistic Regression, SVM, KNN

Feature extraction: grayscale stats, edge detection, histograms

Hyperparameter tuning with GridSearchCV

Voting Ensembles

Soft voting ensemble of the three classical models

Handling class imbalance with SMOTE

CNN

Sequential CNN with Conv2D, MaxPooling, Dense, and Dropout layers

Trained on normalized RGB images

Results

Classical ML models achieve accuracies around 0.48–0.63

Voting ensemble improves performance slightly

CNN provides higher accuracy on RGB images

Final performance comparison is summarized in a table and bar plot

Visualization

Confusion matrices for all models

Accuracy comparison bar plot

Preprocessing and feature extraction visualizations (grayscale, edges, histograms)

License

This project is open-source. You can freely use and modify it for educational or research purposes.
