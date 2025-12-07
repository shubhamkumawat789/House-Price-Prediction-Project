# House-Price-Prediction-Project
This project builds a machine learning model to predict house prices using key property features such as lot size, basement area, construction year, building type, and zoning details. The workflow includes data cleaning, feature engineering, one-hot encoding, scaling, and training a RandomForestRegressor inside a scikit-learn Pipeline to avoid data leakage. Model performance is evaluated with 5-fold cross-validation, and feature importance is used to interpret key drivers of price.
A Streamlit app is deployed to allow users to enter house details and instantly receive an estimated selling price along with model insights.

#📊 Dataset Description
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
