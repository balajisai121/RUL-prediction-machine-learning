# RUL-prediction-machine-learning
A machine learning project to predict the Remaining Useful Life (RUL) of machinery components. Uses advanced feature selection methods, including L1 regularization, and models like Random Forest and Linear Regression for robust predictions.

# Remaining Useful Life (RUL) Prediction

This repository contains a project aimed at predicting the Remaining Useful Life (RUL) of machinery components using machine learning. The project explores advanced feature selection techniques and models for reliable RUL predictions, contributing to predictive maintenance strategies.

## Project Overview
- **Objective**: Predict the Remaining Useful Life (RUL) of machinery components based on diagnostic data.
- **Key Metric**: RUL, calculated using torque margin and degradation rate.

## Dataset Description
- **Training Data**: 700,000 samples, 50 features
- **Test Data**: 300,000 samples
- **Key Features**:
  - `trq_measured`: Measured torque
  - `oat`: Outside air temperature
  - `mgt`: Mean gas temperature
  - `np`: Propeller speed
  - `ng`: Gas generator speed

## Methodology
- **Data Preprocessing**:
  - Outlier handling using IQR method
  - Standard scaling for feature normalization
- **Feature Selection Methods**:
  - SelectKBest (ANOVA)
  - Recursive Feature Elimination (RFE)
  - L1 Regularization (Lasso)
- **Models Used**:
  - Linear Regression
  - Random Forest Regressor

## Results and Insights
- Best feature selected: `Torque Margin`
- **Model Performance**:
  - Linear Regression: Perfect R² score (1.0) but overfitting observed
  - Random Forest Regressor: Robust performance with high accuracy

## Visualizations
- Degradation plot: Machine health over time
- Correlation heatmap of engine parameters
- Box plot of air temperature and torque

## Repository Structure
```plaintext
rul-prediction-machine-learning/
├── data/                 # Raw and processed datasets
│   ├── train.csv
│   ├── test.csv
│   └── submission.csv
├── notebooks/            # Jupyter notebooks for analysis
│   ├── preprocessing.ipynb
│   ├── feature_selection.ipynb
│   └── model_training.ipynb
├── visualizations/       # Plots and graphs
│   ├── degradation_plot.png
│   ├── correlation_heatmap.png
│   └── torque_vs_rul.png
├── results/              # Model outputs and evaluation metrics
│   ├── classification_report.txt
│   └── predictions.csv
├── README.md             # Project overview
├── LICENSE               # License file
└── requirements.txt      # Dependencies
