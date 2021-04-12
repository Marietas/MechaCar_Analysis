# MechaCar_Analysis

## Overview

This report aims to provide insightful information to assist the manufacturing team to evaluate production data for a Company in the automotive industry.

The following analyses and tasks were performed:

- Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
- Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
- Run t-tests to determine if the manufacturing lots are statistically different from the mean population
- Design a statistical study to compare the vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. 

### Resources

Datasets: MechaCar_mpg.csv, Suspension_Coil.csv
Software: RStudio 1.4.1106

## Summary Results

### Linear Regression to Predict MPG

The MechaCar dataset was considered to identify the ideal Vehicle performance and several metrics were taken into consideration. For each car, different measurements were obtained, including length, weight, spoiler angle, drivetrain, and ground clearance. Thus, applying R skills, I could build a linear model that estimates MechaCar prototype mpg based on the different variables provided on MechaCar dataset file.


Fig. 1 summarises these data.

![](https://github.com/Marietas/MechaCar_Analysis/blob/main/Resources/Images/fig1.PNG)

Each Pr(>|t|) value in the summary output reflects the probability that each coefficient impacts a random amount of variance to the linear model. Also, the vehicle length and ground clearance (and Intercept) provide a non-random sum of variation to the linear model of mpg.

Per the outcome of the analysis, the multi linear model is:

***mpg = 6.267 * vehicle_length + 1.245e-3 *  vehicle_weight + 6.877e-2 * spoiler_angle + 3.546 * ground_clearance -3.411* AWD – 1.040e2***

As a result, the linear model's gradient is not considered to be zero.

Since the R-square is 0.7149, differences in vehicle length, weight, spoiler angle, drivetrain, and ground clearance will explain 71.49 percent of the variability in mpg. This linear model can be considered reasonably effective for predicting mpg of MechaCar prototypes.

### Summary Statistics on Suspension Coils

According to the design requirements, the MechaCar suspension coils must not have a deviation of more than 100 pounds per square inch.

Fig. 2 shows all manufacturing lots.

