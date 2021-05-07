# PanasonicCustomerReviewStrategy
Analysis of user rating categories for better sales of the Panasonic's LCD TVs

Based on the case study of the Panasonic company and that data provided in the excel sheet the following deductions were made.
1.	On using a pivot table on the dataset provided we arrive at the below findings. (After eliminating the categorical variables like Motion Rate, Pixel, Screen size as there are dummies already created for them.) 
 
![Screenshot](/Images/PivotTable.png?raw=true "Pivot Table")

From the pivot table and the respective heatmap, we can see that Panasonic has higher points for the user rating categories of Life Span, Video Quality and Ease of Set up.
This can be further corroborated by ranking these user rating categories with respect to the manufacturers.
 
![Screenshot](/Images/RankTable.png?raw=true "Rank Table")

After running the linear regression for the above model with the target variable being Yearly Units Sold in US, we can see the below chart.
![Screenshot](/Images/Histogram.png?raw=true "Histogram")
  
While investigating further, we derive the variable coefficients of the user rating categories and we get the below details.
 
![Screenshot](/Images/VariableCoefficient1.png?raw=true "VC1")

Video Quality, Number of Features, Ease of Setup have higher positive coefficient indicating their maximum impact on the target variable.
Hence, as a recommendation to the Panasonic team, we suggest investing on the user rating categories in the below order which would be in the best interest of the company.
1.	Video Quality
2.	Number of Features
3.	Ease of Setup
4.	Appearance
5.	Life Span
6.	Sound Quality


Also,we have created the Price Diff variable in the dataset which will help us in getting the difference between the focal product’s price and average price for that segment. 
Average price for that segment is calculated using a groupby function involving the variables Motion Rate, Pixel and Screen Size.
On running the linear regression model on this dataset with the target variable being Yearly Units Sold in US, we get the below variable coefficients.
 
![Screenshot](/Images/VariableCoefficient2.png?raw=true "VC2")



# To conclude, below are the following points that can be drawn from the above model.
The order of the user rating categories is the same even after including the Price Diff variable. So, Panasonic should invest in the same order.
But there are significant differences in the coefficient values. And the negative coefficient of the Price Diff indicates that for every unit increase in the price difference the company sells 3 units lesser than the actual value. 




