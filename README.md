# MobiMart — Mobile Retail Demand Forecasting & Inventory Optimization

## Overview

MobiMart is a data-driven retail analytics project designed to forecast
mobile phone demand and optimize inventory allocation across multiple stores.

The project includes sales analysis, demand forecasting, inventory planning,
store-to-store transfers, and end-of-life markdown recommendations.

## Project Workflow

Historical Sales Data
        ↓
Exploratory Data Analysis
        ↓
Demand Forecasting
        ↓
Random Forest Model
        ↓
Inventory Requirement
        ↓
Excess / Shortage Detection
        ↓
Store-to-Store Transfers
        ↓
EOL / Markdown Recommendations

## Dataset

- 60 mobile phone models
- 25 stores
- Daily sales history
- Product segments
- Product prices
- Product launch dates
- Successor models
- 547,500 sales records

## Forecasting

A 7-day rolling average was used as the baseline forecasting method.

A Random Forest Regressor was trained using:

- Store
- Product model
- Product segment
- Price
- Day of week
- Month
- Week of year
- Day of month
- Recent 7-day demand

## Model Performance

| Model | MAE | RMSE |
|---|---:|---:|
| 7-Day Baseline | 1.1241 | 2.2963 |
| Random Forest | 0.6519 | 1.0151 |

Random Forest performed better than the baseline on the test period.

## Inventory Optimization

The forecasting output was used to calculate recommended inventory.

The system identifies:

- Inventory requirements
- Excess inventory
- Inventory shortages
- Store-to-store transfer opportunities
- EOL products requiring markdown

## Final Results

- Required Inventory: 664,979
- Current Inventory: 665,950
- Excess Inventory: 51,434
- Shortage Inventory: 50,463
- Transfer Quantity: 41,598
- Transfer Recommendations: 1,189
- EOL Markdown Inventory: 4,483
- Markdown Recommendations: 133

## Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Joblib
- Jupyter Notebook

## How to Run

Install the required libraries:

    pip install -r requirements.txt

Then open the Jupyter Notebook and run the cells sequentially.

Generated datasets and model outputs are stored in the data directory.

## Author

Rati Kumari Akela