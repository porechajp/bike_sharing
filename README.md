# Bike Sharing Linear Regression Assignment

A bike-sharing system is a service in which bikes are made available for shared use to individuals on a short term basis for a price or free. Many bike share systems allow people to borrow a bike from a "dock" which is usually computer-controlled wherein the user enters the payment information, and the system unlocks it. This bike can then be returned to another dock belonging to the same system.

In this assignment, we are building the linear regerssion model to predict the demand for shared bikes.

During the process it is determined, which variables are significant in predicting the demand for shared bikes, and how well those variables describe the bike demands.

The provided dataset contains the past usage of two years, various meteorological attributes (weather, temperature, windspeed, seasons, etc...), work / weekend days, etc...  


## Table of Contents
- [Bike Sharing Linear Regression Assignment](#bike-sharing-linear-regression-assignment)
  - [Table of Contents](#table-of-contents)
  - [General Information](#general-information)
  - [Conclusions](#conclusions)
  - [Technologies Used](#technologies-used)
  - [Acknowledgements](#acknowledgements)
  - [Contact](#contact)

<!-- You can include any other section that is pertinent to your problem -->

## General Information

Following steps are performed,

* EDA
  * Data Cleanup
  * Data Preparation
  * Data Visualization

* Model Training
  * Model Training using meteorological attributes
    * LR Model B is the finalized model
  * Model Training using months
* Exercise Summary

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions

After analyzing the data and building multiple linear regression models using various combinations of independent variables, we have found the model which is using the least no. of independent variables (i.e. 6) and has  R² and adjusted R² more than 0.8.

The R² score on predicted value based on test data set is 0.79

Following are the summary points,

* LR Model B is the finalized model. 
* It uses : ```yr, atemp, s_spring, w_light_snow_rain, w_misty, windspeed ```
* The coeffecients of these independent variables are,
```
const                0.310191
yr                   0.236811
atemp                0.388947
s_spring            -0.152877
w_light_snow_rain   -0.267825
w_misty             -0.074380
windspeed           -0.1
```

* There is an intercept of 0.310191
* It is important to note that year and "feels-like" temperature have positive correlation with bike rental, and that correlates to the uptick in rentals in year 2019 (which is represent as 1 in the dataset) compared to 2018 (represented as 0)
    * Higher the temperature, people would like to rent more bikes because it might be a conducive weather for outdoor activities.
* The weather conditions like raining, snowing, and windy would usually discourage the rental activities.
* Except spring no other seasons have any major impact on outcome variable (i.e. cnt).

Based on data, the regression model is **better off** to be relying on temperature, weather, season and year data compared to months and year variables.42822


## Technologies Used

- Python 3.10.9
- Jupyterlab 3.6.3
- pandas 1.5.3
- seaborn 0.12.2
- scikit-learn 1.3.0
- statsmodels 0.14.0
- numpy 1.23.5
- matplotlib 3.7.0

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements

I referred [Investopedia](https://investopedia.com), Wikipedia, GeekForGeeks, AnalyticsVidya, StackExchange to learn and write the answers to subjective questions.


## Contact
Created by [Jatan Porecha](https://github.com/porechajp)

