# House-Price-Prediction-Project
This project predicts house sale prices using Machine Learning.
It includes data preprocessing, feature engineering, model training, and a fully interactive Streamlit web app to make predictions.

# 📌 Project Overview

The goal is to build a model that can estimate the selling price of a house based on its features such as lot size, building type, basement area, age, and renovation history.
The final model is wrapped inside a scikit-learn pipeline, saved as house_price_pipe.pkl, and deployed through a Streamlit web app.

# 📊 Dataset Description
This project uses a structured housing dataset containing property characteristics, building quality indicators, and neighborhood information to predict home sale prices.

| **Feature**         | **Description**                                                                            |
| ------------------- | ------------------------------------------------------------------------------------------ |
| **MSSubClass**      | Identifies the type of dwelling (1Fam, duplex, townhome, etc.).                            |
| **MSZoning**        | Residential zoning classification — affects location quality & house value.                |
| **LotArea**         | Lot size in square feet. Larger lots generally indicate higher price.                      |
| **LotConfig**       | Layout of the property (Inside, Corner, CulDSac). Corner lots often have premium value.    |
| **BldgType**        | Type of building (Single-family, Duplex, Townhouse). Impacts pricing significantly.        |
| **OverallCond**     | Rates overall condition on a scale of 1–10. Higher condition indicates better maintenance. |
| **Exterior1st**     | Primary exterior covering on the house (Vinyl, Metal, Wood, etc.).                         |
| **YearBuilt**       | Original construction year of the house. Newer houses typically sell at higher prices.     |
| **YearRemodAdd**    | Year of major remodeling/additions. Recent renovations increase value.                     |
| **TotalBsmtSF**     | Total unfinished + finished basement area (sq ft).                                         |
| **BsmtFinSF2**      | Finished basement area (second category). Adds livable space.                              |
| **HouseAge**        | Age of the property = CurrentYear − YearBuilt.                                             |
| **YearsSinceRemod** | Time since last renovation = CurrentYear − YearRemodAdd.                                   |
| **TotalLivingArea** | Combined livable area = TotalBsmtSF + BsmtFinSF2.                                          |
| **BsmtFinRatio**    | Ratio of finished basement area to total basement area.                                    |
| **IsRemodeled**     | 1 if remodeled, 0 if original construction.                                                |
| **LotAreaCategory** | Lot size categorized into Small / Medium / Large / XL.                                     |
| **SalePrice**       | Final sale price of the house (continuous numeric value).                                  |

# 🧠 Feature Engineering

To improve model performance, several new features were created:

- HouseAge – current year minus year built
- YearsSinceRemod – years since last remodeling
- TotalLivingArea – total usable basement space
- BsmtFinRatio – percentage of basement that is finished
- IsRemodeled – 1 if renovated, otherwise 0
- LotAreaCategory – buckets: Small / Medium / Large / XL

These engineered features help the model capture patterns that raw features alone cannot.

# ⚙️ Model Training

The project uses a RandomForestRegressor inside a full preprocessing pipeline.
Key steps:
- One-hot encoding for categorical features
- Scaling for numerical features
- Train-test split
- 5-fold cross-validation
- Hyperparameter tuning using RandomizedSearchCV
- Final training on full dataset
  
The trained pipeline is saved as:
house_price_pipe.pkl

# 📈 Model Results

The model performs well with:
- Low MAPE (Mean Absolute Percentage Error)
- Strong R² score
- Meaningful feature importance rankings

# 📂 Project Structure
```
House-Price-Prediction-Project/
│
├── app/
│   └── app.py
│
├── models/
│   └── house_price_pipe.pkl
│
├── data/
│   ├── HousePricePrediction.xlsx
│   └── feature_importance.csv
│
├── notebooks/
│   └── House Price Prediction using Machine Learning.ipynb
│
├── docker/
│   └── Dockerfile
│
├── docs/
│   └── README.md
│
├── requirements.txt
├── LICENSE
└── .gitattributes

```

