# E-commerce Spending Prediction Model

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge)
![Seaborn](https://img.shields.io/badge/Seaborn-3776AB?style=for-the-badge)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Linear Regression](https://img.shields.io/badge/Linear%20Regression-4CAF50?style=for-the-badge)

## Business Overview

I analyzed data for a clothing store that offers in-person styling appointments. After these sessions, clients can purchase items through either a mobile application or a desktop website. The business needs to determine which platform is driving more value to optimize their digital investments effectively.

## Problem Statement

The core objective of this project is to predict the **Yearly Amount Spent** by customers. By analyzing their behavior, I aim to provide data-driven insights to help the company decide whether to focus their budget and development efforts on improving the mobile application or the website.

## Solution & Approach

I developed a **Multiple Linear Regression** model to quantify the relationship between customer engagement metrics and their annual spending. My approach included:

- **Exploratory Data Analysis (EDA):** I visualized correlations between numerical variables to identify patterns in user behavior and engagement.
- **Data Preprocessing:** I split the dataset into training and testing sets using a 70/30 ratio to ensure unbiased model evaluation and prevent overfitting.
- **Model Training:** I utilized Scikit-Learn to fit the multiple linear regression model to the training data.
- **Evaluation:** I assessed the model's reliability using performance metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), and Residual Analysis to verify that my predictions were accurate and normally distributed.

## Tools & Tech Stack

- **Python** - Core programming language.
- **Pandas & NumPy** - For data manipulation and numerical analysis.
- **Matplotlib & Seaborn** - For statistical plotting and data visualization.
- **Scikit-Learn** - For machine learning model implementation.

## Dataset

The dataset used in this project is publicly available on Kaggle:
[Focusing on Mobile App or Website](https://www.kaggle.com/datasets/kolawale/focusing-on-mobile-app-or-website)

## Repository Structure

```
.
├── e-commerce_customer_linear_regression.ipynb   # Main analysis notebook
├── data/
│   └── ecommerce_customers.csv                   # Dataset (download from Kaggle)
├── README.md
└── requirements.txt
```

## Getting Started

### Prerequisites

- Python 3.8 or higher
- Jupyter Notebook or JupyterLab installed
- A Kaggle account (to download the dataset)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Tusneld/e-commerce_customer_linear_regression.git
   cd e-commerce_customer_linear_regression
   ```

2. **Create and activate a virtual environment** (recommended)
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```

3. **Install the required dependencies**
   ```bash
   pip install -r requirements.txt
   ```

   Or install the core packages directly:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn jupyter
   ```

4. **Download the dataset**
   - Visit the [Kaggle dataset page](https://www.kaggle.com/datasets/kolawale/focusing-on-mobile-app-or-website).
   - Download the CSV file and place it in a `data/` folder in the project root.

## How to Use the Notebook

1. **Launch Jupyter Notebook** from the project root directory:
   ```bash
   jupyter notebook
   ```

2. **Open the notebook** named `e-commerce_customer_linear_regression.ipynb` from the Jupyter interface.

3. **Update the file path** (if needed) in the data-loading cell so it points to where you saved the dataset, e.g.:
   ```python
   df = pd.read_csv("data/ecommerce.csv")
   ```

4. **Run the notebook cells in order**, from top to bottom, using `Shift + Enter` on each cell (or select **Run > Run All Cells** from the menu). The notebook is structured to follow the project workflow:
   - **Step 1 - Data Loading & Inspection:** Load the dataset and review its structure, data types, and summary statistics.
   - **Step 2 - Exploratory Data Analysis (EDA):** Generate pair plots, correlation heatmaps, and scatter plots to explore relationships between engagement metrics (e.g., Time on App, Time on Website, Length of Membership) and Yearly Amount Spent.
   - **Step 3 - Data Preprocessing:** Define feature variables (X) and the target variable (y), then split the data into training (70%) and testing (30%) sets.
   - **Step 4 - Model Training:** Fit a Multiple Linear Regression model to the training data using Scikit-Learn.
   - **Step 5 - Model Evaluation:** Generate predictions on the test set and evaluate performance using MAE, MSE, RMSE, and R² score. Residual plots are included to confirm the residuals are normally distributed.
   - **Step 6 - Coefficient Interpretation:** Review the model's coefficients to quantify the impact of each feature on Yearly Amount Spent, and visualize feature importance.

5. **Review the outputs** at each step - plots and printed metrics will render inline beneath each cell.

> **Tip:** If you only want to reproduce the final results without re-running the full EDA, scroll to the **Model Training** and **Evaluation** sections and run those cells directly, provided the data has already been loaded and preprocessed in earlier cells.

## Insights & Impact

By interpreting the model's coefficients, I successfully identified that **Length of Membership** is the most significant driver of annual revenue, followed by **Time on App**. Interestingly, the analysis revealed that **Time on Website** has a significantly lower impact compared to the mobile application. These findings allow the business to shift resources toward optimizing the mobile experience, which yields a higher return on investment - effectively transitioning the company from intuitive decision-making to a strategy backed by quantitative evidence.

## Contact

For questions or feedback regarding this project, feel free to reach out or open an issue in this repository.
