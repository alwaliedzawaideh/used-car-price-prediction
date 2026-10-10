# End-to-End Used Car Price Prediction & Data Pipeline

An end-to-end data science and engineering project built around data cleaning, automated validation suites, feature engineering, and baseline regression modeling using Python and Scikit-Learn.

## 📌 Project Overview
This project processes a large-scale automotive dataset (sourced from Kaggle's Playground Series) to predict used car prices. It covers the entire lifecycle of a data science workflow—from messy raw data ingestion and outlier capping to feature transformation and performance evaluation.

## 🛠️ Key Pipeline Stages
1. **Data Cleaning & Imputation:** Removed duplicate records, standardized categorical text formats (lowercase/whitespace trimming), and handled missing values using median/mode imputation.
2. **Quality Checks & Validation Suite:** Implemented automated assertion checks verifying zero remaining null values, correct data types, and valid value ranges.
3. **Outlier Management:** Applied the Interquartile Range (IQR) method (1.5x rule) to cap extreme values in continuous variables like mileage and price.
4. **Feature Engineering:** Extracted meaningful features such as `car_age`, standardized engine capacities, and computed mileage-per-year ratios.
5. **Data Transformations & Scaling:** Utilized Standard Scaler, Yeo-Johnson power transformations, and logarithmic target scaling (`np.log1p`) to normalize skewed distributions.
6. **Modeling & Error Analysis:** Trained an OLS Linear Regression baseline, evaluated performance via root mean squared error (RMSE), and generated residual error analysis plots.

## 📂 Repository Structure
```text
car-price-prediction-pipeline/
├── README.md               # Project documentation
├── requirements.txt        # Python dependencies
├── project_final.ipynb     # Cleaned Jupyter notebook containing the full pipeline
└── data_lineage_report.pdf # Detailed project report and data lineage documentation
```

## 🚀 Getting Started
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/car-price-prediction-pipeline.git
   cd car-price-prediction-pipeline
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Download the Kaggle dataset (`train.csv` and `test.csv`) into a folder named `data/` or update the file paths accordingly.
4. Open and run `project_final.ipynb` in Jupyter Notebook or VS Code.
