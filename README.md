# 🏠 Predictive Analysis of Housing Prices (India)

This project focuses on **predicting house prices across major Indian metropolitan cities** using **machine learning**.  
It integrates **multi-source real estate datasets**, performs **extensive data preprocessing & exploratory data analysis (EDA)**, and evaluates **multiple regression models** to identify the best-performing predictor.

---

## 📌 Project Overview

- **Problem**: Real estate prices depend on multiple interacting factors (area, location, amenities, resale status, city, etc.), making accurate prediction challenging using traditional methods.
- **Solution**: A **data-driven ML pipeline** that cleans, merges, analyzes, and models housing data from multiple sources.
- **Final Model**: **Gradient Boosting Regressor**
- **Best Performance**:
  - **R²** ≈ 0.86  
  - **RMSE** ≈ ₹7.99 Million  

---

## 📂 Repository Structure

📁 House-Price-Prediction
│
├── BDA_final.ipynb
├── ml_on_final_csv.ipynb
├── FINAL.csv
├── README.md


---

## 📘 Notebook Explanation

### 1️⃣ `BDA_final.ipynb`  
**(Data Preprocessing & Exploratory Data Analysis)**

This notebook covers the **entire data preparation pipeline**, including:

- Loading **multiple real-estate datasets** from different Indian cities
- Merging city-wise and generic datasets into a unified dataset (~66K records)
- Data cleaning:
  - Removing duplicates
  - Handling missing values
  - Replacing invalid encoded values
  - Outlier removal
- Feature engineering:
  - Standardizing column names
  - Creating derived feature `rate_persqft = Price / Area`
- Exploratory Data Analysis (EDA):
  - Price distribution analysis
  - Area vs price relationship
  - Amenity impact on pricing
  - City-wise affordability analysis
  - Correlation heatmaps and visual insights

📌 **Output**: A clean and structured dataset saved as `FINAL.csv`

---

### 2️⃣ `ml_on_final_csv.ipynb`  
**(Machine Learning on Final Dataset)**

This notebook focuses on **modeling and prediction** using the processed data.

Steps included:
- Loading `FINAL.csv`
- Selecting key predictive features
- Encoding categorical variables
- Train–test split (80/20)
- Training and evaluating multiple ML models:
  - Random Forest
  - XGBoost
  - CatBoost
  - Gradient Boosting
  - LightGBM
  - Stacked Ensemble
- Model evaluation using:
  - RMSE
  - R² Score
  - MAPE
- Feature importance analysis
- Final model selection based on performance

📌 **Best Model**: Gradient Boosting Regressor

---

## 🧠 Key Features Used for Prediction

- Area (sq. ft.)
- Number of Bedrooms
- Location
- City
- Resale Status
- Rate per square foot (derived)
- Amenities (Lift, Power Backup, Parking, Gym, etc.)

---

## 🛠️ Tech Stack

- **Programming Language**: Python 3
- **Libraries**:
  - Pandas, NumPy
  - Matplotlib, Seaborn
  - Scikit-learn
  - XGBoost, CatBoost, LightGBM
- **Platform**: Google Colab / Jupyter Notebook

---

## 🚀 How to Run the Project

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/house-price-prediction.git
   
Open BDA_final.ipynb and run all cells to generate FINAL.csv

Open ml_on_final_csv.ipynb to train and evaluate models

Modify features or models to experiment further 

## 📊 Results Summary

| Model                 | R² Score  | RMSE       |
| --------------------- | --------- | ---------- |
| Random Forest         | ~0.84     | ₹8.39M     |
| XGBoost               | ~0.78     | ₹10.01M    |
| CatBoost              | ~0.79     | ₹9.67M     |
| **Gradient Boosting** | **~0.86** | **₹7.99M** |
| LightGBM              | ~0.78     | ₹9.80M     |
| Stacked Ensemble      | ~0.85     | ₹8.21M     |

