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

![](https://github.com/Marietas/MechaCar_Analysis/blob/main/Resources/Images/Total%20summary%20coils.PNG)

With a global variation of 62.293 psi, the specifications are followed for all production lots.

Fig. 3 shows the summary for each manufacturing lot.

![](https://github.com/Marietas/MechaCar_Analysis/blob/main/Resources/Images/lot_summary_coils.PNG)

Lot 1 and Lot 2 are also under the specifications required, with variances of 0.979 and 7.469 psi, respectively. With a difference of 170.286 psi, Lot 3 is out of specification.

### T-Tests on Suspension Coils

Fig.4 shows T-Test of all manufacturing lots compared to the total population mean.

![](https://github.com/Marietas/MechaCar_Analysis/blob/main/Resources/Images/fig4.PNG)

Assuming our significance level is the standard 0.05 percent, our p-value of 0.0602 is above the significance threshold. As a result, there is insufficient data to ignore the null hypothesis, and the PSI for all production lots is statistically close to the population mean of 1498.78 psi.

Fig. 5 shows T-Tests of each manufacturing lot1 compared to the total population mean Lot1.

![](https://github.com/Marietas/MechaCar_Analysis/blob/main/Resources/Images/fig5.PNG)

Since the p-value is below the significance threshold of 0.05 percent, we can consider the hypothesis null and assume that the PSI around Lot 1 is statistically different from the population mean.

Fig. 6 T-test of each manufacturing lot2 compared to the total population mean Lot2.

![](https://github.com/Marietas/MechaCar_Analysis/blob/main/Resources/Images/fig6.PNG)

Fig. 7 T-Test of each manufacturing lot3 compared to the population mean Lot3.

![](https://github.com/Marietas/MechaCar_Analysis/blob/main/Resources/Images/fig7.PNG)

### Study Design: MechaCar vs Competition

We should explore the option to do a comparative analysis based on the following metrics to evaluate the efficiency of the MechaCar concept in relation to the competition vehicles:

-Fuel consumption 
-Level of security
-Time it takes to go from 0 to 60 Mph
-Breaking distance 
-The Engine Power
-Weight 
-Annual maintenance cost

Based on the metrics selected, the following hypothesis and statistic test can be considered:

The null hypothesis should be considered assuming that each performance metrics is statistically similar between the MechaCar prototype and all vehicles from the different manufacturers.

In this case, one of the tools that could be employed is the ANOVA test. We should consider the use  of this method  to compare the means of a continuous numerical variable across a number of groups.

In this way we can compare the means for each individual metric over the different manufacturers.

A dataset similar to MechaCar would be needed to perform the test. We could create a single data frame where we could gather the data from MechaCar vehicles and its competition, as well as the data coming from the ANOVA test. 
