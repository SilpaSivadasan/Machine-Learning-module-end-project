# Machine-Learning-module-end-project

# 🚗 Car Price Prediction using Machine Learning

This project aims to build and compare various regression models to predict car prices based on key automobile attributes. It was done as part of a market-entry analysis for a Chinese automobile company exploring the US car market.

---

## 📂 Dataset

- [📥 Car Price Dataset (Google Drive)](https://drive.google.com/file/d/1FHmYNLs9v0Enc-UExEMpitOFGsWvB2dP/view?usp=drive_link)

---

## 🎯 Objectives

- Understand key variables affecting car price
- Build regression models for prediction
- Compare model performance using R², MSE, and MAE
- Identify most important features
- Tune the best model for better performance

---

## 🧰 Tools & Libraries

- Python
- Jupyter Notebook
- Pandas, NumPy
- Seaborn, Matplotlib
- Scikit-learn

---

## 📊 Models Used

| Model                    | R² Score | MSE           | MAE       |
|--------------------------|----------|---------------|------------|
| Linear Regression        | ❌       | Very high     | Unusable   |
| Decision Tree Regressor | ✅       | Moderate      | Decent     |
| Random Forest Regressor | ✅✅ ✅   | **Best**      | **Best**   |
| Gradient Boosting        | ✅       | Good          | Good       |
| Support Vector Regressor | ❌       | Poor          | High error |

---

## ✅ Best Performing Model

- **Model:** Random Forest Regressor
- **R² Score:** ~0.953
- **MSE:** ~3.68M
- **MAE:** ~1367

---

## 🔍 Feature Importance

Top influential features:
- Engine size
- Horsepower
- Car width
- Drive wheels
- Curb weight

---

## 🧪 Hyperparameter Tuning

Tuned Random Forest using `GridSearchCV`:

```python
param_grid = {
    'n_estimators': [50, 100, 200],
    'max_depth': [None, 10, 20],
    'min_samples_split': [2, 5]
}
