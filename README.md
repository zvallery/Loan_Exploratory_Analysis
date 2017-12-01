# Loan Analysis Data Science Project 

## Abstract
- I took on this project so that I could get some experience with a data science project and with building a predictive model in particular.  I found the project on a website called [Analytics Vidhya](https://www.analyticsvidhya.com/blog/2016/01/complete-tutorial-learn-data-science-python-scratch-2/#).  

## Contributor

  - Zachary Vallery

## Challenges
- Often times the code wouldn't work when I typed it in or even copied it directly from the tutorial so for things like munging the data I had to figure out a process on my own.  Also for two of the three predictive models that I created in the project, I had to troubleshoot some problems which were due to typos by the tutorial creator.

## Results
#### Using Logistic Regression:
```python
outcome_var = 'Loan_Status'
model = LogisticRegression()
predictor_var = ['Credit_History']
classification_model(model, df,predictor_var,outcome_var)
```
Accuracy : 80.945%
Cross-Validation Score : 80.946%

#### Using Decision Tree:
```python
model = DecisionTreeClassifier()
predictor_var = ['Credit_History','Gender','Married','Education']
classification_model(model, df,predictor_var,outcome_var)
```
Accuracy : 81.270%
Cross-Validation Score : 81.110%

#### Using Random Forrest:
```python
model = RandomForestClassifier(n_estimators=100)
predictor_var = ['Gender', 'Married', 'Dependents', 'Education',
       'Self_Employed', 'Loan_Amount_Term', 'Credit_History', 'Property_Area',
        'LoanAmount_log','ApplicantIncome#Create a series with feature importances:
featimp = pd.Series(model.feature_importances_, index=predictor_var).sort_values(ascending=False)
print featimp']
classification_model(model, df,predictor_var,outcome_var)
```
## Conclusion
- I think this project was a sufficient introduction to data science and will serve as a good model for me as I move forward and complete more projects independently.  I uploaded the full python code from Jupyter Notebook and the data set I used in this repository for viewing.
