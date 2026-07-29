# Imbalance-Aware Multiclass Diabetes Classification using Machine Learning

## Overview

This project implements an imbalance-aware machine learning framework for multiclass diabetes classification using clinical data. The objective is to accurately classify patients into one of three categories:

- Non-Diabetic
- Pre-Diabetic
- Diabetic

The implementation follows the methodology presented in our paper:

> **Imbalance-Aware ML for Multiclass Classification of Diabetes Data**

The framework focuses on handling class imbalance using synthetic oversampling techniques and compares the performance of multiple machine learning algorithms.

---

## Features

- Data preprocessing pipeline
- Missing value imputation
- Label encoding
- Feature standardization
- Class imbalance handling using:
  - SMOTE
  - ADASYN
- Training of eight machine learning classifiers
- Stacking ensemble model
- Performance evaluation using multiple metrics
- Visualization using confusion matrices and radar plots

---

## Dataset

The implementation supports two publicly available datasets from Mendeley Data.

### Dataset 1

- Diabetes Dataset
- 1000 patient records

### Dataset 2

- Multiclass Diabetes Dataset
- 264 patient records

Each dataset contains clinical and biochemical attributes such as:

- Age
- Gender
- BMI
- HbA1c
- Blood Glucose
- Creatinine
- Cholesterol Levels
- Triglycerides
- Urea
- VLDL
- HDL
- LDL

Target Classes:

| Label | Description |
|--------|-------------|
| 0 | Non-Diabetic |
| 1 | Pre-Diabetic |
| 2 | Diabetic |

---



## Workflow

The complete workflow consists of the following stages:

```
Dataset
      │
      ▼
Data Cleaning
      │
      ▼
Missing Value Imputation
      │
      ▼
Label Encoding
      │
      ▼
Feature Scaling
      │
      ▼
Train-Test Split
      │
      ▼
Class Balancing
(SMOTE / ADASYN)
      │
      ▼
Model Training
      │
      ▼
Performance Evaluation
      │
      ▼
Visualization
```

---

## Machine Learning Models

The following classifiers are implemented:

- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting
- K-Nearest Neighbors
- XGBoost
- Support Vector Classifier
- Multi-Layer Perceptron

Additionally,

### Stacking Ensemble

Base Learners

- Random Forest
- Gradient Boosting
- XGBoost

Meta Learner

- Logistic Regression

---

## Data Preprocessing

The preprocessing pipeline includes:

- Removing unnecessary identifiers
- Cleaning column names
- Encoding categorical variables
- Handling missing values using mean imputation
- Feature normalization using StandardScaler
- Label encoding

---

## Handling Class Imbalance

Two oversampling methods are evaluated.

### SMOTE

Synthetic Minority Oversampling Technique generates synthetic samples for minority classes using nearest neighbors.

### ADASYN

Adaptive Synthetic Sampling generates additional samples for difficult minority instances, improving decision boundaries.

---

## Performance Metrics

The following evaluation metrics are used:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC

Additional visualizations include:

- Confusion Matrix
- Radar Plot
- Bar Charts
- Feature Importance

---

## Installation

Clone the repository

```bash
git clone https://github.com/username/diabetes-multiclass-classification.git
```

Navigate to the project

```bash
cd diabetes-multiclass-classification
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

## Required Libraries

```text
numpy
pandas
matplotlib
scikit-learn
imbalanced-learn
xgboost
scipy
joblib
```

Install all dependencies:

```bash
pip install -r requirements.txt
```

---

## Running the Project

Train all models

```bash
python main.py
```

or

```bash
python train.py
```

Evaluate models

```bash
python evaluate.py
```

Generate radar plots

```bash
python visualization.py
```

---

## Results

The paper reports the following observations:

- Random Forest achieved the best baseline performance.
- SMOTE consistently improved recall and F1-score.
- ADASYN significantly enhanced minority-class detection.
- The stacking ensemble achieved the highest performance on the 1000-sample dataset.
- Oversampling improved robustness across multiple classifiers.

---

## Future Improvements

Possible extensions include:

- Hyperparameter optimization
- Explainable AI (SHAP/LIME)
- Deep learning models
- Cross-validation
- Feature selection
- Automated Machine Learning (AutoML)
- Clinical deployment using Flask or Streamlit

---

## Citation

If you use this repository in your research, please cite the original paper:

Imbalance-Aware ML for Multiclass Classification of Diabetes Data,
IEEE, 2026.

---

## License

This project is intended for academic and research purposes.

---

