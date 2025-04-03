# Credit Card Default Prediction Model

![Machine Learning](https://img.shields.io/badge/-Machine%20Learning-blueviolet)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.0+-orange)

A machine learning system to predict credit card payment defaults using logistic regression, SVM, and neural networks.

## Table of Contents
- [Project Overview](#project-overview)
- [Key Features](#key-features)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

This project develops predictive models to identify customers at risk of credit card default. We compare three machine learning approaches:

1. **Logistic Regression** (AUC: 0.752)
2. **Support Vector Machine with RBF Kernel** (AUC: 0.600)
3. **Multi-Layer Perceptron Neural Network** (AUC: 0.772 - Best Performance)

The MLP model achieved 77.2% accuracy in predicting defaults, providing financial institutions with actionable risk assessments.

## Key Features

- **Comprehensive Feature Engineering**:
  - Delinquency flags for payment history
  - Payment-to-bill ratios
  - Credit utilization metrics
  - Standardized feature scaling

- **Optimized Model Pipeline**:
  - Automated data preprocessing
  - PCA dimensionality reduction
  - Hyperparameter tuning via GridSearchCV
  - 5-fold cross-validation

- **Performance Evaluation**:
  - AUC-ROC as primary metric
  - Comparative model analysis
  - ROC curve visualization

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/credit-card-default-prediction.git
cd credit-card-default-prediction