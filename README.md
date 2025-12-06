Team Members -
Poulomi Chakraborty
Khwrwmsar Basumatary
Mohit Modi
Pakijur Rahman
Tenzing Basumatary

📌 Project Overview

This project focuses on analyzing a synthetic dog health dataset and building a logistic regression model to predict whether a dog is Healthy or Not Healthy.
The workflow includes:
Data loading
Data cleaning & preprocessing
Handling null values
Encoding & removing irrelevant features
Train–test splitting
Logistic Regression modeling using StatsModels
Evaluating model summary and significance of predictors
The goal is to understand which features contribute to predicting a dog's health and to build a statistically interpretable model.

📂 Dataset

File used: synthetic_dog_breed_health_data.csv

The dataset includes attributes such as:
Breed
Breed Size
Age
Weight
Diet
Activity Level
Daily Walk Distance
Spay/Neuter Status
Food Brand
Environmental factors
Health indicators (target variable: Healthy)
During preprocessing, many non-significant or non-numeric columns were removed before modeling.

🔧 Technologies & Libraries Used

Python
Pandas – Data handling
NumPy – Mathematical operations
Seaborn / Matplotlib – Visualization
Scikit-Learn – Train-test split
StatsModels – Logistic regression model

🧹 Data Cleaning Steps

Key preprocessing performed:
Removed rows where the Healthy target value was null.
Checked & removed duplicate rows.
Filled missing values:
Mode for categorical features
Mean for numerical features
Dropped irrelevant or high-cardinality columns:
Example: Breed, Diet, Age, Food Brand, etc.
Converted Healthy column to integer (0/1).
Added constant term before logistic regression.

🧠 Modeling

A Logit (Logistic Regression) model was trained using:
model = sa.Logit(ytrain, xtrain_c).fit()

Outputs include:
Coefficient significance
P-values
Model fit statistics
Understanding how each attribute influences the probability of a dog being healthy

📈 Results

The model.summary() provides:
Overview of significant predictors
Statistical confidence
Model strength & performance (Pseudo R², log likelihood)
This helps interpret which variables meaningfully affect health status.

▶️ How to Run the Notebook
Place the dataset file in the same directory as the notebook.
Install dependencies:
pip install pandas numpy seaborn statsmodels matplotlib scikit-learn
Run the notebook sequentially from top to bottom.
Ensure the CSV file loads correctly.

📜 Future Improvements

Use different ML models (Random Forest, XGBoost)
Improve feature engineering
Add visualizations for deeper insights
Build a web interface for predictions
