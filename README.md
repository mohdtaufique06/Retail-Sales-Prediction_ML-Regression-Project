# **<h3 align="center">Rossmann Sales Prediction </h1>**
<h3 align="center"> AlmaBetter Verfied Project - <a href="https://www.almabetter.com/"> AlmaBetter School </a> </h5>
<p align="center"><img src="https://media-cdn.tripadvisor.com/media/photo-s/16/e1/ec/f7/rossmann.jpg" align="center" ALT="HTML" width="alt%"/></p>

# Business Problem.

Rossmann operates over 3,000 drug stores in 7 European countries. Currently, Rossmann store managers are tasked with predicting their daily sales for up to six weeks in advance. Store sales are influenced by many factors, including promotions, competition, school and state holidays, seasonality, and locality. With thousands of individual managers predicting sales based on their unique circumstances, the accuracy of results can be quite varied.

# Data Description

* Rossmann Stores Data.csv - historical data including Sales

* store.csv - supplemental information about the stores

### Columns in the dataframe:
1. Id - an Id that represents a Store within the test set
2. Store - a unique Id for each store
3. Sales - the turnover for any given day (this is what you are predicting)
4. Open - an indicator for whether the store was open: 0 = closed, 1 = open
5. StateHoliday - indicates a state holiday. a = public holiday, b = Easter holiday, c = Christmas, 0 = None
6. SchoolHoliday - indicates if the Store on a particular Date was affected by the closure of public schools
7. StoreType - differentiates between 4 different store models: a, b, c, d
8. Assortment - describes an assortment level: a = basic, b = extra, c = extended
9. CompetitionDistance - distance in meters to the nearest competitor store
10. CompetitionOpenSince[Month/Year] - gives the approximate year and month of the time the nearest competitor was opened
11. Promo - indicates whether a store is running a promo on that day
12. Promo2 - Promo2 is a continuing and consecutive promotion for some stores: 0 = store is not participating, 1 = store is participating
13. Promo2Since[Year/Week] - describes the year and calendar week when the store started participating in Promo2
14. PromoInterval - describes the consecutive intervals Promo2 is started, naming the months the promotion is started anew. E.g. "Feb,May,Aug,Nov" means each round starts in February, May, August, November of any given year for that store

## Conclusions

### On EDA
- Stores with Assortment level ‘b’ has the highest sales.
- Approx. 50% stores are of type ‘a’. There are very few stores 
of type ‘b’.
- Store type ‘b’ has the highest sales and all other store 
types ‘a’,’c’,’d’ has nearly equal sales.
- December records the highest monthly sales. This may be 
due to Christmas and New Year.
- Sales is more when promos/offers are running on stores.
- From the sales and customer scatterplot, the relationship 
is sort of linear ie sales is increasing with number of 
customers increasing which is obvious.

### On Model Training
- By Looking at the evaluation metrics obtained on
implementing different sort of regression model, we decided to
go with the Random Forest Tuned model.The maximum R^2 was
seen in tuned Random Forest model with the value 0.97267. It
means our best accurate model is able to explain approx/almost
97% of variances in the datasets.

- Based on our model; Customer, store Type, Promo &
Competition Distance are the most impactful features which are
driving the sales more as compared to other features present in
the dataset.



