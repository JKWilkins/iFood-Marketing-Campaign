# iFood-Marketing-Campaign

This project uses data from iFood, a Brazilian food delivery platform. The dataset has 2200+ rows of customers and contains demographic information and buying behavior for each. 

After cleaning up data types and encoding categorical features, I handle missing "income" data with regression imputation.
Regressinon impuation uses other features as predictors to model and estimate the missing data. Though this technique introduces error, it has an advantage over mean impuation because it preserves the relationships between income and other demographic and behavior data which is unlikely to be random. To improve this model for imputation, I would use log(income) as the response, because income data tends to follow an exponential distribution. This would result in more accurate predictons for higher incomes.

I then use Seaborn for visualizations to explore the relationships in demographics and customer activity, below are some of visualizations I found interesting or insightful. 

In this 2x2 facet, the scatterplots display the correlations between Income and Total Expenditure (MntTotal), Total Number of Purchases (NumPurchasesTotal), Num of Monthly Web Visits, and a violin plot showing the Income distribution per level of education. Each data point is color coded to the response variable, whether or not the customer accepted the recent marketing promotion. 

#### 2x2 facet of Scatterplots featuring Income on X axis
<img src="images/IncomeCorrelations.png" width = "800">  


In the top left scatter plot, it is evident that Income and Total Expenditure have a strong positive correlation. It also appears that those labled as promotion responders (orange) outspent customers of similar income levels.  
This is reinforced in the top right plot showing a similar correlation between Income and Num of Total Purchases. Visually it does not appear that upper-middle income promotion responders (orange) made more purchases than customer sof similar income level, indicating that the promotion may have led to larger orders rathen than more frequent ones.  
The bottom left plot interesting shows a negative correlation between income and Number of Monthly Web Visits. This seems contradictory to the previous plots showing a positive corelation between Income and Buying Behaviors, and might *imply that higher income customers buy more impulsively and with less consideration than their lower income counterparts*.  
Finally the Bottom right plot shows a violin plot betwene Income and levels of Education. The violin plot is interesting because it shows the min, max, and mean, while also displaying the distributions for the bivariate response variable. From the plot we can see a correlation between higher education and income, but also see that promotion responders trend towards having higher incomes than non-responders.


Lastly, I use random forest classification to predict whether or not a customer has responded to the latest marketing campaign and tune the model's parameters using both the visual "elbow technique" to balance bias-variance tradeoff and with a randomized grid search.

This model and visualizations can be used to estimate returns from the marketing campaign and determine what demographics to target. 
At a future time, I wish to cluster the customer's to get a better idea of the market demographics.
