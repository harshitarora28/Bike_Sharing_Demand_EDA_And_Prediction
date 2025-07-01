# 🚲 Bike Sharing Demand Prediction

## 📌 Project Overview  
This project aims to predict the demand for bike rentals in urban cities to enhance mobility and ensure the timely availability of rental bikes. The dataset used is the Seoul Bike Sharing Demand dataset, which includes various features such as weather conditions, time, and seasons to forecast the number of bikes required at different hours of the day. The project implements multiple machine learning models to predict bike rental counts, with a focus on achieving high accuracy and interpretability.

---

## 🧭 Table of Contents  
- [Problem Statement](#problem-statement)  
- [Dataset](#dataset)  
- [Project Structure](#project-structure)  
- [Methodology](#methodology)  
- [Results](#results)  
- [Conclusion](#conclusion)  
- [Author](#author)

---

## 📌 Problem Statement  
The goal is to accurately predict the number of bikes required at each hour to meet fluctuating demand and maintain service efficiency. This helps minimize user waiting time and ensures a stable supply of rental bikes across different hours of the day, addressing a critical challenge for city planners and service providers.

---

## 📊 Dataset  
The dataset used is `SeoulBikeData.csv`, which contains hourly bike rental data along with features such as:

- Rented Bike Count (target variable)  
- Hour, Temperature, Humidity, Wind Speed, Visibility  
- Solar Radiation, Rainfall, Snowfall  
- Holiday, Functioning Day, Day, Month  
- Seasons (one-hot encoded as Autumn, Spring, Summer, Winter)

> ℹ️ Note: The dataset is loaded using `latin` encoding in the notebook.

---

## 🗂 Project Structure  
- 📓 `Bike_Sharing_Notebook_Harshit_Arora_2023277664(DS_AIML_Batch_1).ipynb`:  
  The main notebook containing the entire analysis, including data loading, EDA, data cleaning, feature engineering, model building, and evaluation.

- 📁 `SeoulBikeData.csv`:  
  The dataset used for analysis (not included in the repository; users must provide their own copy).

- 📄 `README.md`:  
  This file — providing an overview of the project.

---

## 🧪 Methodology

### 🔍 Exploratory Data Analysis (EDA)  
- Analyzed the distribution, correlation, and relationship of features with the target variable (`Rented Bike Count`)

### 🧹 Data Cleaning  
- Handled missing values  
- Removed multicollinear features  
- Performed one-hot encoding for categorical variables

### 🛠 Feature Engineering  
- Extracted relevant features like Day and Month  
- Encoded seasonal data using one-hot encoding

### 🤖 Model Building  
Implemented multiple regression models, including:

- Linear Regression, Ridge, Lasso, Elastic Net  
- K-Nearest Neighbors, Decision Tree, Random Forest, Extra Trees  
- Gradient Boosting, AdaBoost, XGBoost, LightGBM, SVR

### 🔧 Hyperparameter Tuning  
- Used `GridSearchCV` and `RandomizedSearchCV` to optimize model performance

### 📈 Model Evaluation  
- Evaluated models using metrics like RMSE, R², and Adjusted R²  
- Visualized results using bar plots for test R² and Adjusted R² scores

---

## ✅ Results

### 🏆 Final Model: LightGBM Regressor  
- 📈 Training R² Score: 99%  
- 📉 Test R² Score: 92.5%  
- 🥇 Lowest RMSE among all models

### 🔍 Key Findings  
- Bike rentals peak during commuting hours:  
  ⏰ 7–9 AM and 5–6 PM on working days  
- Rentals are higher during Spring and Summer  
- Moderate-to-high temperatures (32–36°C) and clear weather result in more rentals  
- Rentals drop with increasing humidity or during rain/snow

---

## 🧾 Conclusion  
The project successfully built a predictive model for bike rental demand using the LightGBM algorithm, which outperformed other models in terms of accuracy and interpretability.

### 💡 Recommendations  
- Add bike stations near workplaces and colleges  
- Allocate extra bikes during peak hours (7–9 AM, 5–6 PM)  
- Schedule maintenance at night to avoid disruption  
- Retrain the model regularly with updated data

---

## 👨‍💻 Author  
**Harshit Arora**  
B.Tech CSE Student, Sharda University
