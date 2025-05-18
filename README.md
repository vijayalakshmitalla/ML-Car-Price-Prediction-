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

| Model                       | R² Score | RMSE  |
| --------------------------- | -------- | ----- |
| Linear Regression           | 0.65     | 18,250|
| Decision Tree Regressor     | 0.72     | 15,800|
| Random Forest Regressor     | 0.81     | 11,500 |
| Extra Trees Regressor       | 0.82     | 11,200 |
| Gradient Boosting Regressor| 0.84     | 10,400 |
| AdaBoost Regressor          | 0.80     | 12,000 |
| XGBoost Regressor           | 0.85     | 10,100 |

## Results

The notebook includes:
* Histograms and boxplots for numeric features
* Countplots for categorical feature distributions
* Correlation heatmap
* Bar charts comparing model performance
* importance plot for the selected best model

## Conclusion

This project presents a fully reproducible workflow for predicting used car prices, demonstrating how to transform raw listings into actionable, data-driven insights.  XGBoost and ExtraTrees Regressor  achieve the best performance and are suitable for further optimization and deployment.

## Acknowledgements

* Dataset taken from Kaggle
* Developed on Google Colab
* Inspired by open-source examples and automotive market analyses
