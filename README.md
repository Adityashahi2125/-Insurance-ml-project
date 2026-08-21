# Insurance Cost Prediction — Machine Learning Project

# 📌 Project Overview

This project focuses on analyzing health insurance data and developing a machine learning model to predict individual medical insurance charges.

The project follows a complete data science workflow, including data exploration, data cleaning, preprocessing, feature engineering, feature extraction, statistical feature selection, and predictive modeling.

The primary objective is to understand the factors that influence medical insurance charges and build a Linear Regression model for predicting insurance costs.

⸻

# 🎯 Objectives

The main objectives of this project are:

* Perform Exploratory Data Analysis (EDA) on the insurance dataset.
* Understand the distribution and relationships between different features.
* Identify missing values and duplicate records.
* Clean and preprocess the dataset for machine learning.
* Convert categorical variables into numerical representations.
* Perform feature engineering and feature extraction.
* Analyze feature relationships using statistical techniques.
* Select relevant features for predictive modeling.
* Train a Linear Regression model.
* Evaluate model performance using R² Score and Adjusted R² Score.

⸻

# 📊 Dataset

The project uses an insurance dataset containing information about individuals and their medical insurance costs.

Features

Feature	Description
age	Age of the individual
sex	Gender of the individual
bmi	Body Mass Index
children	Number of dependent children
smoker	Whether the individual is a smoker
region	Residential region
charges	Medical insurance charges

Target Variable

charges

The target variable represents the individual medical insurance cost that the machine learning model attempts to predict.

⸻

# 🔍 Exploratory Data Analysis

The dataset is explored to understand its structure, distributions, and relationships.

The following analysis is performed:

* Dataset shape and structure
* Data types
* Descriptive statistics
* Missing-value analysis
* Numerical feature distributions
* Categorical feature distributions
* Boxplots for numerical variables
* Correlation analysis
* Correlation heatmap

# Visualizations

The project uses Matplotlib and Seaborn to create visualizations such as:

* Histograms with KDE
* Count plots
* Boxplots
* Correlation heatmap

These visualizations help identify patterns, distributions, potential outliers, and relationships between variables.

⸻

# 🧹 Data Cleaning and Preprocessing

The following preprocessing steps are performed:

## 1. Duplicate Removal

Duplicate records are removed from the dataset to avoid redundant observations.

df_cleaned.drop_duplicates(inplace=True)

## 2. Missing-Value Checking

Missing values are checked across all columns before proceeding with modeling.

## 3. Categorical Encoding

Categorical variables are converted into numerical form.

For example:

sex
male   → 0
female → 1

and:

smoker
no  → 0
yes → 1

The columns are then renamed for better interpretability:

sex     → is_female
smoker  → is_smoker

## 4. One-Hot Encoding

The region feature is converted into numerical dummy variables using one-hot encoding.

⸻

# 🛠️ Feature Engineering and Feature Extraction

Feature engineering is performed to create more meaningful information from the existing variables.

BMI Categorization

The continuous bmi variable is transformed into meaningful categories:

BMI Range	Category
< 18.5	Underweight
18.5 – 24.9	Normal
25 – 29.9	Overweight
>= 30	Obese

These categories are then converted into numerical features using one-hot encoding.

⸻

# 📐 Feature Scaling

Standardization is applied to selected numerical features:

* age
* bmi
* children

The project uses StandardScaler from Scikit-learn.

Standardization transforms numerical features so that they have a comparable scale, which is useful for machine learning algorithms that are sensitive to feature magnitude.

⸻

# 📈 Statistical Feature Analysis

The project uses statistical techniques to investigate the relationship between features and the target variable.

Pearson Correlation

Pearson correlation is calculated between selected numerical/binary features and the target variable charges.

This helps measure the strength and direction of linear relationships.

# Chi-Square Test

A Chi-Square test is applied to categorical features.

The target variable charges is divided into four groups using quantiles, and the relationship between categorical features and the grouped target is analyzed.

A significance level of:

α = 0.05

is used to determine whether a feature has a statistically significant association with the target.

⸻

# 🤖 Machine Learning Model

## Linear Regression

A Linear Regression model is trained to predict medical insurance charges.

The dataset is divided into:

* 80% Training Data
* 20% Testing Data

using:

train_test_split(
    X,
    y,
    test_size=0.20,
    random_state=42
)

The model is then trained using the training dataset and used to generate predictions on the testing dataset.

⸻

# 📊 Model Evaluation

The Linear Regression model is evaluated using:

R² Score

R² (R-squared) measures how well the model explains the variation in the target variable.

A higher R² value generally indicates that the model explains more of the variation in the target.

Adjusted R² Score

Adjusted R² accounts for the number of predictors included in the model.

It provides a more controlled measure of model performance when multiple features are used.

⸻

# 🧰 Technologies and Libraries

The project is implemented in Python using the following libraries:

* Python
* NumPy — Numerical computing
* Pandas — Data manipulation and analysis
* Matplotlib — Data visualization
* Seaborn — Statistical visualization
* SciPy — Statistical analysis
* Scikit-learn — Machine learning and preprocessing
* Jupyter Notebook — Interactive development environment

⸻

# 📁 Project Structure

insurance-ml-project/
│
├── Insurance.ipynb       # Complete analysis and machine learning workflow
├── insurance.csv         # Insurance dataset
└── README.md             # Project documentation

⸻

# 🚀 How to Run the Project

1. Clone the Repository

git clone https://github.com/Adityashahi2125/insurance-ml-project.git

2. Navigate to the Project

cd insurance-ml-project

3. Install Required Libraries

pip install numpy pandas matplotlib seaborn scipy scikit-learn jupyter

4. Start Jupyter Notebook

jupyter notebook

5. Open the Notebook

Open:

Insurance.ipynb

Make sure insurance.csv is present in the same project directory.

⸻

# 📌 Key Machine Learning Workflow

The complete workflow followed in this project is:

Raw Dataset
     ↓
Data Understanding
     ↓
Exploratory Data Analysis
     ↓
Data Cleaning
     ↓
Categorical Encoding
     ↓
Feature Engineering
     ↓
Feature Extraction
     ↓
Feature Selection
     ↓
Feature Scaling
     ↓
Train-Test Split
     ↓
Linear Regression
     ↓
Prediction
     ↓
Model Evaluation

⸻

# 📈 Future Improvements

The project can be further improved by:

* Comparing multiple regression algorithms.
* Applying cross-validation.
* Performing hyperparameter tuning.
* Comparing Linear Regression with tree-based models.
* Performing more advanced feature engineering.
* Analyzing model residuals.
* Using additional regression evaluation metrics such as MAE and RMSE.
* Improving model interpretability.
* Deploying the final model as a web application or API.

⸻

This project was developed as part of a practical learning journey in Data Analysis, Feature Engineering, and Machine Learning.

⸻

⭐ Project Highlights

Data Analysis → Data Cleaning → Feature Engineering → Statistical Analysis → Feature Selection → Machine Learning → Model Evaluation
