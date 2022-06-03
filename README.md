# Linear Regression Model for Bike Sharing Rided Demand Prediction and Inferences

A bike-sharing system is a service in which bikes are made available for shared use to individuals on a short term basis for a price or free. Many bike share systems allow people to borrow a bike from a "dock" which is usually computer-controlled wherein the user enters the payment information, and the system unlocks it. This bike can then be returned to another dock belonging to the same system.

Compnay wants to understand the factors on which the demand for these shared bikes depends. Specifically, they want to understand the factors affecting the demand for these shared bikes in the American market.

The company wants to know:

*   Which variables are significant in predicting the demand for shared bikes.
*   How well those variables describe the bike demands
     
## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)

## General Information
Required to model the demand for shared bikes with the available independent variables. It will be used by the management to understand how exactly the demands vary with different features. They can accordingly manipulate the business strategy to meet the demand levels and meet the customer's expectations. Further, the model will be a good way for management to understand the demand dynamics of a new market. 

Bike Sharing dataset [here](https://github.com/bhogasena/BikeSharingDemad/blob/main/day.csv) and Data dictionary [here](https://github.com/bhogasena/BikeSharingDemad/blob/main/Data_Dictionary.txt).

## Conclusions
- Below are the top3 Significant variables which drivers the demand for Bike Share Rides.
      Feature         Co-efficient
       temp             0.5499
    weathersit_3       -0.2880
        yr              0.2331

- A unit increase in temp variable casues the bike share rides count increase by 0.5499 units
- A unit increase in yr variable casues the bike share rides count increase by 0.2331 units
- A unit increase in weathersit3(Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds variable casues the bike share rides count decrease by 0.2880 units

- Our model has R2-Score of 0.836 with train data and with test data predictions we got 0.796 which is good.
- Error terms are almost normally distrbuted with mean 0- this is one of the assumption for linear regression model
- There is no multicollinearity in our model as VIFs are less than 5
-
                            OLS Regression Results                            
==============================================================================
Dep. Variable:                    cnt   R-squared:                       0.836
Model:                            OLS   Adj. R-squared:                  0.832
Method:                 Least Squares   F-statistic:                     254.0
Date:                Fri, 03 Jun 2022   Prob (F-statistic):          1.47e-188
Time:                        02:01:19   Log-Likelihood:                 499.18
No. Observations:                 510   AIC:                            -976.4
Df Residuals:                     499   BIC:                            -929.8
Df Model:                          10                                         
Covariance Type:            nonrobust                                         
===================================================================================
                      coef    std err          t      P>|t|      [0.025      0.975]
-----------------------------------------------------------------------------------
const               0.0753      0.019      4.051      0.000       0.039       0.112
yr                  0.2331      0.008     28.382      0.000       0.217       0.249
workingday          0.0563      0.011      5.048      0.000       0.034       0.078
temp                0.5499      0.020     27.885      0.000       0.511       0.589
windspeed          -0.1552      0.025     -6.201      0.000      -0.204      -0.106
isSummer            0.0874      0.010      8.481      0.000       0.067       0.108
isWinter            0.1318      0.010     12.760      0.000       0.112       0.152
Month_9             0.0972      0.016      6.181      0.000       0.066       0.128
Mist               -0.0813      0.009     -9.292      0.000      -0.099      -0.064
Light_Snow_Rain    -0.2880      0.025    -11.659      0.000      -0.337      -0.239
Weekday_6           0.0677      0.014      4.710      0.000       0.039       0.096
==============================================================================
Omnibus:                       68.959   Durbin-Watson:                   2.080
Prob(Omnibus):                  0.000   Jarque-Bera (JB):              153.793
Skew:                          -0.731   Prob(JB):                     4.02e-34
Kurtosis:                       5.258   Cond. No.                         11.6
==============================================================================


        features   VIF
2             temp  4.76
1       workingday  4.04
3        windspeed  3.43
0               yr  2.02
9        Weekday_6  1.69
4         isSummer  1.57
7             Mist  1.53
5         isWinter  1.40
6          Month_9  1.20
8  Light_Snow_Rain  1.08


## Technologies Used
- numpy - version 1.21.6
- matplotlib - version 3.2.2
- seaborn - version 0.11.2
- plotly - version 5.5.0
- statsmodels - version 0.10.2
- sklearn - version 1.0.2

## Contact
Created by [@bhogasena] - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
