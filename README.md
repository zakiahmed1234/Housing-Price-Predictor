# Melbourne House Price Prediction

## Overview
This project predicts house prices in Melbourne, Australia using historical property data. The workflow includes data cleaning, feature engineering, preprocessing, modeling, and hyperparameter tuning. The goal is to showcase practical machine learning skills relevant for data science roles.

---

## Dataset
The dataset contains 13,580 property listings with 21 features, including:  
- **Suburb, Regionname, CouncilArea** – Location information  
- **Rooms, Bathroom, Car, Landsize, BuildingArea** – Property characteristics  
- **YearBuilt, Date, SellerG, Method** – Temporal and agent information  
- **Price** – Target variable  

The dataset is publicly available [here](https://www.kaggle.com/datasets/dansbecker/melbourne-housing-snapshot) (Melbourne Housing Snapshot).

---

## Key Features
- **Feature Engineering**:
  - `HouseAge` – Age of the property at sale time
  - `Building_to_Land_Ratio` – Relative property size
  - `TopAgent` – Top 20 real estate agents as a categorical feature
  - Temporal features: `YearSold`, `MonthSold`, `QuarterSold`, `SeasonSold`
- **Handling Missing Values**: Imputed numerical features with median and categorical features with most frequent values.  
- **Categorical Encoding**:  
  - High-cardinality columns (`Suburb`, `SellerG`) encoded with TargetEncoder  
  - Low-cardinality columns one-hot encoded  

---

## Modeling
- **Pipeline Approach**: Preprocessing and modeling combined using `sklearn.Pipeline` and `ColumnTransformer`  
- **Model**: `XGBRegressor` from XGBoost  
- **Hyperparameter Tuning**: `RandomizedSearchCV` to optimize learning rate, max depth, subsample ratio, and number of estimators  
- **Evaluation**: RMSE on test set

---

## How to Run
1. Clone the repository:  
  ```bash
  git clone https://github.com/zakiahmed1234/Housing-Price-Predictor.git
  cd Housing-Price-Predictor

```
2. Make sure you have python 3 installed, and then run:
  ```bash
   pip install -r requirements.txt
   ```
3. Open and run the Jupyter notebook:
   ```bash
   jupyter notebook Housing_Model.ipynb
   ```
