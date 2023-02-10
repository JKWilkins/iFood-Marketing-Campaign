# iFood-Marketing-Campaign

This project uses data from iFood, a Brazilian food delivery platform. The dataset has 2200+ rows of customers and contains demographic information and buying behavior for each. 

After cleaning up data types and encoding categorical features, I handle missing income data with regression imputation

I then use Seaborn for visualizations to explore the relationships in demographics nd customer activity.

Lastly, I use random forest classification to predict whether or not a customer has responded to the latest marketing campaign and tune the model's parameters using both the visual "elbow technique" to balance bias-variance tradeoff and with a randomized grid search.

This model and visualizations can be used to estimate returns from the marketing campaign and determine what demographics to target. At a future time, I wish to cluster the customer's to get a better idea of the market demographics.
