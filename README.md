=======
Toyota Used Car Price Prediction
📌 Project Overview
This project analyzes a dataset of Toyota used vehicles to identify the key factors that influence vehicle prices and to build machine learning models that accurately predict car prices.
The analysis progresses from exploratory data analysis and correlation analysis to predictive modeling using both Linear Regression and Random Forest Regression.
❓ Research Question
What are the top factors that influence the price of used Toyota vehicles, and how accurately can machine learning models predict vehicle prices?
📁 Project Structure
toyota-price-analysis/
├── data/
│   └── toyota.csv
├── notebooks/
│   └── analysis.ipynb
├── models/
│   └── random_forest_price_model.joblib
├── README.md
└── .gitignore
📊 Dataset Description
Rows: 6,738
Target Variable: price
Features:
year
mileage
engineSize
tax
mpg
model (not used in final model)
fuelType
transmission
🔍 Exploratory Data Analysis
Correlation analysis revealed that the strongest numeric predictors of price were:
Engine Size (strong positive correlation)
Vehicle Year
Mileage (negative correlation)
These findings guided feature selection for modeling.
🤖 Modeling Approach
1️⃣ Linear Regression (Baseline)
A linear regression model was trained using the following features:
year
mileage
engineSize
tax
mpg
Performance:
R²: 0.7659
MAE: $2,254
RMSE: $3,156
This model performed reasonably well but showed limitations in capturing non-linear relationships.
2️⃣ Random Forest Regression (Final Model)
A Random Forest Regressor was trained using the same features to capture non-linear relationships and feature interactions.
Performance:
R²: 0.9557
MAE: $885
RMSE: $1,373
The Random Forest model significantly outperformed linear regression, reducing prediction error by over 60%.
📈 Model Comparison Summary
Model	R²	MAE	RMSE
Linear Regression	0.7659	$2,254	$3,156
Random Forest	0.9557	$885	$1,373
🧠 Key Insights
Vehicle pricing relationships are non-linear
Feature interactions (e.g., year × engine size) strongly influence price
Tree-based models outperform linear models for this problem
💾 Model Persistence
The final Random Forest model was saved using joblib and can be reloaded for future predictions.
import joblib
model = joblib.load("models/random_forest_price_model.joblib")
▶️ How to Run This Project
Clone the repository
Open the notebook in notebooks/
Run all cells to reproduce the analysis and model training
🚀 Future Improvements
Encode categorical variables (model, fuelType, transmission)
Perform hyperparameter tuning (GridSearchCV)
Add cross-validation
Deploy model as an API
📬 Author
Raghe Mahamud
GitHub: https://github.com/raghem
✅ Status
Complete
>>>>>>> c8194bf (Rewrite README with full project summary)
