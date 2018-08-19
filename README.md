# 100 days of ML

**Day 1: Data Preprocessing:**
   - [x] Importing the libraries
   - [x] Handling missing values in the data.
     There is no good way to deal with missing data
     - Solutions:
       - Remove all rows with null values (Worst possible solution).
       - Replacing missing value with the mean for that column using the [Imputer](http://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.Imputer.html) class from `sklearn.preprocessing`.
       
          ```
          from sklearn.preprocessing import Imputer
          imputer = Imputer(axis = 0, missing_values = 'NaN', strategy = 'mean')
          imputer = imputer.fit_transform(X[:, *columns to impute*])
          ```
![alt text](https://github.com/adityakk29/100_days_of_ML/blob/master/Images/1%20_RA3mCS30Pr0vUxbp25Yxw.png)
[Source](https://towardsdatascience.com/how-to-handle-missing-data-8646b18db0d4) for the image
