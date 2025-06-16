# 🚗 Car Price Prediction Web App

This project is a **machine learning-based web application** built with Flask that predicts the selling price of a used car based on several features like the year of purchase, kilometers driven, fuel type, seller type, transmission, and ownership.

It uses a **Random Forest Regression Model** trained on historical car data and provides an interactive front-end for predictions.

---

## 📌 Features

- Web interface built using Flask
- Input fields for:
  - Year of purchase
  - Present price of the car
  - Kilometers driven
  - Ownership count
  - Fuel type (Petrol/Diesel)
  - Seller type (Dealer/Individual)
  - Transmission type (Manual/Automatic)
- Model trained using **Random Forest Regressor** with **RandomizedSearchCV** for hyperparameter tuning
- Visualizations using Matplotlib and Seaborn
- Model serialization using Pickle

---

## 🔧 Tech Stack

- Python
- Pandas, NumPy
- Scikit-learn
- Flask
- HTML/CSS (Jinja2 templating)
- Matplotlib, Seaborn
- Pickle

---

## 🚀 Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/devinenisrik/carpred.git
   cd carpred


2. **Create a virtual environment and activate it**

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   ```

3. **Install required packages**

   ```bash
   pip install -r requirements.txt
   ```

4. **Run the Flask application**

   ```bash
   python app.py
   ```

5. **Open your browser and navigate to**

   ```
   http://127.0.0.1:5000/
   ```

---

## 📊 Model Training Overview

* Dataset: `car data.csv`
* Preprocessing steps:

  * Removed irrelevant columns
  * Handled categorical variables using `pd.get_dummies()`
  * Engineered new features like `car_age`
  * Performed EDA (correlation heatmaps, feature importance)
* Model: `RandomForestRegressor` with hyperparameter tuning via `RandomizedSearchCV`
* Final model stored as `random_forest_regression_model.pkl`

---

## 🧪 Sample Prediction

After launching the app, input values like:

| Feature       | Value    |
| ------------- | -------- |
| Year          | 2015     |
| Present Price | 5.5 Lakh |
| Kms Driven    | 35000    |
| Owner         | 0        |
| Fuel Type     | Petrol   |
| Seller Type   | Dealer   |
| Transmission  | Manual   |

Click **Predict** and get the resale price prediction.

---

## 📁 File Structure

```
carpred/
│
├── app.py                         # Flask app
├── car data.csv                   # Dataset used for training
├── random_forest_regression_model.pkl  # Trained ML model
├── templates/
│   └── index.html                 # HTML template
├── static/                        # (Optional) CSS/JS/Images
└── README.md                      # Project README
```

---

## 📈 Model Evaluation Metrics

* **MAE**: Mean Absolute Error
* **MSE**: Mean Squared Error
* **RMSE**: Root Mean Squared Error

```text
MAE:    ~0.8
RMSE:   ~1.2
```

---

## 🧠 Future Improvements

* Add model explainability with SHAP or LIME
* Deploy to Heroku or Render
* Collect user feedback for continuous learning
* Enhance UI with Bootstrap or React

---
