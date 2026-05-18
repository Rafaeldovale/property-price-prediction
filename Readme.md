# Property Price Prediction (King County, Seattle)

This repository contains a Data Science project focused on predicting residential property prices in King County, USA. The main objective of this project is to practice and demonstrate advanced **Feature Engineering** techniques and their impact on machine learning model performance.

## Project Goal
To build a regression model that accurately estimates house prices based on structural features, while enriching the original dataset with calculated business rules such as geographical location advantages and property depreciation over time.

## Project Structure
    
property-price-prediction/
      |- dataset/
           |- kc_house_data.csv
      |- images/
           |- price_by_renovation_status.png
           |- price_vs_age_scatter.png
           |- price_distribution_histogram.png
           |- price_outliers_boxplot.png
           |- price_distribution_by_bedrooms.png
           |- model_mae_comparison.png
      |- models/
           |- random_forest_house_model.pkl
      |- notebooks/
           |- housing_analysis.ipynb
      |- venv/
      |- README.md 

## 🛠️ Technologies & Libraries Used
This project was developed using **Python** inside a **Jupyter Notebook** environment. The following core libraries were installed and used:
* **Pandas & NumPy:** For data manipulation, handling datetime formats, and mathematical operations.
* **Matplotlib & Seaborn:** For exploratory data analysis (EDA) and plotting statistical charts.
* **Scikit-Learn:** For data splitting (`train_test_split`), metric evaluations (`MAE`, `R²`), and training Linear Regression and Random Forest models.
* **XGBoost:** For advanced, optimized gradient boosting regression.

---

## 🚀 How to Run this Project (Installation Guide)
To clone this repository and run the notebook locally, follow these steps in your terminal:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Rafaeldovale/property-price-prediction
   cd property-price-prediction

2. **Set up and activate the Virtual Environment (Venv)**

**Windows**
      python -m venv venv
      .\venv\Scripts\activate
**Linus/macOS**
      python3 -m venv venv
      source \venv\Scripts\activate

3. **Install all required dependencies**

      pip install pandas numpy matplotlib seaborn scikit-learn xgboost notebook

4. ** launch Jupyter:**

      jupyter notebook

## Phase 1: Exploration & Feature Engineering

[x] Set up the local virtual environment and folder structure.
[x] Handle initial data ingestion and datetime conversions.
[x] Feature Engineering: Created house_age to measure property depreciation.
[x] Feature Engineering: Implemented the Haversine Formula to calculate dist_center (distance in km from Seattle's city center).
[x] Feature Engineering: Created is_renovated to isolate the impact of modernizations.
[x] Data Visualization: Analyzed price distribution, identified market outliers via Boxplots, and exported all plots to the /images directory.

## Phase 2: Model Training & Evaluation (Benchmark)
In this phase, a comparative benchmark strategy was deployed to find the best machine learning algorithm. We tested three models, moving from 
a baseline linear approach to advanced tree-based ensemble methods.

Performance Results:
. Linear Regression (Baseline): * MAE: $120,230.17 | R² Score: 73.12%

      . Verdict: Too rigid to capture non-linear patterns of the real estate market.

. Random Forest Regressor: * MAE: $70,355.47 | R² Score: 88.79%

      . Verdict: Winner in average error reduction (MAE). The ensemble of 100 decision trees mapped property segments brilliantly.

. XGBoost Regressor (Optimized): * MAE: $73,932.27 | R² Score: 88.81%

      . Verdict: Highest explained variance (R²), but slightly more sensitive to extreme market luxury outliers than Random Forest.

[x] Split data into Training (80%) and Testing (20%) sets to avoid data leakage.
[x] Train and evaluate Linear Regression baseline.
[x] Implement Random Forest Regressor and slash the average error by $50k.
[x] Tune and optimize XGBoost Regressor hyperparameters to handle data types and avoid overfitting.