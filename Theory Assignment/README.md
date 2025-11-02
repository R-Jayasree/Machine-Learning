# Machine Learning Assignment – Regression & Classification

This repository contains the complete implementation, datasets, and LaTeX report for a Machine Learning assignment focusing on **Linear Regression** and **Linear Classification** techniques.

---

## Directory Structure

```

project/
├── datasets/
│   ├── Cellphone.csv                  # Dataset for Regression task
│   └── BankNote_Authentication.csv    # Dataset for Classification task
│
├── screenshots/
│   ├── regression_plots.png           # Visualizations for regression
│   ├── classification_plots.png       # Visualizations for classification
│   └── ...                            # Additional plots used in the report
│
├── code.ipynb                         # Complete implementation notebook
├── report.pdf                         # Final compiled report
├── report_latex.tex                   # LaTeX source for the report
└── question.pdf                       # Assignment question document

```

## Assignment Overview

The assignment focuses on implementing and comparing **supervised learning algorithms** for two core ML tasks:

1. **Regression (Mobile Phone Price Prediction)**  
   Evaluate Linear Regression using matrix formulation, Gradient Descent, and Ridge Regularization.

2. **Classification (Bank Note Authentication)**  
   Build linear and neural classification models to detect fake banknotes, analyze regularization effects, and test robustness to outliers.

## Objectives

- Implement Linear Regression using **closed-form** and **gradient descent** approaches.  
- Apply **L2 (Ridge) regularization** and analyze the effect of the regularization parameter (λ).  
- Evaluate regression models using **MSE, RMSE, MAE, and R²** metrics.  
- Fit and compare **Logistic Regression** and **Multi-Layer Perceptron (MLP)** for binary classification.  
- Visualize **pairplots**, **heatmaps**, **accuracy vs. λ curves**, and **feature importance**.  
- Study the impact of **outliers** on model stability and performance.

## Libraries Used

- **numpy**, **pandas** – data handling and numerical computation  
- **matplotlib**, **seaborn** – visualizations and plots  
- **scikit-learn** – regression, classification, evaluation metrics  
- **scipy** – optimization and linear algebra  
- **warnings**, **os** – utility handling
  
## Techniques Used

### Regression
- **Linear Regression (Closed-form Solution)** using Normal Equation  
- **Gradient Descent Optimization** for parameter learning  
- **L2 Regularization (Ridge Regression)** for stability  
- **Feature Standardization** to observe scaling effects  
- **Error analysis and metric comparison**  

### Classification
- **Logistic Regression** (with and without L2 regularization)  
- **Multi-Layer Perceptron (1 hidden layer)** for non-linear separation  
- **Feature importance ranking** based on model coefficients  
- **Outlier injection** and model robustness evaluation  

## Results Summary

### **Regression Results**

| Method | Regularization (λ) | RMSE | R² | Remarks |
|--------|---------------------|------|----|----------|
| Closed-form | 0 | **151.86** | 0.959 | Best accuracy |
| Gradient Descent | 0 | 287,162 | -145,463 | Diverged due to learning instability |
| Ridge (Closed-form) | 10 | 161.09 | 0.954 | Regularized, stable |
| Ridge (Scaled) | 10 | 161.09 | 0.954 | Similar after scaling |

### **Classification Results**

| Model | Train Acc | Test Acc | Precision / Recall / F1 | Remarks |
|--------|------------|-----------|--------------------------|----------|
| Logistic (No Reg) | 0.991 | 0.985 | ≈ 0.98–0.99 | Excellent generalization |
| Logistic (L2, C=1.0) | 0.985 | 0.971 | ≈ 0.97 | Slight drop, more stable |
| MLP (1 Hidden Layer) | 1.000 | 1.000 | 1.000 | Perfect classification |
| Outlier-injected | 0.844 | 0.818 | ≈ 0.82 | Clear impact of noisy data |


### **Classification Reports (Clean vs. Outlier Model)**

| Metric | Clean Model (0.0) | Clean Model (1.0) | Outlier Model (0.0) | Outlier Model (1.0) |
|---------|-------------------|-------------------|----------------------|----------------------|
| Precision | 1.00 | 0.94 | 0.86 | 0.78 |
| Recall | 0.95 | 1.00 | 0.81 | 0.83 |
| F1-score | 0.97 | 0.97 | 0.83 | 0.80 |
| Support | 153 | 122 | 153 | 122 |
| **Accuracy** | **0.97** |  | **0.82** |  |

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/R-Jayasree/Machine-Learning.git
   cd TheoryAssignment
Open and run the notebook:

```jupyter notebook code.ipynb```

Change the paths of the datasets accordingly. 

## Learning Outcomes
* Gained hands-on experience in implementing linear models from scratch.
* Understood matrix-based formulations for regression and classification.
* Observed the role of regularization and feature scaling in model performance.
* Compared linear vs. non-linear models (Logistic vs. MLP).
* Analyzed model robustness under the presence of outliers.

