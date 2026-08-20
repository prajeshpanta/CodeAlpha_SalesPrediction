# Sales Prediction using Python

A machine learning project that predicts product sales based on advertising spend across TV, Radio, and Newspaper channels. Built as part of the **CodeAlpha Data Science Internship**.

## Overview

This project uses the classic Advertising dataset to demonstrate a complete regression pipeline: data loading, exploratory data analysis, visualization, model training, and evaluation. A **Linear Regression** model is trained to predict sales from advertising spend across three platforms.

## Dataset

- **Source:** [Advertising Sales Dataset — Kaggle](https://www.kaggle.com/datasets/yasserh/advertising-sales-dataset)
- **Size:** 200 samples
- **Features:**
  - TV (advertising budget, in thousands $)
  - Radio (advertising budget, in thousands $)
  - Newspaper (advertising budget, in thousands $)
- **Target:** Sales (in thousands of units)

## Tech Stack

- Python 3.12
- pandas
- scikit-learn
- matplotlib
- seaborn
- Jupyter Notebook

## Project Workflow

1. **Data Loading & Exploration** — Loaded the dataset, dropped the unused index column, and confirmed no missing values.
2. **Data Visualization** — Used a seaborn pairplot to explore relationships between each advertising channel and sales.
3. **Train-Test Split** — Split the data into training and testing sets to evaluate performance on unseen data.
4. **Model Training** — Trained a Linear Regression model on the training set.
5. **Model Evaluation** — Assessed performance using MAE, MSE, RMSE, and R² score, and visualized predicted vs. actual sales.
6. **Feature Importance** — Examined the model's learned coefficients to identify which advertising channel drives sales the most.

## Results

The trained model achieved:

- **R² Score:** 0.88
- **Mean Absolute Error (MAE):** 1.31
- **Root Mean Squared Error (RMSE):** 1.78

**Key insights:** TV advertising showed the clearest, strongest relationship with sales in the data. However, based on the model's coefficients, Radio spend was actually more cost-efficient per dollar than TV, while Newspaper advertising had almost no measurable impact on sales — suggesting budget could be better allocated toward TV and Radio.

## How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/prajeshpanta/CodeAlpha_SalesPrediction.git
   cd CodeAlpha_SalesPrediction
   ```
2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   venv\Scripts\activate      # Windows
   source venv/bin/activate   # Mac/Linux
   ```
3. Install dependencies:
   ```bash
   pip install scikit-learn pandas matplotlib seaborn jupyter
   ```
4. Open `sales_prediction.ipynb` in VS Code or Jupyter and run all cells.

## 📁 Project Structure

```
CodeAlpha_SalesPrediction/
│
├── Advertising.csv            # Dataset
├── sales_prediction.ipynb     # Main notebook with full analysis
├── README.md                  # Project documentation
└── .gitignore                 # Excludes venv/ from version control
```

## About

This project was completed as **Task 4** of the **Data Science Internship at CodeAlpha**.

**Author:** Prajesh Panta
**Internship:** CodeAlpha Data Science