# Toyota Used Car Price Prediction

## Project Overview
This project analyzes a dataset of used Toyota vehicles to identify the key factors that influence vehicle prices and to build machine learning models that accurately predict car prices.

The workflow progresses from exploratory data analysis and correlation analysis to predictive modeling using Linear Regression and Random Forest Regression.

---

## Research Question
**What factors most strongly influence the price of used Toyota vehicles, and how accurately can machine learning models predict vehicle prices?**

---

## Dataset Description
- **Observations:** 6,738 vehicles  
- **Target variable:** `price`  
- **Numeric features used:**
  - `year`
  - `mileage`
  - `engineSize`
  - `tax`
  - `mpg`

Additional categorical variables (`model`, `fuelType`, `transmission`) were explored but not included in the final model.

---

## Exploratory Data Analysis
Correlation analysis identified the strongest predictors of price:

1. **Engine size** – strong positive correlation  
2. **Vehicle year** – newer vehicles tend to be more expensive  
3. **Mileage** – negative correlation with price  

These findings guided feature selection for modeling.

---

## Modeling Approach

### Linear Regression (Baseline Model)
A linear regression model was trained using the following features:
- `year`
- `mileage`
- `engineSize`
- `tax`
- `mpg`

**Performance:**
- **R²:** 0.7659  
- **MAE:** $2,254  
- **RMSE:** $3,156  

The linear model provided a strong baseline but showed limitations in capturing non-linear relationships.

---

### Random Forest Regression (Final Model)
A Random Forest Regressor was trained using the same features to capture non-linear effects and feature interactions.

**Performance:**
- **R²:** 0.9557  
- **MAE:** $885  
- **RMSE:** $1,373  

The Random Forest model significantly outperformed linear regression, reducing prediction error by more than 60%.

---

## Model Comparison

| Model | R² | MAE | RMSE |
|------|----|-----|------|
| Linear Regression | 0.7659 | $2,254 | $3,156 |
| Random Forest | **0.9557** | **$885** | **$1,373** |

---

## Key Insights
- Used vehicle pricing relationships are highly **non-linear**
- Feature interactions (e.g., year × engine size) strongly influence price
- Tree-based ensemble models outperform linear models for this problem

---
## Future Improvements
- Encode categorical variables (model, fuelType, transmission)
- Perform hyperparameter tuning (GridSearchCV)
- Add cross-validation
- Deploy the model as an API

---
## Author
- Raghe Mahamud
- GitHub: https://github.com/raghem

---
## Status
- Complete
