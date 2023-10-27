**Data Analysis for Predicting the house prices**

In this data analysis project our aim would be to predict the house prices taken of the test dataset where AMES housing dataset has been considered which consists of data of 1000 houses which would help to build the model to make prediction on the test dataset.

**Description about DATA for the project**
* Considered Dataset : AMES housing dataset
* Target Feature : SalePrice


**Data Loading and Initial Inspection**

*   We initialised the train and test data from the given local dataset.
*   Combined the Train and Test data for initial data preprocessing which later on would be seperated.



**Missing Values and Exploratory Data Analysis**

*  Identified features with missing values and their type whether it is a temporal, numerical , categorical : ordinal or non-ordinal for the further handling.
*   Dropped the feature with major missing value. (i.e. PoolQC in our case which has almost more than 95% of data missing.)


**Data Engineering**

* Check how much the feature with less data is related to the target column, if we can drop them or not.
*  **Numerical Feature** : Features identified as numerical features were checked for the missing values which was then filled up by mean.
*  **Temporal Feature** : Features containing year were identified which were then checked against the target column to check the relationship of how its affecting the saleprice of the houses.
*  **Categorical Feature** :
Categories in categorical Features were turned into numerical values and the missing data points were filled up with median or mode depending on its nature.
 * Ordinal Categorical Features : After finding out the ordinal categories a set of numerical value was assigned to categories of each feature to find the relative strength of the value.

 * Non Ordinal Categorical Feature : The non ordinal features were encoded using getdummies where multiple new features were created as a result of encoding of categories.

* After finishing the cleaning and encoding part of the combined dataset the dataset has been seperated into train and test data as it was in the beginning to conduct experiment on modelling and further optimisation with the help of training data and test it on the test data.

**Modelling** :

For modelling and better results I have tried to use multiple model selection and feature optimisation techniques to find out the best model with the lowest RMSE score of the prediction dataset which includes :
  * Linear Regression
  * Ridge Regression
  * Feature selection using forward subset selection
  * Cross validation approach


**Underfitting Vs Overfitting**:

Underfitting vs overfitting was conveyed by changing the considered parameter for training the model to determine how the model is underfitting or overfitting the data at the time of prediction.

**Final Model**

Non other than the **Simple Linear Regression** was considered to be delivering the best results rather than considering any fancier regression technique or a special subset of features as a final model for the least rate of RMSE.


