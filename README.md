## _Predicting Monetary Damage Caused by Property Fires_NFIRS Data_

### **Project Description**

The goal of this project is to develop a predictive model to estimate the monetary damage caused by property fires. Specifically, linear regression models will be used to analyze historical fire data and identify the key factors that contribute to the severity of property damage, such as the type of property, location, time of day, and the response time of firefighters. The data has been extracted from National Fire Incident Reporting System (NFIRS) . The model will be trained and validated using a combination of supervised learning techniques and cross-validation methods. The ultimate objective is to build a model that can accurately estimate the monetary damages caused by a fire, which can be used by insurance companies and property owners to better assess the risks associated with fire damage and take appropriate mitigation measures.


### **About the Models**

* ***The predictor variables used for modeling have values in different ranges / scales , & hence the models' predictions were skewed initially since the predictor variables having values with a larger scale had a stronger influence on the model.We then standardized the variables to fix this problem.***

* ***The predictor variables (numeric variables) used for modeling did not follow a Normal Distribution and this affected the model's performance. Transforming the distribution of the variables using Power Transformer helped to improve the R2 values for the models significantly.***

* ***From the Summary Table for OLS model, we see that there are predictor variables having p-values greater than 0.05. Instead of dropping these variables, we have used these variables for modeling which has impacted the model's performance.***

* ***We can see from the correlation heat map that none of the predictor variables have a strong correlation with the target variable 'PROP_LOSS' . Hence, we haven't been able to capture too much variance using the 11 Predictor Variables used in the subset. That is why the R2 values for all 3 models are found to be less than 0.3 for Test Set.Hence,more variables will have to incorporated into the model to capture more variance & improve the R2 values.***

* ***The R2 values for test set is comparable to R2 values for the training set for all 3 models. Hence , we can say that these models are not overfitting. So, although the predictive power for the models is not great, we can still categorize these models as 'good'.***


* To improve the prediction power , we have tried the Random Forest Model as well.

* We got the highest R2 value for the Random Forest Model , with an R2 value of 0.55 for the Training Partition & 0.52 for the Test Partition.

* The Mean Absolute Errorr & Median Absolute errors were also found to be the lowest for the Random Forest Model.
