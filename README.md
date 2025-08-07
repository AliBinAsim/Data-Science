# Housing Price Prediction with Random Forest

This is my **first machine learning project**, where I built a regression model to predict housing prices based on various features like square footage, number of bedrooms, year built, and neighborhood.

The model uses a **Random Forest Regressor** and is built using a complete **scikit-learn pipeline** with preprocessing steps for numerical and categorical data.

---

## 📌 Project Highlights

- ✅ **Data Pre-processing** with `StandardScaler` and `OneHotEncoder`
- 🧠 **Machine Learning** model using `RandomForestRegressor`
- 🔧 **Pipeline & ColumnTransformer** to handle both numeric and categorical columns
- 📊 **Evaluation** using Mean Squared Error (MSE) and custom accuracy percentages
- 🚨 **Outlier Detection** using IQR method (especially for `Price` column)

---

## 📁 Dataset Used

The dataset contains columns such as:

- `SquareFeet`
- `Bedrooms`
- `Bathrooms`
- `YearBuilt`
- `Neighborhood`
- `Price` (target)

We found and handled outliers, particularly in the `Price` column, where some values were negative or abnormally high.

---

## 📈 Evaluation Metrics

- Mean Squared Error (MSE)
- Percentage Accuracy (custom calculation per row)

---

## 🚀 How to Run

1. Clone this repo:

```bash
git clone https://github.com/yourusername/housing-price-prediction.git
```

2. Install requirements:

```bash
pip install -r requirements.txt
```

3. Open the Jupyter Notebook:

```bash
jupyter notebook housing_price_model.ipynb
```

---

## 📦 Model Description

The trained model is built using `RandomForestRegressor` within a pipeline that includes all preprocessing steps. It takes care of both numeric and categorical variables and can generalize well on unseen data.

The model can be used to make predictions by calling:

```python
predicted_price = model.predict(new_data)
```

This makes it easy to deploy or integrate into other applications. Model accuracy was evaluated with MSE and row-wise percentage accuracy.

---

## 📥 Example Usage

You can use the trained pipeline model to make predictions on new data like this:

```python
import pandas as pd

# Example new data (should match training feature format)
new_data = pd.DataFrame({
    "SquareFeet": [2200],
    "Bedrooms": [4],
    "Bathrooms": [2],
    "YearBuilt": [2015],
    "Neighborhood": ["Suburban"]
})

# Predict using the trained pipeline model
predicted_price = model.predict(new_data)

print("Predicted Price:", predicted_price[0])
```

> 🧠 Make sure the new data has the **same columns** as the original training set and uses a **DataFrame**, not a list or dict directly.

---

## 🧠 Skills Demonstrated

- pandas
- scikit-learn
- ML pipeline design
- Regression modeling
- Error analysis

---

## 📌 Note

This is my **first end-to-end ML project**, and it helped me practice handling real-world data, building a predictive model, and evaluating results. It also includes **outlier detection and correction** as part of the data cleaning process.

---

## ✅ To Do

-

