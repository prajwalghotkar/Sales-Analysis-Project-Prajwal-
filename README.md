# Sales Analysis Project 

#### * For companies to become competitive and skyrocket their growth, they need to leverage AI/ML to develop predictive model to forecast sales in the future.
#### * Predictive models attempt at forecasting future sales on historical data while taking into account seasonality effects, demand, holidays, promotions, and competition. 
#### * In this Project Prajwal, You work as a data scientist in the sales department and the sales team provided you with data from 1115 stores.

## * The Objective is to predict future daily sales based on the features.

### * Id: transaction ID (combination of Store and date)
### * Store: unique store Id
### * Sales: sales/day,this is the target variable
### * Customers: number of customers on a given day
### * Open: Boolean to say whether a store is open or closed (0= closed. 1= open)
### * Promo: describes if store is running a promo on that day or not
### * StateHoliday: indicate which state holiday (a= public holiday, b = Easter holiday, c= Christmas, 0 = None)
### * SchoolHoliday: indicates if the (Store, Date) was affected by the closure of public schools.
### * StoreType: categorical variable to indicate type of store (a,b,c,d)
### * Assortment: a = basic, b = extra, c = extended
### * CompetitionDistance (meters): distance to closest competitor store
### * CompetitionOpenSince [Month/Year]: date when competition was open.
### * Promo2: Promo2 is a continuing and consecutive promotion for some stores (0 = store is not participating, 1 = store is participating)
### * Promo2Since [Year/Week]: date when store started participating in Promo2
### * PromoInterval: describes the consecutive intervals Promo2 is started, naming the months
### * promotion is started new. E.g. "Feb,May,Aug,Nov" means each round starts in February, May, August, November of any given for that store

# Steps:

## Steps 1) :
####   * IMPORT LIBRARIES AND DATASETS.
####   * Import train and store data separately
####   * Analyze the data set such as info() , describe () etc

## Steps 2) :
####   * Explore Data set : Train
####   * Check for NULL records

## Steps 3) :
####   * Create Histogram to check data
![image](https://github.com/user-attachments/assets/cf487da9-3369-482d-9a07-0b949f903e86)
![image](https://github.com/user-attachments/assets/55cf6420-798b-40f0-ab2b-9def5b66235b)
![image](https://github.com/user-attachments/assets/fb3a7314-df81-40fa-90be-76c0a4193c27)

## Steps 4) :
####   * Check Maximum number of customers 

####   * Count the number of stores that are open and closed

####   * Keep open stores and remove closed stores

####   * Drop the open column since it has no meaning now

####   * Describe the data set Open and check the difference with earlier 

## Steps 5) :
####   * Data Set : Store.csv

####   * Check for Null values – CompetitionDistance, CompetitionOpenSinceMonth

####   * if 'promo2' is zero, 'promo2SinceWeek', 'Promo2SinceYear', and 'PromoInterval' information is set to zero.

####   * There are 354 rows where 'CompetitionOpenSinceYear' and 'CompetitionOpenSinceMonth' is missing  set these values to zeros .

####   * There are 3 rows with 'competitionDistance' values missing, let's fill them up with with average values of the 'CompetitionDistance' column

####   * Check for Null values

## Steps 6) :
####   * Create Histogram to check data
![image](https://github.com/user-attachments/assets/f9c6bd11-6262-42b4-aa63-b22ab06723cf)
![image](https://github.com/user-attachments/assets/65b01205-7f88-4fc5-bf5f-95dd6a38ea2b)
![image](https://github.com/user-attachments/assets/863f2bb7-0ebe-4254-8534-92dc81c03ea2)

## Steps 7) :
####   * Merge both data frames together based on 'store’ sales_train_all_df = pd.merge(sales_train_df, store_info_df, how = 'inner', on = 'Store’)

####   * Create the Co relation with Sales - correlations = sales_train_all_df.corr()['Sales'].sort_values() correlations

####   * Promo and Customers has good co relation with sales

####   * Create Heat Map 

![image](https://github.com/user-attachments/assets/d1770e99-e3a6-432c-9549-0b11ad827118)

## Steps 8) :
####   * Extract Year , Month and Day from the date and create separate columns for Year, Month and Day

####   * Create Average Sales per month (Line Chart)- Group by month

![image](https://github.com/user-attachments/assets/573212fa-9b33-4526-99b2-bf4d421b70f7)

## Steps 9) :
####   * Create Average Customer  per month (Line Chart)

####   * 'groupby' works great by grouping all the data that share the same month column, then obtain the mean of the sales column  

![image](https://github.com/user-attachments/assets/8ebef585-1286-401e-bcd1-e8a0024e5957)

## Steps 10) :
####   * Look at the sales and customers per day. Minimum number of customers are generally around the 24th of the month. Most customers and sales are around 30th and 1st of the month

![image](https://github.com/user-attachments/assets/800e50a6-7a5b-4acb-b632-50c29c116c2c)

## Steps 11) :
![image](https://github.com/user-attachments/assets/b1a890b2-f53b-4960-b33e-1ff05bd68df6)

## Steps 12) :
####   * Repeat the same for Week 
![image](https://github.com/user-attachments/assets/6c6c9928-c52e-42e3-b063-e620dece4064)

## Steps 13) :
![image](https://github.com/user-attachments/assets/5a0ecef1-ce11-4882-ac5d-ed83e4179f5e)

## Steps 14) :
####     Date and Store Type
####     fig, ax = plt.subplots(figsize=(20,10))
####     sales_train_all_df.groupby(['Date','StoreType']).mean()['Sales'].unstack().plot(ax=ax)
![image](https://github.com/user-attachments/assets/a52cf269-d6c2-4ae8-903b-9c6d6a590f85)
         
## Steps 15) :
####   * Promo Sales and Promo Customer Charts
![image](https://github.com/user-attachments/assets/d254d910-c7cd-452b-8dd7-75724817cc9f)

## Steps 16) :
###    * Expected Results :
####   * Projected Sales in 2016 and 2017 by Year 
####   * Projected Sales 2016 and 2017 month wise 
####   * Number of  customers expected in 2016 and 2017 month wise
####   * Sales with Promo 2016 and 2017 month wise 
####   * Top 10 Store by Sales 2016 and 2017
####   * Bottom  10 Store by Sales 2016 and 2017



###### Prajwal




