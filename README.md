# EDA

Exploratory data analysis is basically to analyse the data, aggregate the findings and present it to stakeholders. If the findings are convincing enough then the next step would be to develop a model around the data etc. Exploratory data analysis involves the following steps:

1. Data Cleaning - Here we may have to perform Null value analysis and apply mean, mode and median. For numerical data we have to use mean, median and for categorical variable we have to use mode. Post null value imputation we have to check the data for invalid data and check for outliers.
2. Data Analysis - For categorical variables we can use univariate, bivariate and multivariate analysis. For numerical values, with one attribute we can get some summary analysis and for more than one attribute we can run correlation analysis between attributes.
3. Derived Metrics - Create new columns for example Age as age is a continuous variable hence it is difficult to figure out any details so better to create bins for example 0-20, 21-40 and so on.

# End to End steps for EDA
1. Load all the required python libaries such as pandas, numpy, matplotlib.
2. Load the data using pandas **read_csv** method
3. View the data using pandas **head** and **tail** methods
4. Use pandas method such as **shape** to get an overall idea about the number of columns and rows, **columns.values** will give an idea about all the various columns, **dtypes** will give an idea about data types associated with each column
5. Next use the **describe** method to describe the data and get details such as mean, median, 25%, 50%, 75% etc and make a note of some of these findings
6. Next use **value_counts** on dependent variable to get an idea about the percentage of success and failure
7. Next use the **info** method to check if there are any null values in the data.
8. If there are missing values then the following approach can be used
   * If there are very few missing values then replace the missing values with mean, median or mode
   * If the missing values are quite high then remove the complete column
9. Now the next step is to analyze the values and see if anyone of them requires the data type to be changed for example changing a string column to integer
10. Next step is to check if we need to convert some of the data into bins, for example some variables such as age can be grouped into bins as it may be too much to create individual bars for each age
11. We can also remove some columns which actually will not add any value into our investigation for example customerId, customer name may not add any value
12. This completes the **Data Cleaning Process**
13. Now the next step is to run Univariate Analysis, basically for every other variable try to get an idea. For this we can use **countplot** and plot the graphs for all the categorical variables against dependent variable
14. Now we can run outlier analysis to figure out what percentage of records are outlier, typically if the outlier are more than 0.3% then it means that the distribution is not a Normal distribution hence it is worth to check the distribution which can be done by plotting a KDEPlot. A KDEPlot would give details about skeweness of the data. And then we can apply startegies such as log, double log, inverse etc to reduce the skewness of the data.
15. Now the next step is to run numerical analysis for variables which are numerical in nature, for numerical analysis we also have to make couple of changes
    * We have to transform dependent variable into numerical
    * Apply one-hot encoding to create dummy variables
16. Now we can plot a correlation bar plot between dependent variable and all the predictor or independent variables. This will give us lot more insight about positive as well negative cases for example why a customer is churning and why a customer is not churning.
17. Next we can plot a heatmap between all the variables, this will give us detail of correlation across all variables. **please note point #16 talks about correlation between dependent and independent variable however heatmap is to get correlation details between all the variables and not just predictor and dependent variables**
18. Next we will apply Bivariate, trivariate and multivariate analysis to get more insights on the data for example.
