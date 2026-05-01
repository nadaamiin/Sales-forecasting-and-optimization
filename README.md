# 🛒 Walmart Sales Forecasting & Optimization

A machine learning project that predicts weekly sales across Walmart stores and departments using historical retail data. The project includes exploratory data analysis, multi-model comparison, and an interactive web app built with Gradio.

---

## 📌 Overview

Retail sales forecasting is critical for inventory management, staffing, and promotional planning. This project leverages Walmart's historical sales data (2010–2013) to build predictive models that estimate weekly sales based on temporal, economic, and promotional features.

The best-performing model — **Random Forest Regressor** — achieved an **R² score of 0.963**, explaining over 96% of the variance in weekly sales.

---

## 📊 Dataset

- **Source:** [Kaggle – Walmart Sales Forecast](https://www.kaggle.com/datasets/aslanahmedov/walmart-sales-forecast)
- **Period:** February 5, 2010 – July 26, 2013
- **Granularity:** Weekly records per store and department

### Features

| Feature | Description |
|---|---|
| `Store` | Store identifier |
| `Date` | Week of the record |
| `Temperature` | Weekly average temperature (°F) |
| `Fuel_Price` | Fuel price ($/gallon) |
| `MarkDown1–5` | Promotional markdown amounts |
| `CPI` | Consumer Price Index |
| `Unemployment` | Local unemployment rate |
| `IsHoliday` | Whether the week includes a public holiday |
| `Weekly_Sales` | Target variable — weekly revenue |

---

## 🧠 Models Trained

| Model | Notes |
|---|---|
| Linear Regression | Baseline model |
| Decision Tree Regressor | Captures non-linear patterns |
| **Random Forest Regressor** | **Best model — R² = 0.9634** |
| Support Vector Regressor (SVR) | Evaluated for comparison |

Hyperparameter tuning was performed using **GridSearchCV**.

---

## 🖥️ Interactive App (Gradio)

An interactive forecasting interface lets users upload a sales CSV, select a store and department, and instantly visualize the actual sales trend with the model's **Mean Absolute Error (MAE)**.

```bash
pip install gradio pandas numpy matplotlib scikit-learn
python app.py
```

**Inputs:** CSV file · Store number · Department number  
**Outputs:** Sales trend plot · MAE score

---

## 🚀 Getting Started

### Prerequisites

```bash
pip install pandas numpy matplotlib seaborn scikit-learn plotly gradio wordcloud
```

### Run the Notebook

1. Open `Sales_Forecasting_And_Optimization.ipynb` in Jupyter or Google Colab.
2. Upload `features.csv` (from the Kaggle dataset).
3. Run all cells to reproduce the EDA, model training, and evaluation.

### Run the App

```bash
python app.py
```

Then open the local URL printed in the terminal (e.g., `http://127.0.0.1:7860`).

---

## 📁 Project Structure

```
├── Sales_Forecasting_And_Optimization.ipynb   # Main notebook (EDA + modeling)
├── app.py                                      # Gradio web app
├── features.csv                                # Dataset (download from Kaggle)
└── README.md
```

---

## 📈 Results

- **R² Score:** 0.9634
- **MSE:** 21,696,414
- The Random Forest model significantly outperformed linear and tree-based baselines, capturing complex interactions between economic indicators, seasonality, and promotional activity.

---

## 🛠️ Technologies

`Python` · `Pandas` · `NumPy` · `Scikit-learn` · `Matplotlib` · `Seaborn` · `Plotly` · `Gradio` · `Google Colab`

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
