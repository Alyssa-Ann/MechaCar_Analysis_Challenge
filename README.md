# MechaCar Statistical Analysis

## Overview of Project

1. Load, clean up, and reshape datasets using tidyverse in R.
2. Visualize datasets with basic plots such as line, bar, and scatter plots using ggplot2.
3. Generate and interpret more complex plots such as boxplots and heatmaps using ggplot2.
4. Plot and identify distribution characteristics of a given dataset.
5. Formulate null and alternative hypothesis tests for a given data problem.
6. Implement and evaluate simple linear regression and multiple linear regression models for a given dataset.
7. Implement and evaluate the one-sample t-Tests, two-sample t-Tests, and analysis of variance (ANOVA) models for a given dataset.
8. Implement and evaluate a chi-squared test for a given dataset.
9. Identify key characteristics of A/B and A/A testing.
10. Determine the most appropriate statistical test for a given hypothesis and dataset.

In addition to

1. Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
2. Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
3. Run t-tests to determine if the manufacturing lots are statistically different from the mean population


Software: R, RStudio, dplyr library, VSCode

## Purpose

The purpose of this project is to create a comprehensive showing of statistics that AutosRU can use to study its new prototype, MechaCar. The project is experiencing production issues that is holding back the finalization of the project. The team will take the given data set and analysize it to find the variables used to predict the mpg of MechaCar prototypes. They will then breakdown the summary statistics on the PSI of the suspension coils of the cars. Finally, t-tests wll be run to determine how the varying lots differ from one another. 

## Results

### Linear Regression to Predict MPG 

A Linear Regression was performed on the dataset to get the coefficients below from several variables. 

![Deliverable_1_Linear_Regression_Model](https://user-images.githubusercontent.com/88064181/142276829-53d1f731-678a-446d-a08c-f73c4790f898.png)


Summary statistics were defined, as seen below, to determine any variance in the data set and determine the quality of the data in the set. 


![Deliverable_1_Summary_Statistics](https://user-images.githubusercontent.com/88064181/142276852-05fc12d5-1e77-455f-95e1-c4143ab4fa85.png)

As seen above, vehicle weight, spoiler angle, and AWD are the variables that provide a non-random amount of variance to the mpg values in the dataset. Since the p-value is less than zero, and the variables show coefficients that are close, but not zero, it can be deterined that the slope of the linear model is not considered to be zero. This linear model predicts the mpg of Mechacar prototypes with about a 71% efficiency. This is determined by the R square value. So 71% of the time, the predictions of the mpg will be correct. This is not as accurate as a major car producing corporation would want.


### Summary Statistics on Suspension Coils 

Below is the result of a summary statistic performed on all manufacturing lots with data pulled from the suspension coil csv. 

![Deliverble_2_Summary_Statistics_all_lots](https://user-images.githubusercontent.com/88064181/142276882-531b6ac1-ff76-4a7f-bc83-42f85ce6149a.png)


A summary of statistics was then performed on each individual lot to ensure they are within an acceptable variance. 

![Deliverable_2_Summary_statistics_individual_lots](https://user-images.githubusercontent.com/88064181/142276889-bfdd2b32-5b3d-4342-8081-02181e97b1d3.png)


Lots 1 and 2 show very similar variances. Lot3, however, has a smaller mean, but a bigger variance and standard deviation. The design specifications signify that the MechaCar suspension coils must not exceed 100 PSI. Lots 1 and 2 fell well within this variance. Lot 3 shows a variance of 170 PSI, which does not meet design specifications. 


### T-Tests on Suspension Coils 

The following statistics show T-tests done for a summary of all the manufacturing lots, as well as T-tests done for each individual lot. 

![Deliverable_3_t-test_all_lots](https://user-images.githubusercontent.com/88064181/142276911-e56ecebc-3bc3-46ca-a35c-0b895de5b17d.png)

![Deliverable_3_t-test_lot_1](https://user-images.githubusercontent.com/88064181/142276915-5a86a83d-b862-48fb-8975-c5173e315d16.png)

![Deliverable_3_t-test_lot_2](https://user-images.githubusercontent.com/88064181/142276923-2f776569-cbd4-4c3a-813d-2fa7179d7d89.png)

![Deliverable_3_t-test_lot_3](https://user-images.githubusercontent.com/88064181/142276938-a80f067c-ecd7-47b8-9ffb-31e6b6dade98.png)


With the t-tests performed, one can see that all the lots averaged a P-value of 1. Lot 1 saw the most significant different to the standard 1500 PSI. Based on this data, one can see the major impacting variables on mpg are the car weight, the spoiler angle, and the AWD capability. To improve the overall mpg for Mechacar, designers would have to consider these variables. 

## MechaCar vs Competition

If one were to compare MechaCar to its competition, they should consider testing consumer interests such as cost, fuel efficiency, and safety ratings. This hits on key consumer indicators of initial and long term costs and safety. The null hypothesis would be that is the p value is greater than 0.05 in these categories, the MechaCar will have a similar performance, but if the p value is less than 0.05, the MechaCar will perform differently in a significant way (alternative hypothesis). This theory could be testing using multiple linear regression sumaries to show how the variables impact these new considerations. One would need new data on Mechacar, specifically a random sampling of Mechacars alsong with the same number of random sampling of a competitor's care with the cost, fuel efficiency, and safety data to run these statistics. 

