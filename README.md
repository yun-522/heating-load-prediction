# Building Heating Load Prediction  

## Overview  
This project was developed as part of **QBUS2820 (Predictive Analytics)** at the University of Sydney.  
The task was to build and evaluate multiple **regression models** to predict the **heating energy demand of buildings** using both **structural features** (height, insulation, wall/floor area, glazing) and **environmental factors** (temperature, sunlight, orientation).  

The dataset (`HeatingLoad_training.csv`, `HeatingLoad_test_without_HL.csv`) was provided by the course instructor.  
Due to licensing restrictions, the full datasets are **not included in this repository**.  

To illustrate the structure, sample files (first 5 rows) are provided:  
- [Sample Training Dataset](./data/sample_training.csv)  
- [Sample Test Dataset](./data/sample_test.csv)  


---

## Objectives  
1. **Model Building**  
   - Develop baseline regression models (OLS).  
   - Extend with **Polynomial Regression** to capture nonlinearities.  
   - Apply **regularized regressions (Lasso & Ridge)** for feature selection and multicollinearity handling.  
   - Compare with **non-parametric KNN regression**.  

2. **Model Evaluation**  
   - Metrics: **Root Mean Squared Error (RMSE)**, **AIC**, **BIC**.  
   - Focus on trade-offs between accuracy and interpretability.  

3. **Reproducibility & Deliverables**  
   - End-to-end **Jupyter Notebook** (exported to HTML).  
   - Predictions for withheld test dataset.  
   - Clear documentation of model choices and results.  

---

## Tech Stack  
- **Language:** Python (Jupyter Notebook)  
- **Libraries:**  
  - `pandas` & `numpy` → data handling  
  - `matplotlib` → visualization  
  - `scikit-learn` → regression models (OLS, Polynomial, Ridge, Lasso, KNN)  
- **Evaluation Metrics:** RMSE, AIC, BIC  

---

## Repository Structure  


## Key Results  
- **OLS Regression:** Provided baseline interpretability, but higher RMSE.  
- **Polynomial Regression:** Best predictive performance with RMSE ≈ lowest among models; however, risk of overfitting noted.  
- **Lasso Regression:** Performed feature selection, simplifying the model.  
- **Ridge Regression:** Controlled multicollinearity and improved generalization.  
- **KNN Regression:** Non-linear flexibility but sensitive to hyperparameters.  
- **Final Takeaway:** **Polynomial Regression** achieved the lowest training RMSE, while **Ridge Regression** offered the best generalization balance.  

---

## Insights  
- Building heating load is strongly influenced by **floor area, insulation, and glazing type**.  
- **Polynomial models** captured interaction effects (e.g., between wall area and insulation) better than linear OLS.  
- **Regularization (Lasso/Ridge)** improved interpretability by reducing redundant predictors.  
- Demonstrates how regression can support **energy efficiency policies** and **building design optimization**.  
