# 🛍️ E-Commerce Spending Prediction Model

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge)
![Seaborn](https://img.shields.io/badge/Seaborn-3776AB?style=for-the-badge)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Linear Regression](https://img.shields.io/badge/Linear%20Regression-4CAF50?style=for-the-badge)

A Multiple Linear Regression model built in Python to predict annual customer spending for a clothing retailer - enabling data-driven decisions on digital platform investment between a mobile application and a desktop website.
---

## 📋 Table of Contents

- [Business Overview](#-business-overview)
- [Problem Statement](#-problem-statement)
- [Dataset](#-dataset)
- [Solution & Approach](#-solution--approach)
- [Model Performance](#-model-performance)
- [Key Insights](#-key-insights)
- [Technologies Used](#-technologies-used)
- [Getting Started](#-getting-started)
- [Project Structure](#-project-structure)
- [Author](#-author)

---

## 🏢 Business Overview

A clothing retail company offers in-person styling appointments where clients are guided by personal stylists. Following these sessions, customers can browse and purchase items through one of two digital channels - a **mobile application** or a **desktop website**.

The business is at a strategic crossroads: with limited development resources, they need to determine which platform drives greater customer value in order to allocate their digital investment effectively. This project delivers a quantitative answer to that question.

---

## 🎯 Problem Statement

> *Which digital platform - the mobile app or the website - has a greater influence on how much a customer spends annually, and how accurately can we predict that spending?*

The core objective is to **predict the Yearly Amount Spent** by each customer using behavioural engagement metrics. The resulting model provides both a predictive capability and an interpretable set of coefficients that directly inform the business's platform strategy.

---

## 📊 Dataset

The dataset contains customer-level behavioural and transactional data for the clothing retailer, including the following features:

| Feature | Description |
|---|---|
| `Avg. Session Length` | Average duration of in-store styling sessions (minutes) |
| `Time on App` | Average time spent on the mobile application (minutes/month) |
| `Time on Website` | Average time spent on the desktop website (minutes/month) |
| `Length of Membership` | Number of years the customer has been a member |
| `Yearly Amount Spent` | **Target variable** - total annual spend in USD |

---

## 🔬 Solution & Approach

### 1. Exploratory Data Analysis (EDA)
Visualised the relationships between all numerical variables using pairplots and a correlation heatmap to identify which engagement metrics exhibit the strongest linear relationships with annual spending. This step surfaced early evidence that membership duration and app usage were the most predictive features.

### 2. Data Preprocessing
Split the dataset into training and testing sets using a **70/30 ratio** to ensure unbiased model evaluation and reduce the risk of overfitting. Feature and target arrays were isolated prior to model fitting.

### 3. Model Training
Fitted a **Multiple Linear Regression** model using scikit-learn's `LinearRegression` estimator on the training set. The model learns the weighted contribution of each engagement metric to annual spending.

### 4. Model Evaluation
Assessed predictive accuracy and model reliability using three complementary evaluation methods:

- **Mean Absolute Error (MAE)** - average magnitude of prediction errors in USD
- **Mean Squared Error (MSE)** - penalises larger errors more heavily
- **Residual Analysis** - confirmed that residuals are approximately normally distributed, validating the core assumptions of linear regression and ensuring predictions are statistically sound

---

## 📈 Model Performance

| Metric | Value |
|---|---|
| Mean Absolute Error (MAE) | *see notebook* |
| Mean Squared Error (MSE) | *see notebook* |
| Root Mean Squared Error (RMSE) | *see notebook* |
| Residual distribution | Approximately normal - model assumptions satisfied |

> Full evaluation results and visualisations are available in the project notebook.

---

## 💡 Key Insights

Interpreting the model's regression coefficients revealed the following ranked drivers of annual customer revenue:

| Rank | Feature | Business Implication |
|---|---|---|
| 1 | **Length of Membership** | The strongest predictor of spend - long-term retention is the highest-value lever |
| 2 | **Time on App** | Mobile engagement has a significantly positive impact on annual spending |
| 3 | **Avg. Session Length** | In-store styling sessions contribute meaningfully to overall spend |
| 4 | **Time on Website** | Notably lower impact - the website is underperforming relative to the mobile app |

### Strategic Recommendation

The analysis provides clear, quantitative evidence to guide platform investment:

- **Prioritise mobile app development** - Time on App is the second-strongest revenue driver. Improving the mobile experience delivers a measurable uplift in annual customer spend.
- **Investigate the website** - The low coefficient for Time on Website presents a strategic choice: either invest in improving website performance to match the app, or deliberately shift resources toward the mobile channel.
- **Invest in retention programmes** - Length of Membership is the single strongest predictor of revenue. Customer loyalty initiatives and membership incentives have the highest potential ROI.

This analysis transitions the business from intuition-based decision-making to a strategy backed by quantitative evidence.

---

## 🔧 Technologies Used

| Technology | Purpose |
|---|---|
| [Python 3.11](https://www.python.org/) | Core programming language |
| [Pandas](https://pandas.pydata.org/) | Data loading, manipulation, and feature engineering |
| [NumPy](https://numpy.org/) | Numerical computation and array operations |
| [Matplotlib](https://matplotlib.org/) | Statistical plotting and visualisation |
| [Seaborn](https://seaborn.pydata.org/) | Correlation heatmaps and pairplot analysis |
| [scikit-learn](https://scikit-learn.org/) | Model training, train/test split, and evaluation metrics |

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Tusneld/e-commerce_customer_regression.git
cd e-commerce_customer_regression
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the notebook

```bash
jupyter notebook e-commerce_customer_regression.ipynb
```

---

## 📁 Project Structure

```
e-commerce_customer_regression/
│
├── data/
│   └── ecommerce_customers.csv       # Customer behavioural dataset
│
├── notebooks/
│   └── e-commerce_customer_regression.ipynb  # End-to-end analysis notebook
│
├── images/
│   ├── pairplot.png                  # EDA correlation pairplot
│   ├── heatmap.png                   # Feature correlation heatmap
│   └── residuals.png                 # Residual distribution plot
│
├── requirements.txt                  # Python dependencies
└── README.md
```

---

## 👤 Author

**Tusnelde Endjala**
Data Engineer · Data Analyst · Machine Learning Engineer · Software Engineer · Windhoek, Namibia

[![Portfolio](https://img.shields.io/badge/Portfolio-tusnelde.vercel.app-black?style=flat&logo=vercel)](https://tusnelde.vercel.app)
[![GitHub](https://img.shields.io/badge/GitHub-Tusneld-181717?style=flat&logo=github)](https://github.com/Tusneld)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
