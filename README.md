# 100 days of ML

**Day 1: Data Preprocessing:**
   - [x] Importing the libraries
   - [x] Handling missing values in the data.
     There is no good way to deal with missing data
     - Solutions:
       - Remove all rows with null values.
       - Replacing missing value with the mean for that column using the [Imputer](http://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.Imputer.html) class from `sklearn.preprocessing`.
       
          ```
          from sklearn.preprocessing import Imputer
          imputer = Imputer(axis = 0, missing_values = 'NaN', strategy = 'mean')
          imputer = imputer.fit_transform(X[:, *columns to impute*])
          ```
![alt text](https://github.com/adityakk29/100_days_of_ML/blob/master/Images/Data%20preprocessing.png)
[Source](https://towardsdatascience.com/how-to-handle-missing-data-8646b18db0d4) for the image


   - [x] Encoding categorical data.
      - What and Why?:
         - Columns with categorical data (e.g. names) cannot be used in ML models (since they are based on mathematical equations). So we need to encode these categorical data to numbers.
      - How:
         - Use [OneHotEncoder](http://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.OneHotEncoder.html) class from `sklearn.preprocessing`
         ```
         from sklearn.preprocesssing import OneHotEncoder
         oneHotEncoder_X = OneHotEncoder(categorical_features = [*index of column*])
         X = oneHotEncoder_X.fit_transform(X).toarray()
         ```