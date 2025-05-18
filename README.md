# Car Price Prediction Project

This project focuses on predicting car prices using machine learning techniques. It involves data exploration, preprocessing, model building, and evaluation to estimate car prices based on various features.

## Overview

The goal of this project is to develop a robust model that can accurately predict the price of a car given its attributes. This is valuable for both buyers and sellers, enabling price benchmarking, inventory valuation, and market analysis.

## Problem Statement

Estimating a fair selling price for a used car can be challenging due to the myriad factors affecting valuation. This project aims to automate price prediction by leveraging historical listing data and modern regression techniques.

## Project Objectives

* Load and clean raw car listing data
* Explore relationships between car attributes and price
* Engineer predictive features from raw variables
* Train and compare multiple regression algorithms
* Identify the best-performing model for deployment

## Dataset Description

The primary dataset (`train.csv`) comprises ~19,200 used car listings with these key attributes:

**Numeric Features**

* Price (target variable)
* Production year
* Mileage
* Levy
* Cylinders
* Airbags

**Categorical Features**

* Manufacturer & Model
* Category (e.g., SUV, sedan)
* Leather interior (yes/no)
* Fuel type
* Gear box type
* Drive wheels configuration
* Doors
* Wheel rim type
* Exterior color

## Data Preprocessing

* **Missing values:** Imputed or removed based on feature type.
* **Duplicates:** Identified and dropped.
* **Data types:** Converted dates and numeric strings to appropriate formats.
* **Outliers:** Detected via IQR method and handled for critical features (e.g., mileage, price).

## Exploratory Data Analysis

* Distribution plots for price, mileage, and production year
* Countplots for categorical features (manufacturer, category, fuel type)
* Correlation heatmap to uncover feature interdependencies

## Feature Engineering

* Date-based features: Extracted car age from production year.
* Binning: Grouped mileage into quartiles.
* Encoding:
    * Label encoding for ordinal categories (e.g., number of doors).
    * One-hot encoding for nominal variables (manufacturer, model, fuel type).
* Scaling: StandardScaler for algorithms sensitive to feature scale.

## Model Training & Evaluation

**Train-Test Split**

80/20 split.

**Algorithms Compared**

* Linear Regression
* Decision Tree Regressor
* Random Forest Regressor
* Extra Trees Regressor
* Gradient Boosting Regressor
* XGBoost Regressor
* KNN Regressor
* LightGBM Regressor

**Evaluation Metrics**

* R² Score
* Root Mean Squared Error (RMSE)
* Mean Absolute Error (MAE)

## Results

The notebook includes:
* Histograms and boxplots for numeric features
* Countplots for categorical feature distributions
* Correlation heatmap
* Bar charts comparing model performance
* importance plot for the selected best model

| Model                       | R² Score | RMSE  | MAE   |
| --------------------------- | -------- | ----- | ----- |
| Linear Regression           | 0.08     | 18,250|  N/A   |
| Decision Tree Regressor     | 0.41     | 15,800|  N/A   |
| Random Forest Regressor     | 0.51     | 11,500 |  N/A   |
| Extra Trees Regressor       | 0.62     | 11,200 |  N/A   |
| Gradient Boosting Regressor| 0.45     | 10,400 |  N/A   |
| XGBoost Regressor           | 0.55     | 10,100 |  N/A   |
| KNN Regressor           | 0.49     | N/A     | N/A  |
| LightGBM Regressor           | 0.56     | N/A     | N/A  |

## Conclusion

This project presents a fully reproducible workflow for predicting used car prices, demonstrating how to transform raw listings into actionable, data-driven insights.  XGBoost and ExtraTrees Regressor  achieve the best performance and are suitable for further optimization and deployment.

## Acknowledgements

* Dataset taken from Kaggle
* Developed on Google Colab
* Inspired by open-source examples and automotive market analyses
