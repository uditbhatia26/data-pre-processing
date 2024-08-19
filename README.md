# Dataset Cleaning


# Overview
This repository contains the code and documentation for cleaning a dataset involving demographic and employment-related features. The primary aim was to preprocess the data to ensure its quality and suitability for analysis or machine learning tasks.

# Dataset<br>
The dataset includes the following features:

age: Age of the individual <br>
education-num: Numeric representation of the education level <br>
hours-per-week: Hours worked per week <br>
workclass: Type of employment <br>
occupation: Job role <br> 
sex: Gender <br>
salary: Salary class (e.g., <=50K, >50K)  <br>


# Data Cleaning Steps 
# <li> Import Libraries

Imported necessary libraries: numpy, pandas, seaborn, and matplotlib.<br>
# <li> Read Dataset

Loaded the dataset using pandas.
# <li> Remove Irrelevant Features

Removed the following features: <br>
fnlwgt: This feature was removed as it was deemed irrelevant to the analysis. <br>
native-country: This feature was removed because more than 75% of the values were 'United-States', which reduced variability. <br>
marital-status, race, relationship: Removed to simplify the dataset and focus on more relevant features. <br>
education: Removed as there was a numeric equivalent (education-num) that provided comparable information, making the object-type education redundant. <br>

# <li> Handle Missing Values

Replaced all '?' values in the occupation and workclass features with null. <br>
Dropped rows with null values in the occupation feature and filled remaining null values with the mode of the workclass feature. <br>

# <li> Scaling Numerical Data

Applied feature scaling to all numerical features to ensure consistency and improve model performance. <br>
Imported necessary functions from scikit-learn (in this case: MinMaxScaler)<br>
Applied the Min Max scaling method to all numerical features in the dataset to standardize their range and ensure consistent input for subsequent modeling.

# <li> Encoding Categorical Columns

Encoded all categorical features to convert them into a format suitable for machine learning models. <br>
For example Lable Encoding was done on the target ie: Salary in this case <br>
The rest of the categorical features were encoded using one hot encoding <br>

# <li> Outlier Treatment

Addressed outliers to improve the quality of the data and the performance of any models using this dataset. <br>
The numerical features were scaled earlier in order to reduce the number of outliers. The remainig outliers were treated using this technique 
