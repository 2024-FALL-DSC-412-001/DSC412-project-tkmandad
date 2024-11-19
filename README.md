# DSC412-project

This repository contains any code and files for the DSC412 project.

The project proposal and plan are in DSC412_001_FA24_PR_tkmandad.pdf

# Iowa House Price Prediction using ML techniques

## Project Overview
The objective of this project is to develop and evaluate predictive models for estimat- ing house prices in Iowa, using a dataset that encompasses a wide range of property attributes. In order to create an effective predictive model, we employed linear regres- sion and two regularization techniques—Ridge and Lasso regression. By leveraging these methods, we aimed to handle potential multicollinearity among features and improve the model’s predictive accuracy.

The data preparation involved cleaning, feature selection, and scaling to ensure that our dataset was consistent and ready for modeling. Following this, we split the data into training, validation, and test sets to facilitate model development and unbiased perfor- mance evaluation. Ridge and Lasso regression were applied with varying regularization parameters to identify the best model for minimizing the mean squared error (MSE). This report details the methods, findings, and conclusions derived from these modeling efforts.

## Files
- `DSC 412_ Project_main.ipynb`: The main notebook containing all code for data collection, processing, and analysis.
- `IA_House_Price_Original_Data.xlsx`: File contains the actual data of Iowa House Prices.

## Dataset
The dataset consists of multiple columns, each representing different attributes related to house prices, with 2,908 data points in total.
  
## Data Processing
- **Cleaning Data**: To assess the uniqueness of the data, the number of unique values was calculated for each column, and each column was checked for missing (NaN) values and duplicates.To handle missing values, numerical columns were filled with the median of each respec- tive column, while categorical columns were filled with the most frequent value (mode).
- **Feature Selection**: Features were selected from the dataset to build the model. Two categorical and twenty-one numerical features were chosen for this process. The categorical features included BsmtQual (which evaluates the height of the basement) and Neighborhood (which refers to physical loca- tions within the Ames city limits).
- **Splitting Data and Scaling**: The dataset was split into three subsets: training, validation, and test sets. This allowed for proper evaluation of model performance dur- ing training and final testing.After splitting the data, feature scaling was applied to the features and the target variable SalePrice.

## Model Building
The project implemented multiple models:
1. **Linear Regression**: This model was fit to the scaled training data using the Lin- earRegression() function from the scikit-learn library. 
2. **Ridge Regression**: This regression technique introduces a regularization term to linear regression. and works to minimize the function
3. **Lasso Regression**: Un-like Ridge regression where we squared our coefficients, Lasso regression uses the absolute value. This term not only shrinks the coefficients but can also force some to be exactly zero, effectively performing variable selection.


## Results and Evaluation
To choose our model we analyzed the calculated MSEs. The Ridge model with λ=0.10 was chosen as the best model based on its performance on the validation set. To further evaluate the Ridge model, it was implemented on the test dataset. The resulting MSE was 0.1482, indicating that our model generalizes well.

# Getting Started Instruction

You can run your tests in terminal by doing the following:

Make sure your terminal is in this directory. You can confirm that is true by typing `pwd` in terminal.

Create a virtual environment with

`python -m venv ./.venv`

Then activate it in terminal:

Windows: `.\.venv\Scripts\activate`

Mac: `source ./.venv/bin/activate`

Linux: `source ./.venv/bin/activate`

You should see `.venv` appear in the terminal on the left side of teh command line.

Then run `pip install -r requirements.txt` in terminal
