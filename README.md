# MechaCar Statistical Analysis
Challenge 15 for Butler Data Science


## Linear Regression to Predict MPG

**Model:** 

## mpg =  (6.267)**vehicle_length** + (0.0012)**vehicle_weight** + (0.0688)**spoiler_angle** + (3.546)**ground_clearance** + (-3.411)**AWD** + (-104.0)
				

**Statistical Summary:** 
![lm](https://github.com/coxjack/MechaCar_Statistical_Analysis/blob/main/Additional%20supporting%20images/MechaCar_deliv1(linear%20regression).png)

From the above output we can see that:

1. The **vehicle length**, and **vehicle ground clearance** provide non-random amount of variance to the mpg values in the dataset -- the vehicle length and vehicle ground clearance have a significant impact on miles per gallon on the MechaCar prototype.

2. The p-Value, 5.35e-11, is much smaller than the assumed significance level of 0.05%. This indicates there is sufficient evidence to reject our null hypothesis, also indicating that the slope is not zero.


3.  This linear model has an r-squared value of 0.7149, meaning that approximately 71% of all mpg predictions will be determined by this linear model. Using this figure we can say that this regression model does predict mpg of MechaCar prototypes effectively. 


## Summary Statistics on Suspension Coils


Total Summary (all manufacturing lots):

![total](https://github.com/coxjack/MechaCar_Statistical_Analysis/blob/main/Additional%20supporting%20images/MechaCar_deliv2(total_Summary).png)

Lot summary (grouped lots):

![lots](https://github.com/coxjack/MechaCar_Statistical_Analysis/blob/main/Additional%20supporting%20images/MechCar_deliv2(lot_summary).png)

When looking at the entire population of the manufacturing lots, the variance of the suspension coils is 62.29 PSI. This is significantly below the 100 PSI variance threshold.  

When breaking down the lots into groups -- Lot 1 has a variance of .98 and Lot 2 has a variance of 7.47 these are showing very little variance and definitely meet the variance requirement (100 PSI variance). Lot 3 though, has a PSI variance of 170.29, this lot is disproportionately skewing the overall variance for the entire dataset.  


## T-Tests on Suspension Coils


Summary of the t-test results across all manufacturing lots
![alllots](https://github.com/coxjack/MechaCar_Statistical_Analysis/blob/main/Additional%20supporting%20images/MechaCar_deliv3(t-testAll).png)

The true mean of the sample is 1498.78. Additionally the p-Value is 0.06, which is higher than the common significance level of 0.05, meaning there is NOT enough evidence to support rejecting the null hypothesis. We can determine the mean of all the manufacturing lots is statistically similar to the presumed population mean of 1500.

Summary of the t-test results for each lot
![t-testlots](https://github.com/coxjack/MechaCar_Statistical_Analysis/blob/main/Additional%20supporting%20images/MechaCar_deliv3(t-testlots).png)

1. Lot 1 true sample mean of 1500 with a p-Value of 1, meaning we cannot reject null hypothesis that there is no statistical difference between the observed sample mean and the presumed population mean (1500).
2. Lot 2 has the same outcome with a sample mean of 1500.02, and a p-Value of 0.61; the null hypothesis cannot be rejected, and the sample mean and the population mean of 1500 are statistically similar.
3. Lot 3 the sample mean is 1496.14 and the p-Value is 0.04, which is lower than the common significance level of 0.05.  This means we need to reject the null hypothesis that this sample mean and the presumed population mean are not statistically different.


## Study Design: MechaCar vs Competition

This study would involve collecting data on MechaCar and its comparable models across several different manufacturers over the past 5 years.

#### Metrics
Collecting data for comparable models from major manufacturers for past 5 years for the following metrics:

*  Current Selling Price (Selling)  
*  Safety Rating
*  Resale Value
*  Engine Type (Electric, Hybrid, Gas)
*  Average Annual Maintenance Cost
*  MPG

#### Hypothesis: Null and Alternative

 * Null Hypothesis: MechaCar is priced correctly based on its performance of key factors of its competition.
 * Alternative Hypothesis: MechaCar is NOT priced correctly based on performance of key factors of its competition.
 
#### Statistical Tests
Similarly to this challenge a multiple linear regression should be used to determine the factors that have the highest correlation/predictability with the list selling price and which combination of the variables has the greatest impact on selling price
