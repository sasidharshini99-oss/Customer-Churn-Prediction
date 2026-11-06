# Customer Churn Prediction for the Telecom Industry

A machine learning project that predicts which telecom customers are likely to leave, so a business can act before they go. 

## Overview

Keeping an existing customer costs far less than winning a new one. This project analyses customer behaviour and account data, compares three classification models, and provides a simple desktop app for live predictions.

## Dataset

- **Source:** Kaggle customer churn dataset
- **Size:** 64,374 records, 12 columns
- **Features:** Age, Gender, Tenure, Usage Frequency, Support Calls, Payment Delay, Subscription Type, Contract Length, Total Spend, Last Interaction
- **Target:** `Churn` (1 = customer left, 0 = customer stayed)
- No missing values or duplicate rows were found.

## Workflow

1. **Data checks:** `info()`, `describe()`, missing values, duplicates
2. **Preprocessing:** label encoding of Gender, Subscription Type and Contract Length; dropping `CustomerID`; feature scaling with StandardScaler
3. **Exploratory analysis:** count plots, box plots, histograms and a correlation heatmap (Matplotlib, Seaborn, Plotly)
4. **Modelling:** Logistic Regression, Random Forest and SVM on an 80/20 train-test split
5. **Evaluation:** accuracy, confusion matrix, precision, recall and F1-score
6. **Prediction app:** a Tkinter GUI where a user enters customer details and gets a churn prediction

## Results

| Model | Accuracy |
|---|---|
| Random Forest | ~77% |
| **SVM** | **~83.4%** |

The SVM model had balanced precision and recall (about 0.82 to 0.85) for both churned and retained customers.

## Tech Stack

Python · Pandas · NumPy · Scikit-learn · Matplotlib · Seaborn · Plotly · Tkinter · Jupyter Notebook

## Project Structure

```
├── churn.ipynb           # Analysis, modelling and GUI code
├── customer_churn.csv    # Dataset
└── README.md
```

## How to Run

1. Clone the repository
   ```bash
   git clone https://github.com/<your-username>/<repo-name>.git
   cd <repo-name>
   ```
2. Install the dependencies
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn plotly
   ```
3. Make sure `customer_churn.csv` is in the same folder as the notebook.
4. Open the notebook and run all cells
   ```bash
   jupyter notebook churn.ipynb
   ```

Tkinter comes with Python. The prediction window opens when you run the last cells of the notebook.

## Future Improvements

- Deploy as a web app with Flask or Streamlit
- Try advanced models such as XGBoost and tune hyperparameters
- Add a dashboard for business users

## Author

Dharshini S
