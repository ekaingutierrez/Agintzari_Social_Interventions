# Agintzari Social Interventions: Predictive & Socioeconomic Analysis

## Project Overview
This repository contains a Machine Learning pipeline developed to analyze the demographic and economic evolution of the Uribarri district between 2014 and 2023. Instead of relying on static historical averages, I built a predictive system using regression models to forecast the exact volume of social interventions required for 2024, 2025, and 2026, providing a data-driven baseline for resource allocation.

## Tech Stack & Libraries
* Language: Python
* Data Processing: Pandas, NumPy
* Machine Learning & Modeling:
  * Scikit-learn (Simple Linear Regression, Multiple Linear Regression)
  * Scikit-learn Metrics (MSE, MAE, R2 Score)
* Visualization: Matplotlib

## Methodology & Technical Pipeline

### 1. Data Engineering & Preprocessing (01_eda_and_correlation_analysis_3.ipynb)
* Handled district datasets (datos.xlsx) by filtering and isolating the Uribarri data.
* Cleaned and structured demographic and income variables to build a correlation matrix, identifying the core mathematical drivers behind social interventions.

### 2. Feature Projections: Simple Linear Regression (02, 03, 04 notebooks)
To accurately forecast future interventions, the independent variables needed to be projected first. 
* I implemented Simple Linear Regression models to project Average Age, Foreign Population Percentage, and Net Average Income for the years 2024, 2025, and 2026.
* Evaluated the models using R-squared and Mean Absolute Error to ensure logical baseline projections.

### 3. Intervention Forecasting: Multiple Linear Regression (05_interventions_multiple_regression_3.ipynb)
* I implemented a Multiple Linear Regression model using the projected features as inputs.
* Validated the model against a test set (25% split), evaluating accuracy metrics and achieving a robust R-squared score (R2 = 0.60).
* Isolated 3 distinct projection years to generate final intervention volume predictions:
  * 2024: 125 estimated interventions.
  * 2025: 129 estimated interventions.
  * 2026: 132 estimated interventions.

## How to Run the Project

1. Clone the repository:
   ```bash
   git clone [https://github.com/](https://github.com/)[ekaingutierrez]/Agintzari_Social_Interventions.git
   ```

2. Install dependencies:
   ```bash
   pip install pandas numpy scikit-learn matplotlib openpyxl
   ```

3. Run the notebooks in sequential order starting from 01_eda_and_correlation_analysis_3.ipynb.
