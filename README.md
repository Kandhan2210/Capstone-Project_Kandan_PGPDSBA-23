**Life Insurance Sale Capstone Project**

**Business Problem Understanding:**

**Introduction of the business proble**m:
  The dataset belongs to a leading life insurance company. The company wants to predict the bonus for its agents so that it may design appropriate engagement activity for their high performing agents and up skill programs for low performing agents
Executive Summary
  Understanding  the business problem:
	  All Life Insurance companies offer various incentive plans for their employees, to boost their sales and to have higher balance of insurance plans, “The higher the Insurance amount the higher the bonus pay out”. However, not all companies get successful in the above Mantra. Some companies fail to have a better plan for bonus payouts. For such companies we should study the data and need to understand the requirements to implement the above plan. Where in, the company can predict the bonus for its employees and design appropriate engagement activity for their high performing employees and also have training programs for non/low performing employees.
The business environment - Life insurance sector in India, 
India has 67 insurers of which 24 are life insurers, 26 are general insurers, 5 are stand-alone health insurers, and 12 are re-insurers (March 2022).
India’s insurance premium volume stands at $ 127 Bn as of 2021 (Life – 76%, Non-Life – 24%). 
Total insurance premium in India increased by 13.5% in 2021 as against a global average of 9%.
Motivate agent for more sales, increase market share & profit and retaining agents. 
Increasing awareness for life insurance, more lives getting insured.

**Modeling Approach Used and Why:**
  Merged data from other sources such as, demographic information, account details etc. for further deep analysis
Data Quality and preparation activities were performed such as  missing value treatment, imputation, data type conversions for homogeneity in the data set
Performed EDA on the data to understand the data and to determine any outlier and treatment for the same
The purpose of Univariate Analysis is to find out which variables have clear separation for the target variable – separation of mean & median of continuation variables and their skewness affecting the target variable – Agent bonus. 
Bivariate analysis is to establish the relationship among various independent variables and with dependent variables.
Also used ANNOVA to understand if the model performance can be improved and very significance test of variable through ANNOVA
Checking unbalance data  which is very critical to classification problem
**Model building and interpretation.**
Liner discrimination analysis & Kmeans are suited for classification problem
Model building approach (Multicollinearity – VIF, significant features & their selection process based on p-values & coefficient estimates etc.)
**Model Tuning **
  Actionable business insights like identification of features which are contributing to increase in bonus (e.g. sum assured) so that company could focus on those features for up skilling agents.
**Insights**
  Insights from models, one unit change of a significant feature resulting how much change in bonus. - Delta of coefficients from linear models.  Likewise, feature importance of optimum model.
  specific recommendations to up skilling the low performing agents and incentivizing the high performing agents.

**  Exploratory Data Analysis:**
            3Categorical Variable’s Univariate Analysis
            Most Customers approached are Post Graduates having 47% weightage.
            Acquisition of a customer is mostly done Via an Agent having 71% weightage.
            Most customers have Salaried Occupations around 48%. 
            Here freelancers have a low weightage.
            Approximately 59% of customers are males.
            Most customers are either an executive or managers having weightage of 37% and 36% respectively.
            Around 50% of the customers are married.
            West Zone brings the most Customers with 57% weightage. 
            Around 59% of Customers went for half-yearly payment plan

****Outlier Treatment ****
    Correlation between the various features and Principal Component
**Modeling Approach Used and Why:**
    Modelling approach used here is Linear Regression, which is a machine learning algorithm based on supervised learning. 
It performs a regression task.
Regression models a target prediction value based on independent variables. It is mostly used for finding out the relationship between variables and forecasting.
The other  models tested and compared alongside Linear Regression were Decision Tree Regressor, Random Forest Regressor and Artificial Neural Network(ANN)Regressor.

**Linear Regression of Predicted Values:**

**Model Selection**
          From the previous results, it is evident that Linear Regression is a better model
          Why Linear Regression?
          Post removal of variables causing multicollinearity, Linear Regression provided a good R squared value and similarly a high adjusted R squared value Hence a good percentage of variance can be successfully explained by our model.
          A very important factor being the train and test set accuracy scores are 80 and consistent
          Unlike other models where overfitting and inconsistency in the performance metrics can be observed Linear Regression model does not show these inconsistencies in the observation
          (Here by overfitting we mean, the model is performing very good for training set and giving poor results for the testing set)
          The LR model makes it easier to understand the model, multicollinearity in the data also, unlike other model its computational time is quick therefore we can run it multiple times whereas ANN and Random Forests needs capable machines as they are very time consuming models Might have to wait for hours and in our case they still don’t perform better than LR.

Note: 100 % accuracy cannot be achieved in real life data as there is always some unexplainable factors and noise that’s always present in our data.

**Model Evaluation:**

From the equation the variables with a low or no coefficient value depicts that the variable is very important to the independent variable’s prediction. 

As the coefficients value increase it shows the variable has become comparatively less significant.

**Insights from Analysis:**
R-Squared Obtained from final Linear Regression Model:0.807 (LM1) & 0.806 (LM2)
Adjusted R-Squared Obtained from final Linear Regression Model:0.805
Here, R-squared (R2) is a statistical measure that represents the proportion of the variance for a dependent variable that’s explained by an independent variable or variables in a regression model.

**Decision Trees, Random Forest, and ANN(Before Hyper parameter Tuning):**
      It can be observed that all the 3 models have over fitting problems where we have ideal accuracies of ~100% for our training set. However the models are performing poorly on our testing set having accuracies ~70% -84%. 
      There is a major accuracy difference between the training and testing set which is not acceptable for predictions.
      If the accuracy difference is greater than 6-10% it is advised to not accept the model as the predictions can be unreliable.
      
**Decision Trees, Random Forest, and ANN (After Hyperparameter Tuning):**
    After Hyperparameter Tuning Decision Trees and Random Forest models showed no overfitting errors.
    The training accuracies were ~85% and testing accuracies were~80%.
    ANN still showed no improvement in results and was still overfitting.

Although the Decision Trees and Random Forest were performing good, I went with Linear Regression as it gave more stable results and Variable importance could be calculated more easily from the Linear Regression Equation and stats-model performed to predict the results.

**Recommendations:**

For High Performing Agents we can create a healthy contest with a threshold.
Where, if they achieve the desired sum assured, they are eligible for certain incentives like latest gadgets, exotic family vacation packages and some extra perks as well.
For low performing agents, we can introduce certain feedback upskill programs to train them into closing higher sum assured policies, reaching certain people to ultimately becoming top/high performers.
Apart from this, we need more data/predictors like Premium Amount, this will help us to solve the business problem even better as well have more variables to test upon thereby having more accurate results in real-time problems like this.
I also feel another predictor can be added as customers geographic allocation or Region and not just the zones as people living in rural areas are less likely to buy a policy where as those living in a highly developed location are likely to be belonging to the upper class and should be targeted.
Similarly, another predictor can be AgentID can be introduced which will make it easier to observe the high and low performing agent trend.



















