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
- Below are the top5 Significant variables which drivers the demand for Bike Share Rides.
      Feature         Co-efficient
        temp             0.5582
        hum             -0.2911
         yr              0.2268
      windspeed         -0.2047
      weathersit3       -0.1964

- A unit increase in temp variable casues the bike share rides count increase by 0.5582 units
- A unit increase in hum variable casues the bike share rides count decrease by 0.2911 units
- A unit increase in yr variable casues the bike share rides count increase by 0.2268 units
- A unit increase in windspeed variable casues the bike share rides count decrease by 0.2047 units
- A unit increase in weathersit3(Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds variable casues the bike share rides count - decrease by 0.1964 units

- Out final Model with RFE (Recursive Feature Elimination) has R2-Score: 0.843, F-Static: 228.0, Prob (F-statistic):          2.03e-186
- R2- Score and test data is 0.810 which is good.
- Error terms are almost normally distrbuted with mean 0- this is one of the assumption for linear regression model
- There is no multicollinearity in our model as VIFs are less.

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
