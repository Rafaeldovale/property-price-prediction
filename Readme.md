# Property Price Prediction (King County, Seattle)

This repository contains a Data Science project focused on predicting residential property prices in King County, USA. The main objective of this project is to practice and demonstrate advanced **Feature Engineering** techniques and their impact on machine learning model performance.

## Project Goal
To build a regression model that accurately estimates house prices based on structural features, while enriching the original dataset with calculated business rules such as geographical location advantages and property depreciation over time.

## Project Structure
    
property-price-prediction/
     |- dataset/
           |- kc_house_data.csv
     |- images/
     |- notebooks/
           |- housing_analysis.ipynb
     |- venv/
     |- README.md 

## Phase 1: Exploration & Feature Engineering (In Progress)
[x] Set up the local virtual environment and folder structure.

[x] Handle initial data ingestion and datetime conversions.

[x] Feature Engineering: Created house_age to measure property depreciation.

[x] Feature Engineering: Implemented the Haversine Formula to calculate dist_center (distance in km from each house to Seattle's city center).

[x] Feature Engineering: Created is_renovated to isolate the impact of modernizations on older structures.

[x] Data Visualization: Analyzed correlation and plotted price behavior against location and renovation status.

Next Steps
[ ] Investigate missing/null values and perform formal data cleaning.

[ ] Analyze target variable distribution (Price skewness).

[ ] Baseline model training (Linear Regression & Tree-based models).

Developed by Rafael Bezerra do Vale as part of a career transition portfolio