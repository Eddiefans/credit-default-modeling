# Credit Card Default Prediction Model

![Machine Learning](https://img.shields.io/badge/-Machine%20Learning-blueviolet)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.0+-orange)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

A machine learning system to predict credit card payment defaults using logistic regression, SVM, and neural networks.

## Table of Contents
- [Project Overview](#project-overview)
- [Data Description](#data-description)
- [Methodology](#methodology)
- [Key Results](#key-results)
- [Getting Started](#getting-started)
  - [Installation](#installation)
  - [Usage](#usage)

## Project Overview

This project develops predictive models to identify customers at risk of credit card default using historical payment data. We implemented and compared three machine learning approaches to create an early warning system for financial institutions.

**Key Achievements:**
- Achieved 77.2% prediction accuracy (AUC) using neural networks
- Developed 18 engineered features capturing payment behaviors
- Created a reproducible model training pipeline

## Data Description

The dataset contains 30,000 anonymized credit card records from a Taiwanese bank (2005) with:

**Demographic Features:**
- Credit limit (LIMIT_BAL)
- Gender, education level, marital status
- Customer age

**Financial Behavior:**
- 6 months of payment history (PAY_0 to PAY_6)
- Bill statements (BILL_AMT1-6)
- Payment amounts (PAY_AMT1-6)

**Target Variable:**
- Binary default indicator (default.payment.next.month)

## Methodology

### Feature Engineering
- Created delinquency flags for late payments
- Calculated payment-to-bill ratios
- Developed credit utilization metrics
- Applied standardization and PCA (retaining 90% variance)

### Model Development
- **Logistic Regression**: Baseline model with L2 regularization
- **SVM**: RBF kernel for non-linear patterns
- **MLP Neural Network**: 2 hidden layers with ReLU activation

### Evaluation
- 5-fold cross-validation
- AUC-ROC as primary metric
- Class-weighted scoring to handle imbalance

## Key Results

**Model Performance Comparison:**

| Model                | AUC Score | Training Time |
|----------------------|-----------|---------------|
| Logistic Regression  | 0.752     | 2 min         |
| SVM (RBF Kernel)     | 0.600     | 15 min        |
| MLP Neural Network   | **0.772** | 8 min         |

**Key Findings:**
- MLP performed best at capturing complex patterns
- Payment history features were most predictive
- Model can identify 77% of true defaulters

## Getting Started

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/credit-card-default-prediction.git
cd credit-card-default-prediction