# NPRI-Data-project
The provided project outlines the use of various machine learning techniques, including feature engineering, data preprocessing, and modeling, to analyze and predict pollutant emissions, particularly from fossil fuel-based electric power generation. Below is an overview of the project's key components:

Project Goals:
Predict Substance Emissions: Forecast the quantity of pollutants released by fossil fuel electric power generators.
Identify Key Contributors: Analyze the factors influencing emissions, with a focus on various substances.
Data:
Dataset: Contains emission data categorized by facility, year, substance, and other operational details.
Features: Includes YearMinus1, YearMinus2, Quantity, pollutant categories, and operational variables (e.g., NAICSPrimary, FacilityName).
Methodology:
Preprocessing:

Converted categorical data into numeric values using techniques like target encoding.
Addressed missing values and normalized data for consistency.
Removed or transformed highly correlated features to reduce redundancy.
Feature Engineering:

Added new derived features, such as average emissions per NAICS category and standard deviations for emissions.
Modeling:

Multiple regression models were explored, including:
Linear Regression: Performed poorly with high RMSE and low 
𝑅
2
R 
2
  values.
Decision Tree Regressor: Moderate performance.
Random Forest Regressor: Best model with optimized hyperparameters achieving an 
𝑅
2
R 
2
  score of 0.69 and RMSE of ~153,000.
Predictions were generated for 2023 emissions based on trends and past data.
Hyperparameter Tuning:

Conducted Randomized Search CV to fine-tune the Random Forest model parameters, leading to improved prediction accuracy.
Validation:

Split the data into training, validation, and test sets for unbiased performance evaluation.
Results:
Predictions: Forecasted emissions for the year 2023 for various facilities, with specific focus on pollutants like PM2.5 and nitrogen oxides.
Model Performance:
Random Forest emerged as the best model for predicting emissions.
Metrics for the Random Forest model:
RMSE: ~153,000
𝑅
2
R 
2
 : 0.69 (indicating reasonably good fit)
