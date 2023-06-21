# Car-Price-Prediction-Report
CAR PRICE PREDICTION USING MULTIPLE LINEAR REGRESSION ANALYSIS IN EXCEL

INTRODUCTION

The analysis aims at identifying significant variables required to predict the price of a car and to describe how well the variables describe the price of the car. 

UNDERSTANDING DATA STRUCTURE

The dataset used for this analysis with a 250 sample size was gotten from Kaggle, containing car prices and attributes related to the predictive analysis. The dataset contained 13 numerical variables and 10 categorical variables.

By understanding the data structure and the variables involved, correlation analysis was further done to explore the relationships between these car attributes and the prices. This analysis will provide insights into the factors that may influence car prices and help understand the dynamics of the car market.

DATA CLEANING AND EXPLORATION

•	Incorrect spellings; the car names with incorrect spellings were corrected.

•	The Car brands were extracted from the car name column and converted to the proper text format.

•	The prices of the car were adjusted to the right format.

DESCRIPTIVE STATISTICS OF THE CAR PRICES
	
Summary statistics table
	
Mean	| 13276.71

Standard Error	| 557.97

Median	| 10295.00

Mode	| 16500.00

Standard Deviation| 7988.85

Sample Variance| 63821761.58

Kurtosis| 3.05

Skewness| 1.78

Range| 40282.00

Count| 205.00


CORRELATION AND MULTIPLE REGRESSION ANALYSIS

NUMERICAL VARIABLES

Correlation result summary

Independent variables

Wheelbase| 0.58| Moderate Positive correlation

Car length| 0.68| Moderate Positive correlation

Car width| 0.76| Strong Positive correlation

Car height| 0.12| Weak Positive correlation

Curb weight| 0.84| Strong Positive correlation

Engine size| 0.87| Strong Positive correlation

Bore ratio| 0.55| Moderate Positive correlation

Stroke| 0.08| Weak Positive correlation

Compression ratio| 0.07| Weak Positive correlation

Horsepower| 0.81| Strong Positive correlation

Peak rpm| -0.09| Weak Negative correlation

City mpg| -0.69| Weak Negative correlation

Highway mpg|-0.70| Weak Negative correlation

Significant Numerical Variables based on the correlation analysis

1.	Curb weight
2.	
3.	Engine Size
4.	
5.	Horsepower
   
Calculating Variance Inflation Factor (VIF) of each variable

•	Engine size; 4.77

•	Horse power; 3.02

•	Curb weight; 3.77

To address multicollinearity, the engine size which has high value of VIF (approximately 5) was removed.

CATEGORICAL VARIABLES

They were converted into dummy variables, and regression analysis was performed.

Regression Analysis Result for each variable

#Car Name

this regression analysis was performed after removing variables with evidence of possible multicollinearity and presence of extreme values.

Interpretation from regression analysis;

38% of the variation in the price of a car is dependent on the car model and the P-values show that the variables are statistically significant. However, the higher standard error associated with the coefficient indicates that the estimate not precise and therefore not reliable which reduces the confidence that we can have in the estimate. 

#Drive Wheel

Interpretation from regression analysis; 

the adjusted R square indicates that 41% of the variance in the price of the car can be explained by the drive wheel. The variable "rwd" (Rear-Wheel Drive) has a low p-value of 0.00, indicating a statistically significant relationship with car prices. Including this variable in the model would be beneficial as it shows a strong association with the target variable. “fwd” on the other hand is not statistically significant and may not be needed to improve model predictive accuracy.

#Cylinder Number

Interpretation from regression analysis; 

the adjusted R square indicates that 63% of variance in the price of car can be explained by the cylinder number. The variables "four," "six," "five," "three," and "two" have low p-values (all less than 0.05), suggesting statistically significant relationships with car prices. Including these variables in the model would be relevant as they provide information about the engine's cylinder configuration, which can influence car prices.

#Engine Type

Interpretation; the adjusted R square indicates that 22% of variance in the price of car can be explained by the drive wheel. The variables "ohcf," "L," "ohc," and "rotor" have low p-values (all less than 0.05), indicating statistically significant relationships with car prices. Including these variables in the model would be valuable as they represent different engine types, which can impact car prices.

#Car Body
 
Interpretation;

the adjusted R square indicates that 14% of the variance in the price of the car can be explained by the drive wheel. The p-values associated with the rwd indicate that it is statistically significant but that of fwd indicates that it is not statistically significant and may not provide meaningful insights or improve model predictive accuracy. 

#Door Number

Interpretation; the adjusted R square of 0% shows that the price of car cannot be explained by the door number. The p-values associated with the door number (four) is very high which indicates that it is not statistically significant and including it in the model may not be necessary as it does not provide strong evidence of influencing car price.

#Aspiration

Interpretation;

The p-value indicates that the analysis is statistically significant but the adjusted R square indicates that the variable contributes 3.0% to the variance in the price of the car and so including this to the predictive model may not contribute valuable information or enhance the model's performance.

#Engine Location

Interpretation; 

The R square indicates that 11% of the variance in the price of the car can be explained by the engine location. The p-values show that the analysis is statistically significant. This variable would however not be included in the model due to the low coefficient of determination.

#Fuel Type

Interpretation; the adjusted R square indicates that 10% of the variance in the price of the car can be explained by the fuel type. The p-values indicate that it is not statistically significant (above the threshold of 0.05) and including it in the model may not provide meaningful insights or improve model predictive accuracy.

#Fuel System

Interpretation;

Adjusted R square indicates that 36% of the variance in the price of the car can be explained by the fuel system. However, none of the fuel system variables (mpfi, 2bbl, 1bbl, Spdi, 4bbl, Idi, mfi) show statistically significant relationships with car prices, as their respective p-values are above the typical threshold of 0.05. Including these variables in the model may not contribute significant predictive power and could introduce noise or unnecessary complexity. 

Categorical variables with higher significance after regression analysis

1.	Cylinder Number
2.	
3.	Engine type
4.	
5.	Drive wheel
   
Adjusted R square indicated that 78% of the variance in the price of the car can be explained by these categorical variables. The p-values associated with all the variables show evidence of statistical significance (below 0.05)

Multiple Regression analysis on the categorical and numerical variables indicate 94% of the variance in car price is explained by the model. 

Calculating the VIF of each of the variables to check for multicollinearity
Six; 6.66 

five; 5.47

Three; 1.92 

rwd; 2.37   

Curb weight; 4.5   

Horsepower; 3.6

Dohc; 2.72  

Ohcf; 3.43 

L; 4.21   

Ohc; 8.74      

Rotor; 2.13

Removing six, five, ohc due to the high VIF values

After the regression, ohcf and rotor was removed because the P-values associated with them shows that they are not statistically significant.

Interpretation;

The multiple R-value 0.89 shows that there is a strong relationship between the variables and the car prices. The R square shows that 79% of variance in the dependent variable is explained by the independent variables. The P-values associated with the variables shows that they are statistically significant.

Linear Regression Model Equation

Dependent variable (Price of car) = -16142.9 + 66.41401 * horsepower + -3097.06 * dohc + -5156.62 * L + 10413.67 * three + 2345.715 * rwd + 8.635081 * curb weight

Testing the Model Using Prediction

Expected car price; 13495
Engine Type; dohc

Horse Power; 111

Cylinder number; four

Curb weight; 2548

Drive wheel; rwd

Using the regression model equation;

-16142.9 + 66.41401 * horsepower + -3097.06 * dohc + -5156.62 * L + 10413.67 * three + 2345.715 * rwd + 8.635081 * curb weight

Y (price of the car) = -16142.9 + 66.41401 * 111 + -3097.06 * 1 + -5156.62 *0 + 10413.67 * 0 + 2345.715 * 1 + 8.635081 * 2548

Predicted price: 12,479.9

Actual price: 10,661.05 (79% of the expected price)

Deviation: The predicted price is 1,818.85 higher than the actual price.

Assessment: Based on this evaluation, the prediction is slightly overestimating the actual price.

LIMITATION

The presence of heteroscedasticity in the data, possibly due to the small sample size pf 205 observations, may have impacted the accuracy of the correlation analysis. The small sample size also limits the generalizability of the findings. Future research with larger samples and robust statistical techniques is recommended.

CONCLUSION

The regression model developed explains approximately 79% of the variance in car prices, 21% can is dependent on other unknown variables. However, further improvements or alternative modelling approaches can be considered. 
Overall, this analysis provides insights into the significant variables and their relationships with car prices, helping to understand the dynamics of the car market and providing a foundation for predicting car prices using multiple linear regression analysis.  

RECOMMENDATION

Future research in car price prediction should focus on enhancing the robustness and generalizability of findings. This can be achieved simply by increasing the sample size to improve statistical power and enable broader generalization. Additionally, employing advanced statistical techniques specifically designed to address heteroscedasticity would enhance the accuracy of the analysis.
