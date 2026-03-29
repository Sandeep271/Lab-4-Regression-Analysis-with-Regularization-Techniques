# MSCS_634_Lab_4

## Lab Title
Regression Techniques and Regularization on the Diabetes Dataset

## Student Information
**Name:** Sandeep Parupalli  
**Course:** Advanced Big Data and Data Mining (MSCS-634-B01)  
**Instructor:** Satish Penmatsa  
**University:** University of the Cumberlands  

## GitHub Repository
Repository for this lab submission:  
https://github.com/Sandeep271/Lab-4-Regression-Analysis-with-Regularization-Techniques

## Purpose of the Lab
The purpose of this lab was to apply and compare several regression techniques using the Diabetes dataset from `sklearn.datasets`. The work focused on understanding how different regression models perform on the same prediction task and how regularization methods such as Ridge and Lasso can help reduce overfitting and improve generalization.

## Dataset Used
This lab uses the Diabetes dataset from scikit-learn. It contains 442 observations and 10 standardized baseline health variables. The target variable represents a quantitative measure of disease progression one year after baseline.

## Models Implemented
The notebook includes the following models:
- Simple Linear Regression
- Multiple Linear Regression
- Polynomial Regression
- Ridge Regression
- Lasso Regression

## Evaluation Metrics
Each model was evaluated using:
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R-squared (R²)

## Summary of the Work Completed
The notebook begins with data loading, basic exploration, summary statistics, a missing-value check, and a target distribution plot. After the dataset was reviewed, the analysis moved through the required regression techniques in a structured order.

A simple linear regression model was created first using BMI as the single predictor because it showed the strongest individual relationship with the target. This served as a baseline.

A multiple linear regression model was then trained using all available features. After that, polynomial regression models with degree 2 and degree 3 were tested to show how increasing model complexity can improve fit on training data while also increasing the risk of overfitting.

Finally, Ridge and Lasso regression models were trained using multiple alpha values so the effect of regularization strength could be compared directly.

## Key Insights from the Regression Analysis
- **BMI** showed the strongest individual relationship with the target variable, which is why it was selected for the simple linear regression baseline.
- **Multiple linear regression** performed much better than the simple linear model because it used all available features instead of only one.
- **Polynomial regression (degree 2)** added flexibility, but it did not outperform the strongest regularized models.
- **Polynomial regression (degree 3)** overfit the training data and performed very poorly on the test set, showing that too much model complexity can reduce real predictive performance.
- **Ridge regression** produced stable results and slightly improved generalization compared with standard multiple regression.
- **Lasso regression** performed best overall in this analysis with a moderate alpha value and also simplified the model by shrinking some coefficients to zero.

## Final Model Performance Summary
Based on the test data:
- **Best model:** Lasso Regression with alpha = 1.0
- **Best RMSE:** approximately **53.15**
- **Best R²:** approximately **0.467**

Other strong models included:
- Ridge Regression with alpha = 100.0
- Standard Multiple Linear Regression

## Challenges Faced and Decisions Made
- I needed to choose one feature for simple linear regression, so I selected **BMI** because it had the strongest correlation with disease progression.
- I used the same training and testing split across the models to keep the comparison fair.
- I applied **StandardScaler** before Ridge and Lasso because regularized models are sensitive to feature scale.
- I tested multiple alpha values for Ridge and Lasso to observe how regularization strength affected model performance.
- I compared both polynomial degree 2 and degree 3 models to clearly demonstrate the difference between a more flexible model and an overfit model.

## Files Included in the Repository
- `MSCS_634_Lab_4_Regression_Analysis.ipynb` — Complete notebook with code, outputs, visualizations, and written analysis
- `README.md` — Summary of the lab, major insights, and implementation decisions

## How to Run the Notebook
1. Open the notebook in Jupyter Notebook or JupyterLab.
2. Run the cells from top to bottom.
3. Review the generated tables, evaluation metrics, plots, and final comparison discussion.

## Conclusion
This lab showed that stronger model complexity does not always produce better results. Multiple regression improved substantially over the simple baseline, polynomial regression demonstrated the risk of overfitting, and regularization helped improve stability and generalization. Overall, a moderately regularized linear model provided the best balance of performance and robustness on the Diabetes dataset.
