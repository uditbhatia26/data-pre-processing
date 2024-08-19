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
Dropped rows with null values in the occupation feature and filled remaining null values with the mode of that feature. <br>

# <li> Scaling Numerical Data

Applied scaling to all numerical features to ensure consistency and improve model performance.

# <li> Encoding Categorical Columns

Encoded all categorical features to convert them into a format suitable for machine learning models.

# <li> Outlier Treatment

Addressed outliers to improve the quality of the data and the performance of any models using this dataset.
