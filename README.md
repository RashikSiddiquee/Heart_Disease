# Heart_Disease
This will help you to understand the problem and how I approached to solve it. 
This is not comprehensive and there is many more things to be done. Rather this is the beginning. 

# Understanding the problem

Heart disease is a major physiological problem, not just in our country but the whole world. There could be numerous factors behind suffering from a heart disease. Determining the probability of heart disease would allow the physicians to take preventive measures, which could save millions of lives. From an economic viewpoin heart diseases cost billions of dollars each year; predicting the possibility of heart disease could save this lot of money. 

Now there could be many different indicators of a possible heart disease. The data set contains nearly 4000 patient data including different physiological metrics. The target variable is whether there is a risk of heart disease or not. 

# The Approach 
The target variable is binary. So this is a classification problem rather than a regression problem. 

The variables are different physical attributes which could be related to CHD. It is needed to find if there are any relation between the attributes with target variable and also between the attributes. 
Then a model can be produced from it. 

# Data preprocessing 

Data preprocessing.ipnyb

- Data were more or less preprocessed. There werr no categorical values. All of the categorical       values were converted into dummy variables. 
- There were missing values. There was no missing values in target variable. 
- No rows were dropped. 
- As these were body metrics, it was reasonable to fill the missing values with normal human body     data. 
- Scaling was done in standard scaler. But some regression model did not work well with scaled       data. So there had to be two versions made, one scaled and one unscaled. 
- Separation of boolean and numeric columns
- creation of backup dataframe

# Data visualization 
Visualization and correlations.ipnyb

- Countplot for basic description of the attributes. 
- Distplot for better apprehension of the data distribution 
- Crosstabing with barplot to visualize the relation with target variable
- Boxplot to visualize the range, means of different columns with respect to target variable.
- Specific gender based visualization with boxplot, violinplot, catplot. 


- Chi squared test for determining if the categorical variables are correlated to the target or       not. 
- Correlation between the variables.

- Discrepancies in data 

- ANOVA test for determining relationship between target and numeric columns

# Modeling

- Two different dataframes: scaled and unscaled
- Test Train split 

- Check if factor analysis is possible
- Factor analysis. Obtained the number of major factors. 5/6 major factor were determined. 
- Feature selection to remove low variance variables
- Principal Component analysis to determine the major components.  

  Firstly, no variables were removed. 
  Scikit learn uses scaled dataset whereas scaled data affects the coefficient of statsmodel logit   function. This is why two dataframes were needed. 
  
- Logistic regression (Scikit learn), Random forest, SVC, KNN, Decision Tree, Naive Bayes algorithm   was used.
- Logit from statmodel was implememnted to obtain the p values and coefficients. 
- Backward elemination was performed 
- Correlated variables were removed 
- Interpretation of the coefficients 
- Rerun the algorithms with reduced variables. 
- Visualization of model performances


