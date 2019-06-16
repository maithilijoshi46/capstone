README


**Objective:**

Instacart is challenging the Kaggle community to use anonymized instacart orders data on customer orders over time to predict which previously purchased products will be in a user’s next order.




**Data from Instacart:**
Instacart published user data from 3 million Instacart orders for public use. Within this data, it included data about each aisle, department, orders, products, and a training and priors data set that explained which order came from the training , priors , and testing.



Aisles - aisle names and ID
Departments - department names and ID
Order products prior - "contains **previous order** contents for all customers"
order products train - training data set
orders - order names and ID
products - product names and ID's



**Data Analysis and Processing:**
The first notebook, titled "exploratory data analysis" explores relationships between variables in each data set, and cleaning up messy data to process later.

The second notebook, Feature Engineering, I merged each data frame that was given from InstaCart to create a "master" training dataset for predictive modeling and created several engineered features.

Of these, I created features such as "days since prior order", "average order of day", "average order hour", and more user behavior features to help best predict the facts that influence reordering.

I created several user-behaviour variables to aid in a better prediction. I dropped categorical data to make feature engineering and modeling easier.

**This is a classification problem**:
 Will this user re-order products or not? Within this notebook, I also took a crack at some predictive modeling with my new features.


In my data analysis I tested three models:

Logistic Regression, Random Forests, and XGBoost Classification.

I chose Logistic Regression because of it's ease in interpretability. Although I knew it would perform the worst, I wanted to assess a baseline accuracy and F1 score.

I chose Random Forests because of it's accuracy and it's ability to address the problem of "overfitting". Additionally, I liked Random Forests because of it's "relative feature importance" in assessing my model. This was key in visualizations.

Finally, the XG Boost model was picked because of it's robustness, and the general consensus in the data science community that it outperforms most models in performance. This model yielded the best scores.

I also applied PCA to XGBoost to see the explained variance in my model. I had to randomly select a sub-sample of my original training dataset to see if it made any difference. It, in fact, performed worse than XGBoost alone. This is likely due to the fact that I did not have a high level of dimensionality. My number of features was not actually that high, therefore it was not going to make a significant impact (if any) on my data.


**Recommender System:**
Finally, the objective of this project was to predict what a user was going to re-order. I created a recommender engine that suggested other orders based on previous product names.

**Summary:**

To evaluate what a user will re-order, I first turned this into a classification problem that predicted whether or not a user will reorder or not.

I then created a recommender system that predicted similar product orders based on product name, and order ID.

**Future Evaluation:**
Using Words2Vec to try and predict similar products has potential to make this model more accurate. If products and orders were used to create vectors that predicted similarities in orders. Perhaps this could be useful in predicting what types of food are purchased the most, beyond "organics".

More Features based on products. I created a lot of "user behavior" features, but not as many "product behavior" features. This was mostly out of not actually knowing how to best leverage this data in this way, however this could be a good avenue to go down next.
