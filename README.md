**EuroSAT-ML-CNN****
Classification of EuroSAT RGB satellite images using Classical ML, Ensemble Methods, and CNNs.

**📌 Overview**

This project provides a complete workflow for EuroSAT RGB dataset classification, including:

Data preprocessing and visualization

Feature extraction for classical ML

Training, hyperparameter tuning, and evaluation of models

Ensemble learning with soft voting and SMOTE

Convolutional Neural Network (CNN) implementation

Performance comparison across all models

**📂 Dataset**

EuroSAT RGB dataset: 27,000 labeled satellite images (64×64) across 10 classes:

AnnualCrop, Forest, HerbaceousVegetation, Highway, Industrial, Pasture, PermanentCrop, Residential, River, SeaLake

Dataset URL: EuroSAT GitHub

**🛠 Project Structure**
.
├── data/               # Dataset (if stored locally)
├── notebooks/          # Jupyter notebooks for experiments
├── src/                # Scripts for preprocessing, feature extraction, and training
├── models/             # Saved trained models (optional)
├── README.md           # Project documentation
└── requirements.txt    # Required Python packages

**⚙️ Setup**

Install required packages:

pip install tensorflow scikit-learn opencv-python matplotlib scikit-image imbalanced-learn seaborn pandas

**🔹 Methods & Models**

**1. Classical ML Models**

Logistic Regression, SVM, KNN

Feature extraction: grayscale stats, histogram, edge detection
Hyperparameter tuning via GridSearchCV

****2. Voting Ensembles****

Soft voting ensemble of Logistic Regression, SVM, and KNN

Optional SMOTE resampling for class imbalance

**3. Convolutional Neural Network (CNN)**

Sequential CNN with Conv2D, MaxPooling, Dense, Dropout

Trained on normalized RGB images

One-hot encoded labels for 10 classes

**📊 Results
**
Classical ML: Accuracy ~0.48–0.63

Voting Ensemble: Slight improvement over individual models

CNN: Highest test accuracy on RGB images

Summary table and bar plot compare all models

**📈 Visualizations**

Confusion matrices for all models

Accuracy comparison bar plot

Preprocessing and feature extraction visuals (grayscale, edges, histograms)
