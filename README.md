# 🚗 Car Price Prediction using Machine Learning  
*Created by Mostafa Saber*

## 📌 Overview

This project aims to predict the **selling price of used cars** using machine learning techniques. Accurate price prediction helps buyers and sellers make informed decisions in the second-hand car market.

The model was trained on a dataset containing car specifications such as brand, year, engine, mileage, power, and ownership type. It achieved **86% accuracy on training data** and **87% on testing data**, showing strong generalization.

---

## 📊 Dataset Description

The dataset contains detailed information about used cars listed for sale. Each entry includes specifications, location, and pricing details.

### 🔢 Numerical Features
- `Year`: Year of manufacture  
- `Kilometers_Driven`: Distance driven (in km)  
- `Mileage`: Fuel efficiency (km/l or km/kg)  
- `Engine`: Engine size (in CC)  
- `Power`: Power output (in bhp)  
- `Seats`: Number of seats  
- `New_Price`: Original price when new  
- `Price`: Target variable (selling price in lakhs)

### 🔠 Categorical Features
- `Name`: Car name (brand + model)  
- `Location`: City of listing  
- `Fuel_Type`: Petrol, Diesel, etc.  
- `Transmission`: Manual or Automatic  
- `Owner_Type`: First, Second, etc.

---

## ⚠️ Data Issues Handled

- Missing values in `Mileage`, `Power`, `Engine`, `Seats`, `New_Price`
- Text formatting in `Mileage`, `Engine`, and `Power` columns
- Outliers in `Kilometers_Driven`, `Power`, and `Price`
- High-cardinality in `Name` → simplified to extract brand
- Encoding of categorical variables
- Skewed target (`Price`) → log-transformed for better accuracy

---

## 📈 Exploratory Data Analysis (EDA)

- Distribution plots for `Price`, `Mileage`, `Power`
- Box plots for `Car Age` vs. `Price`
- Bar plots for average price by `Fuel_Type`, `Transmission`
- Correlation heatmap for numerical features

---

## 🛠 Feature Engineering

- Created `Car_Age = 2025 - Year`
- Converted units in `Mileage`, `Power`, `Engine`
- Scaled numerical columns using StandardScaler
- Encoded categorical features

---

## 🤖 Model Training

- **Models Used**:
  - Linear Regression
  - Polynomial Regression (Degree = 2)
  - Random Forest Regressor

### ✅ Best Model: Polynomial Regression
- **Training Accuracy**: 0.86
- **Testing Accuracy**: 0.87

---

## 📊 Evaluation Metrics

- R² Score
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)

---

## 🔮 Future Improvements

- Deploy the model as a Streamlit web app
- Integrate real-time car data scraping
- Try ensemble models like XGBoost or LightGBM
- Add price range classification as an optional output




