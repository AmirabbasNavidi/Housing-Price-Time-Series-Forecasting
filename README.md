# Housing Price Time Series Forecasting

## Overview

This project explores housing sales data and develops machine learning models to analyze monthly housing price trends and forecast future prices.

The project focuses on exploratory data analysis, feature engineering, time series forecasting, and model evaluation using Linear Regression and a naive baseline model.

## Objectives

* Analyze historical housing sales data.
* Explore trends and seasonality in monthly average prices.
* Engineer time-based and lagged features.
* Compare different seasonal encoding techniques.
* Build a baseline model and compare its performance with Linear Regression models.
* Forecast next-month housing prices.
* Evaluate models using MAE, RMSE, and R².

## Dataset

The project uses `raw_sales.csv`, containing historical housing sales data.

Main columns used:

* `datesold`: Date of the property sale.
* `price`: Property sale price.
* `bedrooms`: Number of bedrooms.
* `propertyType`: Type of property, such as house or unit.

The dataset is aggregated into monthly observations to analyze changes in average housing prices over time.

**Note:** Add the original dataset source and license before publishing the dataset or redistributing it.

## Project Workflow

### 1. Data Loading and Preparation

* Load the dataset using pandas.
* Inspect data types and dataset structure.
* Convert sale dates to datetime format.
* Sort observations chronologically.
* Aggregate sales data into monthly averages.

### 2. Exploratory Data Analysis

* Visualize monthly average housing prices.
* Investigate price trends over time.
* Compare monthly price patterns across different years.
* Analyze seasonal patterns in housing prices.
* Calculate monthly proportions of property types.

### 3. Feature Engineering

The following features and transformations are explored:

* **Time Index:** Represents the overall time trend.
* **Dummy Encoding:** Represents months using binary indicator variables.
* **Cyclic Encoding:** Uses sine and cosine transformations to represent yearly seasonality.
* **Lag Features:** Uses previous monthly prices, including one-month and twelve-month lags.
* **Property-Type Ratios:** Represents the monthly proportion of different property types.

### 4. Model Development

The following approaches are evaluated:

1. Naive Baseline Forecast
2. Linear Regression with Trend
3. Linear Regression with Trend and Seasonal Dummy Variables
4. Linear Regression with Trend and Cyclic Seasonal Features
5. Linear Regression with Lag Features and Additional Predictors

A separate next-month forecasting experiment is also performed by shifting the target price one month into the future.

### 5. Model Evaluation

Models are evaluated using the following metrics:

* **MAE (Mean Absolute Error):** Measures the average absolute difference between actual and predicted prices. Lower values indicate better performance.
* **RMSE (Root Mean Squared Error):** Penalizes larger prediction errors more heavily. Lower values indicate better performance.
* **R² (Coefficient of Determination):** Measures performance relative to a mean-target reference. Higher values are generally better, and negative values indicate poor predictive performance relative to that reference.

Models intended to predict the same target should be compared on the same test period.

## Technologies and Libraries

* Python
* NumPy
* pandas
* Matplotlib
* scikit-learn
* Jupyter Notebook

## Installation

Clone the repository:

```bash
git clone https://github.com/AmirabbasNavidi/Housing-Price-Time-Series-Forecasting.git
cd Housing-Price-Time-Series-Forecasting
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

Open the notebook using Jupyter:

```bash
jupyter notebook
```

Ensure that `raw_sales.csv` is available at the path expected by the notebook.

## Results

The project compares several feature engineering strategies and forecasting approaches.

Add the final model comparison table and evaluation period here after running the notebook. Report next-month forecasting results separately from models that estimate the price of the current month.

## Future Improvements

* Apply time series cross-validation.
* Perform residual analysis.
* Compare Linear Regression with tree-based regression models.
* Improve forecasting performance through additional features.
* Refactor repeated modeling code into reusable functions.
* Improve reproducibility and document final experimental results.

## Author

**Amirabbas Navidi**

GitHub: [AmirabbasNavidi](https://github.com/AmirabbasNavidi)
