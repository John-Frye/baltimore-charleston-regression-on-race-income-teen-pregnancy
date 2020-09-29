# baltimore-charleston-regression-on-race-income-teen-pregnancy
Predicting Teenage Pregnancies in Charleston, SC and Baltimore, MD based on racial demography and household income 
## Background 
In my previous project, I noted what appeared to be an inverse relationship between household income and the teenage pregnancy rate in Charleston, SC and Baltimore, MD. However, I noted that the relationship between income and teenage pregnancy was less pronounced in Charleston; the lowest population tract by household income in Charleston had lower teenage birthrates than Baltimore's highest earning population tract. This discrepency led me to believe that other factors, like race, may affect the teenage pregnancy rates differently in both cities. With this information in mind, I hypothesized that race was a greater determinant of teenage pregnancy rates in Baltimore due to its comparatively large no-white population. 
## Question
What is the relationship between a population tract's household income, percentage of non-white residents, and teenage pregnancy rate?
## Data Sources 
I derived all of my data from Opportunity Atlas. The data is categorized as follows:
- Average household income Charleston: the average household income in a population tract in Charleston, SC
- Average household income Baltimore: the average household income in a population tract in Baltimore, MD
- Teenage pregnancy rate Charleston: the fraction of women in a population tract in Charleston, SC who gave birth between the ages of 13-19
- Teenage pregnancy rate Baltimore: the fraction of women in a population tract in Baltimore, MD who gave birth between the ages of 13-19
- Fraction non-white Charleston: the percentage of a population tract in Charleston, SC that identifies as non-white
- Fraction non-white Baltimore: the percentage of a population tract in Baltimore, MD that identifies as non-white
## Data Analytics
I determined the teenage pregnancy rate, average household income, and fraction non-white for each population tract in both Charleston and Baltimore, where sufficient data was available. I then determined the correlation between teenage pregnancy rate and both average household income and fraction non-white. 

The following table shows the correlation between the aforementioned variables in Charleston, SC:

The following table shows the correlation between the aforementioned variables in Baltimore, MD:

In both cities, there is a negative correlation between household income and teenage pregancy rates and a positive correlation between fraction non-white and teenage pregnancy rates. This indicates that people from low-income, predominantly non-white communities tend to have higher teenage pregnancy rates in Baltimore and Charleston. However, it is important to note that Baltimore's correlation between income and teen pregnancy rates is higher than Charleston's, while Charleston's correlation between race and teen pregnancy is higher than Baltimore's. 

With this correlation in mind, I performed a multiple linear regression model on the datasets from both cities.

The following table shows the multiple linear regression for Charleston's dataset:

The R squared value for the Charleston linear regression is roughly 0.37. As the R squared value tells us the percentage of one variable's behavior that can be predicted by another variable, this lower value indicates that our ability to predict teenage pregnancy rates based on household income and fraction non-white isn't very strong. 

The standard error for Charleston's linear regression is about 0.035. 

The following table shows the multiple linear regression for Baltimore's dataset:

