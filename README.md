# Insurance Cost Prediction

A machine learning project comparing Linear Regression and a Multi-Layer Perceptron (MLP) for predicting individual medical insurance costs.

## Project Overview

The goal is to predict individual medical insurance charges based on customer characteristics, including age, sex, BMI, number of children, smoking status, and region.

## Dataset

The dataset contains 1,338 observations and 7 columns.

- **Target variable:** `charges` — individual medical insurance costs.
- **Features:** age, sex, BMI, number of children, smoking status, and region.

The dataset was obtained from Kaggle. Check the original dataset's licensing terms before redistributing the CSV file.

## Methods

- Exploratory Data Analysis (EDA)
- Numerical and categorical feature preprocessing
- `StandardScaler` for numerical features
- `OneHotEncoder` for categorical features
- Log transformation of the target variable using `log1p`
- `Pipeline` for preprocessing and model training
- Model comparison: `LinearRegression` and `MLPRegressor`
- 5-fold cross-validation
- Evaluation using RMSE, MAE, and R²

## Results

Test set performance:

| Model | RMSE | MAE | R² |
|---|---:|---:|---:|
| LinearRegression | 7814.06 | 3888.44 | 0.607 |
| MLPRegressor (64, 32) | 4758.20 | 2597.56 | 0.854 |

The MLPRegressor achieved better test set performance, with lower prediction errors and a higher R² score.

## Project Structure

```text
insurance-cost-prediction/
├── insurance_prediction.ipynb
└── README.md
```

## Installation and Usage

1. Clone or download this repository.
2. Install the required dependencies:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
```

3. Make sure `insurance.csv` is located in the same directory as the notebook.
4. Start Jupyter Notebook:

```bash
jupyter notebook insurance_prediction.ipynb
```

5. Run the notebook cells sequentially.

## Technologies

- Python
- pandas
- NumPy
- Matplotlib
- Seaborn
- scikit-learn
- Jupyter Notebook
