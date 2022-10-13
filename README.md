# AutoInsurancePrediction-StructuredData
This repository cotains my code that was written for exploratory data analysis, cleaning, prepping, and predictive analytics modeling of structured data with missing, uncleaned data obtained from an auto insurance provider. Below are the steps used in performing this predictive analytics modeling.

Background about input data file:
- .csv format
- structured data
- 100 predictors of data types: float, string, categorical (weekdays, calendar month, state names etc.), binary (0/1,  M/F, Yes/No, etc.)
- 1 target variable which is categorical (0/1)


Step 1 - Clean and prepare data: 
The data in this exercise was simulated to mimic real, dirty data. Data was cleaned with method(s) I believed to be best/most suitable. My success in this exercise  involved feature engineering and avoiding data leakage. I did not add or supplement data from external data source. 
Ideas used:
- Removing columns with >20% missing data
- Creating MetaData DataFrame for Reference
- Imputing NA values for numeric data columns
- Checking for correlations between a pair of data columns and removing all but one of the correlated predictors
- Checking for MultiCollinearity present in several predictors
- Removing MultiCollinear predictors
- One-Hot Encoding of categorical data
 
Step 2 - Build models: 
I built multiple models to predict the output categorical variable (Y) which tok on values 0 or 1. The first model must be a logistic regression, other models that I built included model must be a decision tree, random forest, gradient boosted machine, support vector machine, or neural network. For the multiple models I considered, here, I show two models for reference. First is Logistic regression (as a baseline model) and the other one is Random Forest model, as it provided the best AUC values on the test data provided to me.
 Ideas used:
 - Feature Scaling
 - Sampling
 - Logistic Regression model
 - Random Forest model
 - Comparing Models
 
Step 3 - Generate predictions:
I created predictions Y' = 0 / 1) on the data in test.csv using each of my trained models. The predictions were the class probabilities for belonging to the positive class (labeled '1').   The output a prediction for each of the rows in the test dataset (10K rows) was saved into a .csv file. For the two models, shown, the results of each of my models are saved into  separate CSV file.  Title the two files 'glmresults.csv' and 'nonglmresults.csv'. Each file has a single column representing the predicted probabilities for its respective model. The header label or index columns were not included in the saved file. 
 
Step 4 - Compare the modeling approaches:
I provide an executive summary that includes a comparison of my two modeling approaches, with emphasis on relative strengths and weaknesses of the models.
 
