# House_pricing_case_study
Learning Preprocessing using the house price dataset

Project Overview

This project performs Exploratory Data Analysis (EDA) and Data Preprocessing on a House Pricing dataset. The notebook includes data cleaning, missing value handling, correlation analysis, feature scaling, encoding, outlier treatment, and train-test splitting to prepare the dataset for machine learning models.

Dataset

The dataset contains various features related to residential properties, including:

Sale Price (Target Variable)
Number of Bedrooms
Number of Bathrooms
Flat Area (Sqft)
Lot Area (Sqft)
Overall Grade
Age of House
Waterfront View
Condition of the House
Zipcode
Latitude & Longitude
Renovation Information
Other house-related attributes
Project Workflow
1. Data Loading
Import required libraries.
Load the House Pricing dataset using Pandas.
2. Exploratory Data Analysis (EDA)
Dataset information and summary statistics.
Duplicate row and column detection.
Correlation analysis.
Correlation heatmap visualization.
3. Missing Value Handling
Remove rows with missing target values (Sale Price).
Fill numerical missing values using:
Median Imputation
Fill categorical missing values using:
Mode Imputation
Drop columns with excessive missing values when necessary.
4. Feature Scaling

Features are categorized based on skewness:

Standard Scaling

Applied to relatively symmetric features such as:

ID
Overall Grade
Age of House (in Years)
Zipcode
Latitude
Min-Max Scaling

Applied to skewed numerical features.

5. Feature Encoding
Label Encoding

Used for:

Binary categorical features
Target-related categorical variables
One-Hot Encoding

Used for:

Condition of the House
Date House was Sold
6. Outlier Detection and Treatment
Visualization
Boxplots for numerical columns.
IQR Method

Outliers are detected using:

IQR = Q3 - Q1

Lower Bound = Q1 - 1.5 * IQR
Upper Bound = Q3 + 1.5 * IQR
Treatment
Clipping extreme values
Filtering observations within acceptable ranges
7. Train-Test Split

Dataset is divided into:

Training Set: 80%
Testing Set: 20%
from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(
    X,
    y,
    test_size=0.2,
    random_state=42
)
Libraries Used
numpy
pandas
matplotlib
seaborn
scikit-learn
statistics

Install dependencies:

pip install numpy pandas matplotlib seaborn scikit-learn
Key Techniques Implemented
Data Cleaning
Duplicate Removal
Missing Value Imputation
Correlation Analysis
Feature Scaling
Label Encoding
One-Hot Encoding
Outlier Detection (IQR Method)
Train-Test Splitting
Project Structure
  'Case_study2.ipynb'
  'House_Pricing.csv'
  'README.md'
Future Improvements
Feature Selection
Feature Engineering
Model Training and Evaluation


This project was developed for learning and practicing data preprocessing and exploratory data analysis techniques on a real-world House Pricing dataset.
