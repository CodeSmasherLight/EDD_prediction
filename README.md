# EDD(Estimated Delivery Date) Prediction

## Overview
This Jupyter Notebook (EDD_Final1.ipynb) is designed to predict order delivery SLA (Service Level Agreement) using machine learning techniques. It involves data preprocessing, feature engineering, model training, and evaluation. The notebook utilizes libraries such as pandas, numpy, scikit-learn, matplotlib, seaborn, geopy and lightgbm.

## Installation
Install the required libraries using pip:

``` 
$ python -m pip install pandas numpy scikit-learn matplotlib seaborn geopy lightgbm

```

## Data Loading
The notebook loads three datasets:

- train_df: Training data
- test_df: Test data
- pincodes_df: Pincode data with geospatial information

## Data Preprocessing
### Pincode Data Cleaning
- Latitude and longitude values are extracted and converted to numeric types.

### Merging Geospatial Information
- Geospatial information from pincodes_df is merged with the training and test datasets.

### Handling Missing Values
- Missing values are handled using forward fill.

## Feature Engineering
### Date Features
- Extracts month, day of the week, and weekend indicator from order_shipped_date.

### Distance Calculation
- Calculates the distance between pickup and drop locations using the Haversine formula.

### Courier Performance Features
- Calculates and merges average SLA for each courier partner.

## Model Training
### Data Splitting
- Splits the training data into training and validation sets.

### Imputation and Scaling
- Imputes missing values and standardizes features.

### Model Training
- Trains a Voting Regressor with Gradient Boosting and LightGBM.

## Model Evaluation
- Evaluates the model on the validation set using RMSE (Root Mean Squared Error).

## Prediction and Submission
- Makes predictions on the test data and saves the results to a CSV file.

## Visualization
- Includes visualizations for SLA distribution and the relationship between distance and SLA.

## Conclusion
- This notebook provides a comprehensive workflow for predicting order delivery SLA using various data preprocessing, feature engineering, and machine learning techniques.

