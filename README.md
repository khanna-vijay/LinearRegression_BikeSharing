# Project Name
> Outline a brief description of your project.
# BoomBike - Bike Sharing Demand Prediction Case Study

## Problem Statement
This programming assignment involves building a multiple linear regression model to predict the demand for shared bikes. 

## Business Scenario
A US bike-sharing provider, BoomBikes, has experienced revenue declines due to the ongoing pandemic. To overcome this challenge, BoomBikes aims to create a strategic plan to boost revenue post-lockdown. The goal is to understand the demand for shared bikes after the quarantine situation ends and develop a business strategy to meet customer expectations.

## Objectives
1. Identify significant variables predicting demand.
2. Understand how these variables describe bike demands.
3. Model the demand for shared bikes using available independent variables.
4. Provide insights for formulating a business strategy.

## Model Evaluation
After model building and residual analysis, calculate the R-squared score on the test set.

## Learning Objective
  
- Accurately predict the number of bike rentals for a given time period and location based on historical data and other relevant factors.
- Identify and analyze the key factors that influence bike rental demand, like weather conditions, holidays, and events.
- Develop and evaluate predictive models that can effectively forecast bike rental demand using techniques like regression analysis, time series analysis, and machine learning algorithms.
- Use the forecasting results to optimize bike inventory and resources, ensuring that bike-sharing companies can meet customer demand and maximize revenue.


## Approach
Factors being considered in this analysis for bike sharing demand analysis include weather conditions, seasonality, day of the week and holiday periods.

Understand : 
- What is the expected demand for bikes during peak hours, weekdays, or weekends?
- How does weather (e.g., wind, temperature, precipitation) affect bike rental demand?
- How is the improvement over last year, since the second year would have hidden variables impacting it as promos, awareness etc. 

## 1. Business Understanding
  - Define the problem and objectives:
  - Understand the Business. 
  - What are the KPI's and key metrics required to make profit / customer aquisition
  - Predict demand for shared bikes post-COVID lockdown.
  - Identify significant variables affecting bike demand.
  - Assist in formulating a business strategy.


## 2. Dataset Characteristics
  - Explore 'day.csv':
  - Check data types, missing values, and outliers.
  - Understand Essential Statistics about the Variables, Spread, Mean/Mode, Variable types
  - Understand variable distribution.
  - Review data dictionary for meanings.
  - Univariate Analysis, Bi-Variate and MultiVariate Analysis and understanding of Data.


## 3. Data Cleaning and Preprocessing
   - Handle missing values.
   - Keep 'yr'; it might be valuable.
   - Drop unnecessary columns ('instant', 'dteday').
   - Check and handle outliers.
   - Check for heteroscedasticity and normality.


## 4. Exploratory Data Analysis (EDA)
   - Visualize 'cnt' distribution.
   - Explore relationships between independent variables and 'cnt'.
   - Use correlation analysis to identify significant variables.
   - Check for Normalization. Understand if Data is Normally Distributed. 


## 5. Feature Engineering
   - Create new features if necessary.
   - Convert 'weathersit' and 'season' to categorical string values.
   - Explore interactions between variables.
   - Check for Co-Relation between Independent Variables. 
   - Check VIF > 4.
   - Check P values
   - Reduce OverFitting, Underfitting
   - Select Top variables/features which have most impact on y/outcomes. Identify potential features using python library
    - Check for Standardization if required
    - Some variables like 'weathersit' and 'season' have numeric values (1, 2, 3, 4) with specific labels. Convert them into categorical string values.
    - Column 'yr' with values 0 and 1 represents years 2018 and 2019. Consider retaining it, as bike demand is increasing yearly.


## 6. Train-Test Split
- Split the dataset into training and testing sets.

## 7. Model Building
   - Implement multiple linear regression.
   - Train the model using the training set.
   - The model should predict 'cnt' as the target variable.



## 8. Model Evaluation
   - Evaluate the model on the testing set.
   - Calculate R-squared score for model performance.
   - Check Accuracy against Test Data
   - Check for Errors - MSE
   - Check Confusion Matrix of Predicted vs Actual Scores against Test data-Split

## 9. Residual Analysis
   - Analyze residuals for model assumptions.
   - Use RFE to reduce more variables and check for model efficiency.

## 10. Conclusion and Recommendations
   - Summarize findings and insights.
   - Provide recommendations based on results.
   - Understand Top 10 features contributing significantly towards explaining the demand of the shared bikes.


## 11. Documentation and Reporting
   - Document the process, code, and results.
   - Create a report with visualizations and insights.
   - Document Libraries used


  
## 2. Dataset Characteristics

The dataset 'day.csv' contains the following fields:

- **instant:** Record index
- **dteday:** Date
- **season:** Season (1: Spring, 2: Summer, 3: Fall, 4: Winter)
- **yr:** Year (0: 2018, 1: 2019)
- **mnth:** Month (1 to 12)
- **holiday:** Weather day is a holiday or not (extracted from [DC Holiday Schedule](http://dchr.dc.gov/page/holiday-schedule))
- **weekday:** Day of the week
- **workingday:** If the day is neither weekend nor holiday, it is 1; otherwise, it is 0.
- **weathersit:**
  - 1: Clear, Few clouds, Partly cloudy, Partly cloudy
  - 2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
  - 3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
  - 4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
- **temp:** Temperature in Celsius
- **atemp:** Feeling temperature in Celsius
- **hum:** Humidity
- **windspeed:** Wind speed
- **casual:** Count of casual users
- **registered:** Count of registered users
- **cnt:** Count of total rental bikes, including both casual and registered
  
## Data Understanding
- Explore 'day.csv':
  - Check data types, missing values, and outliers.
  - Understand Essential Statistics about the Variables, Spread, Mean/Mode, Variable types
  - Understand variable distribution.
  - Review data dictionary for meanings.
  - Univariate Analysis, Bi-Variate and MultiVariate Analysis and understanding of Data.


## Conclusions
- Some of the Categorical Variables have a strong effect on dependent variable ‘cnt’.
- The Graphs show a clear Co-Relation of Seasons, Year, Weather Situation, Holiday, and Month. 
- The Highly CoLinear variables as Temp can be dropped without impacting model acuracy. 
- atemp has highest co-relation with Target Variable. 
- The Final Model accuracy was 
R-Squared on testing set: 0.8236158928972526
Adjusted R-Squared on testing set: 0.8124305592761027
Mean Squared Error on testing set: 654483.89934685

- Top 3 Features that contribute significantly to explaining the demand of shared bikes are
1. year
2. WeatherSit_Light_Snow
3. Season_Spring. 




## Technologies Used
- Python: 3.11.5 | packaged by Anaconda, Inc. | (main, Sep 11 2023, 13:26:23) [MSC v.1916 64 bit (AMD64)]
- scikit-learn (sklearn): 1.3.0
- Matplotlib: 3.7.2
- Pandas: 2.0.3
- Seaborn: 0.12.2
- NumPy: 1.24.3
- Statsmodels: 0.14.0
- StandardScaler: sklearn


## Acknowledgements
Give credit here.
- Thank you to the Upgrad and IITB team for simplifying the Data Science and ML Concepts.

## Contact
Created by [@khanna-vijay] - feel free to contact me!

