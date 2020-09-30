# Predicting Teenage Pregnancies in Charleston, SC and Baltimore, MD based on racial demography and household income 
## Background 
In my previous project, I noted what appeared to be an inverse relationship between household income and the teenage pregnancy rate in Charleston, SC and Baltimore, MD. However, I noted that the relationship between income and teenage pregnancy was less pronounced in Charleston; the lowest population tract by household income in Charleston had lower teenage birthrates than Baltimore's highest earning population tract. This discrepency led me to believe that other factors, like race, may affect the teenage pregnancy rates differently in both cities. With this information in mind, I hypothesized that race was a greater determinant of teenage pregnancy rates in Baltimore, due to its larger non-white population.

## Question
What is the relationship between a population tract's household income, percentage of non-white residents, and teenage pregnancy rate?

## Data Sources 
I derived all of my data from Opportunity Atlas. The data is categorized as follows:
- [Average household income Charleston](https://github.com/John-Frye/baltimore-charleston-regression-on-race-income-teen-pregnancy/blob/master/Charleston_Income_Data.xlsx): the average household income in a population tract in Charleston, SC
- [Average household income Baltimore](https://github.com/John-Frye/baltimore-charleston-regression-on-race-income-teen-pregnancy/blob/master/Baltimore_Income_Data.xlsx): the average household income in a population tract in Baltimore, MD
- [Teenage pregnancy rate Charleston](https://github.com/John-Frye/baltimore-charleston-regression-on-race-income-teen-pregnancy/blob/master/charleston_teen_pregnancy%20(1).xltx): the fraction of women in a population tract in Charleston, SC who gave birth between the ages of 13-19
- [Teenage pregnancy rate Baltimore](https://github.com/John-Frye/baltimore-charleston-regression-on-race-income-teen-pregnancy/blob/master/baltimore_teen_pregnancy.xls): the fraction of women in a population tract in Baltimore, MD who gave birth between the ages of 13-19
- [Fraction non-white Charleston](https://github.com/John-Frye/baltimore-charleston-regression-on-race-income-teen-pregnancy/blob/master/charleston_nonwhite_demography.xlsx): the percentage of a population tract in Charleston, SC that identifies as non-white
- [Fraction non-white Baltimore](https://github.com/John-Frye/baltimore-charleston-regression-on-race-income-teen-pregnancy/blob/master/Baltimore_nonwhite_demography%20.xlsx): the percentage of a population tract in Baltimore, MD that identifies as non-white

## Data Analytics
I determined the teenage pregnancy rate, average household income, and fraction non-white for each population tract in both Charleston and Baltimore, where sufficient data was available. I then determined the correlation between teenage pregnancy rate and both average household income and fraction non-white. 

The following table shows the correlation between the aforementioned variables in Charleston, SC:

The following table shows the correlation between the aforementioned variables in Baltimore, MD:

In both cities, there is a negative correlation between household income and teenage pregancy rates and a positive correlation between fraction non-white and teenage pregnancy rates. This indicates that people from low-income, predominantly non-white communities tend to have higher teenage pregnancy rates in Baltimore and Charleston. However, it is important to note that Baltimore's correlation between income and teen pregnancy rates is higher than Charleston's, while Charleston's correlation between race and teen pregnancy is higher than Baltimore's. 

With this correlation in mind, I performed a multiple linear regression model on the datasets from both cities.

The following table shows the multiple linear regression for Charleston's dataset:

The R squared value for the Charleston linear regression is roughly 0.37. As the R squared value tells us the percentage of one variable's behavior that can be predicted by another variable, this lower value indicates that our ability to predict teenage pregnancy rates based on household income and fraction non-white isn't very strong. 

The standard error for Charleston's linear regression is about 0.035. fdkjghjkdfhgjkdfhgkjdfhgkjfdhg

The coefficients for the x variables (Household Income and Fraction Non-White) are -2.056E-06 and 0.13 respectively. The fact that Household Income's coefficient is negative means that, as household income increases, it has a negative effect on the teenage birthrate (i.e. it lessens the teenage birthrate). Meanwhile, the coefficient for Fraction Non-White is positive, meaning that a higher percentage of non-white residents corresponds to a higher teenage pregnancy rate.

However, one should note that not all of the variables for Charleston's linear regression are significant due to the variable's P values. The P value tells us whether or not a dataset is significant, and thus whether or not we can use it to come to a conclusion about a variables' relevancy to the linear regression. A P value higher than 0.05 is considered insignificant, while a P value lower than 0.05 is considered significant. The P value for Household Income is insignificant because it is too high (at 0.4), while the much smaller P value for Fraction Non-White (0.006) is significant. Therefore, we can conclude that household income does not have a significant impact on teenage pregnancy rates in Charleston, despite its aforementioned correlation and coefficient. 

The following table shows the multiple linear regression for Baltimore's dataset:

The R squared value for Baltimore's linear regression is roughly 0.36, which means that our ability to predict teenage pregnancy rates based on household income and fraction non-white is also fairly weak.

The standard error dfkjghfdkjghkjdfhgjkdfhgjk.

The coefficients for houshold income and fraction non-white in Baltimore are -1.18E-5 and 0.078 respectively, indicating that increasing household income has a negative effect on teenage pregnancy rates and fraction non-white has a positive effect on teenage pregnancy rates. 

Interestingly, both household income and fraction-non-white are significant variables when determining teenage pregnancy rates in Baltimore. The P value for household income is 4.6E-09 and 0.015 for fraction non-white. 

Because the variables are significant, we can construct an equation to predict teenage pregnancy rates in Baltimore based on the data. The equation is as follows: Teenage Pregnancy Rate = 0.069 + -1.18E-05(Household Income) + 0.078(Fraction Non-White).

## Data Interpretation 
As household income was not a significant variable in Charleston's case, we cannot accurately say if it does or does not have an impact on the city's teenage pregnancy rates. This discrepency is interesting, as I noted in my original project that income had a less pronounced effect on teenage pregnancy rates in Baltimore. However, the linear regression for Baltimore demonstrated a clear relationship between household income, race, and teenage pregnancy rates. In Baltimore's case, people of color from low income households are more likely to experience teenage pregnancy than white people from higher income backgrounds. 

The fact that household income was significant and Baltimore but not Charleston refutes my hypothesis that race would have a bigger impact on teenage pregnancies in Baltimore due to its larger non-white population. In my linear regression for Charleston, fraction non-white seemed to be the only significant variable. One should also note that fraction non-white had a higher correlation with teenage pregnancy rates in Charleston than Baltimore, implying that race has a more causal effect on teenage pregnancy in my hometown. 

Based on my results, I propose that policy-makers focused on lowering teenage birthrates should develop plans based on a city's social context. While my limited dataset cannot be used to infer the prevalence of racism in Charleston, it does beg the question as to whether or not a higher degree of racism and, by consequence, more unequal access to healthcare or education along racial lines contributes more to teenage pregnancy rates within the city when compared to other parts of the country. Programs aimed at increasing household income in a more racially biased city or region may not be the most effective method of reducing teenage pregnancy.

## Error Analysis 
As with my previous project, Charleston had fewer population tracts and thus fewer datasets to compare. Additionally, many population tracts in Charleston lacked information on income or teenage pregnancy. It is possible that a correlation between household income and teenage pregnancy in Charleston could have been more apparent if more information was provided. 

## Step-By-Step Instructions




