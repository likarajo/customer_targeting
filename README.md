# Customer Targeting

Predicting whether a customer will be interested in an advertisement based on customer Ad-Clicks data.

* To predict if a user is likely to click on an advertisement.

## Background

Through ***Internet marketing***, companies advertise their products on websites and social media platforms. However, ***targeting the right audience*** is very important as it is very costly to display the advertisement to the audience.

## Dependencies

* Pandas
* Numpy
* Matplotlib
* Seaborn
* Scikit-learn

## Dataset

Advertising data of a marketing agency: https://www.kaggle.com/fayomi/advertising<br>
Saved in: *data/advertising.csv*

Columns:

* Daily Time Spent on Site (in minutes)
* Age
* Area Income
* Daily Internet Usage
* Ad Topic Line
* City
* Male: 1 for male, 0 for female
* Country
* Timestamp: exact time when a user clicked on the advertisement
* Clicked on Ad: 1 if yes, 0 if no

## Data Analysis

* 1000 records
* No missing values in any column

### Nunmeric variable analysis

* Significant difference between the smallest and highest Area Income
  * Users belong to different social classes
* Daily Time Spent on Site ranges from 32 to 91 minutes with average of 65 minutes in one session
  * The website is popular
* Average age of user is 36, ranging from 19 to 61 years old
  * Users are adult users
* 48% male users
  * Both men and women visit the site almost equally

### Distribution of *Age*

* Age has normal distribution
* Helpful for effective data processing

### Interdependence of *Age* and *Time Spent on Site*

* Younger users aged 20 to 40 spend more time on the site.
* Users aged 20 to 40 can be target users

### Interdependence of *Time Spent on Site* and *Daily Internet Usage*

* Users who spend more time on the internet also spend more time on the site.

### Site usage Trends

Using scatter matrix on numeric variables

* Young adults spend more time on the site
* Higher income users spend more time on the site

### Categorical variable analysis

* All the *Ad Topic Line* values are unique: omitted from further analysis
* There are 969 unique values for *City* within 1000 records: omitted from further analysis
* There are 237 unique countries: omitted from further analysis

## Data Preprocessing

### Timestamp category analysis

* Break timestamp into smaller units for analysis
* Remove *Ad Topic Line*, *City*, *Country* columns
* Prepare features and labels
* Split dataset into test and training set

## Create, train and test models

* Algorithms:
  * Logistics Regression
  * Decision Tree Classifier
* Evaluation:
  * Accuracy score
  * Confusion matrix

## Conclusion

* Logistic regression accuracy: 91%, Decision tree accuracy: 92%
* Decsion tree has slighlty better performance



