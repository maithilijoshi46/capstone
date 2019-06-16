**Objective:**

Instacart is challenging the Kaggle community to use anonymized instacart orders data on customer orders over time to predict which previously purchased products will be in a user’s next order.


Directory Outline:
- *Data*
**Data Dictionary:**
This data dictionary only contains the variables that I used for my project and feature engineering


    |Columns|TypeDescription|  
    |------|---|-------|----|  ,
    |product_id|int64|product ID|  ,
    |product_name|object|product name|  ,
    |aisle_id|int64|aisle ID|  ,
    |department_id|int64|department ID|  ,
    |order_id|int64|unique order ID|  ,
    |add_to_cart_order|int64| **something** |,
    |reordered|float64|binary, reordered or not| ,
    |user_id|int64|ID number of anonymous user|,
    |order_number|int64|order number|,
    |order_dow|int64|day of week of the order|,
    |order_hour_of_day|int64|hour of day of the order|,
    |days_since_prior_order|float64|number of days since last order by user|,
    |average_orders|float64|by user, avg number of orders|,
    |average_order_dow|float64|by user, avg order day of week|,
    |average_order_hour|float64|by user, avg hour of order|,
    |weekend|int64|ordered on weekend or not, binary|,
    |rate_reordered|float64|rate of reorder by user|,
    |department|object|department name|,
    |aisle|object|aisle name|,
    |aisle_cat|int64|aisle category by unique values|,
    |dept_cat|int64|department category by unique values|,
    |product_cat|int64|product category by unique values|


*The datasets within this repository are:*
aisles.csv - all aisle data
departments.csv - all department data
products.csv - all product data
order_products_prior.csv - priors user reordering data
order_products_train - training user reordering data
orders_train_new - the dataset I used WITHOUT object variables after merging.
orders_train_all - the dataset I used WITH object variables after merging.
priors_sample - smaller, randomly sampled, subset of data from orders_train_new

- *Exploratory Data analysis*
Basic EDA to look at relationships
- *Feature engineering*
Engineering features to make a more accurate predictive model
- *Clustering analysis*
Trying out a PCA unsupervised learning algorithm and applying it to XGBoost
- *Recommender System*
Creating a recommender system to get at the goal of the competition
# Capstone
