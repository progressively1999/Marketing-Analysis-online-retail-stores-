# Marketing-Analysis-online-retail-stores-

**Problem Statement**

An online retail store is trying to understand the various customer purchase patterns for their firm, you are required to give enough evidence-based insights to provide the same.

**Project Objective**

The objective of this project is to find useful insights about the customer purchasing behaviour by using machine learning techniques to improve customer experiences and improve sales and segmenting the customers based on their purchasing behaviour.

**Data Descriptions**

The Online Retails dataset is a collection of data from an online retail store.

It is a transnational dataset which contains all the transactions occurring between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store online retail.

The company mainly sells unique all-occasion gifts. It contains information about customers, products, and orders. The dataset can be used to analyze customer behaviour, product trends, and other insights.

It can also be used to build predictive models to predict customer behaviour and product trends.

**InvoiceNo**: Invoice number. Nominal, a six-digit integral number uniquely assigned to each transaction. If this code starts with letter 'c', it indicates a cancellation  
**StockCode**: Product (item) code. Nominal, a five-digit integral number uniquely assigned to each distinct product  
**Description**: Product (item) name. Nominal  
Quantity: The quantities of each product (item) per transaction. Numeric  
**InvoiceDate**: Invoice Date and time. Numeric, the day and time when each transaction was generated  
**UnitPrice**: Unit price. Numeric, product price per unit in sterling  
**CustomerID** Customer number. Nominal, a six-digit integral number uniquely assigned to each customer  
**Country** Country name. Nominal, the name of the country where each customer resides

**Data Preprocessing Steps and Inspiration:**

- The Pre-processing of the data includes the following steps:
- Data Cleaning: Removing missing or invalid data points, as well as outliers that may skew the results.
- Data Preparation: Analysing Customers based on 3 factors- Recency, Frequency and Monetary.
- Data Transformation: Transforming the data into a format that is more suitable for the analysis.

**We'll be analysing the customer data through the lens of RFM analysis.**

This method considers three key aspects: recency, frequency, and monetary value. By examining these factors, we can gain a deeper understanding of customer behaviour.

**Recency (R):** This calculates how recently a customer made a purchase, typically measured in days since their last purchase compared to the most recent date in the dataset. It identifies how active a customer is.

**Frequency (F):** This determines how often a customer makes purchases. It's calculated by counting the number of unique invoice dates associated with a customer, indicating their purchase behaviour.

**Monetary Value (M):** This represents the total amount a customer has spent. You'll be using the "Total Amount" column established earlier to calculate this metric.

The easiest is to calculate the M-monetary value. We will be using the Total Amount column that we have created before.

**Outliers**

![image](https://github.com/user-attachments/assets/e666e31b-970d-4214-babe-aa56921be8ad)

![image](https://github.com/user-attachments/assets/71345491-4466-4e97-b881-5f761aa647ea)

![image](https://github.com/user-attachments/assets/9710f2f2-4561-49fd-8274-a73397a1a3a0)



**Removed Outliers**

![image](https://github.com/user-attachments/assets/418a140b-5776-456a-be02-7dcf6b37efa7)

![image](https://github.com/user-attachments/assets/9a8a03c9-534e-4f7c-9ae6-4e2cc9c1751c)

![image](https://github.com/user-attachments/assets/d6f88d02-ad82-4f17-b290-0c5d8cfd0709)



**Choosing the Algorithm for the Project:**

The algorithm that should be used for this project depends on the type of data we are working with and the type of problem we are trying to solve.

For example,

if we are working with customer reviews, we can use a supervised learning algorithm such as Logistic Regression or Support Vector Machines.

If we are working with machine learning, we can use an unsupervised learning algorithm such as K-Means Clustering or Hierarchical Clustering.

**Motivation and Reason for choosing the Algorithm:**

I have chosen K-means clustering algorithm.

It is one of the simplest and popular unsupervised machine learning algorithms.

The motivation for choosing a machine learning algorithm for online retail analysis is to gain insights into customer behaviour and preferences.

By using machine learning algorithms, retailers can better understand customer buying patterns, identify trends, and make more informed decisions about product offerings and pricing and also can be used to optimize marketing campaigns and improve customer segmentation

Finding the Optimal Number of Clusters

A fundamental step for any unsupervised algorithm is to determine the optimal number of clusters into which the data may be clustered. The Elbow Method is one of the most popular methods to determine this optimal value of k.

Elbow Curve to get the right number of Clusters
![image](https://github.com/user-attachments/assets/4d187abe-5227-462b-ae56-23f513d860ef)


**Model Evaluation and Technique:**

Machine learning models can be used to analyse online retail data in order to gain insights into customer behaviour and preferences. The most common techniques used for this purpose include supervised learning, unsupervised learning, and reinforcement learning.

K-Means Clustering with 3 Cluster Ids

Customers with Cluster Id 2 are the customers with high number of transactions as compared to other customers. Customers with Cluster Id 2 are frequent buyers. Customers with Cluster Id 0 are not recent buyers and hence least of importance from business point of view.
![image](https://github.com/user-attachments/assets/46af5d65-4eb7-44b1-b57a-56e99f43e073)
![image](https://github.com/user-attachments/assets/8a1daba4-37b6-4025-85dd-a69a8bb430fc)
![image](https://github.com/user-attachments/assets/4cac1382-60ef-4813-8bea-f3358ca02f9a)



**Inference From the Project:**

![image](https://github.com/user-attachments/assets/662f978b-551d-452e-841b-47ecd5958f19)


**Customer Types based on RFM Analysis:**

**Cluster 0 (Potentially Loyal Customers):**

**Recency:** Lower than ideal (average of 239.99 days since last purchase). This indicates these customers haven't purchased recently.

**Frequency:** Medium (average of 21.61 orders per customer). These customers tend to purchase somewhat regularly.

**Monetary Value:** Moderately high (average monetary value of $374.32). They spend a decent amount per purchase.

**Insights:** These customers could become loyal customers with some encouragement. They have a history of spending and purchase with some regularity.

**Recommendation:** Encourage them to become high-value customers with targeted campaigns such as:

- Discounts on bulk purchases or bundled products.
- personalized product recommendations based on their purchase history and browsing behaviour.

**Cluster 1 (Loyal Customers with High Potential Value):**

**Recency**: Average (mean of 44.85 days since last purchase). These customers purchase somewhat regularly.

**Frequency:** High (average of 108.12 orders per customer). They are frequent buyers.

**Monetary Value:** Highest (average monetary value of $1889.86). They spend the most per purchase on average.

**Insights:** These are likely to be your most valuable customers. They tend to purchase often and spend a lot per purchase. They are loyal customers with high potential value.

**Recommendation:** Retain these valuable customers and increase their spending by:

- Rewarding their loyalty with exclusive discounts, early access to new products, or personalized birthday offers.
- Offering them personalized product recommendations based on their purchase history.

**Cluster 2 (Needs Engagement - Potentially at Risk):**

**Recency:** Highest (average of 50.36 days since last purchase). These customers have the most recent purchases on average.

**Frequency:** Lowest (average of 33.44 orders per customer). They purchase the least frequently.

**Monetary Value:** Lower than ideal (average monetary value of $577.41). They tend to spend less per purchase on average.

**Insights:** These customers might be at risk of churning because they haven't purchased frequently despite having recent purchases. They tend to spend less per purchase as well.

**Recommendation:** Win them back with targeted campaigns such as:

- Sending them special offers or highlighting products they might be interested in based on past purchases.
- Offering them a discount or loyalty program points to incentivize a purchase.

**Future Possibilities:**

The future possibilities of this project are endless.

1. With the use of machine learning, the project can be used to analyse customer behaviour and preferences, predict customer buying patterns, and recommend products to customers based on their past purchases.
2. Additionally, machine learning can be used to identify trends in customer buying patterns and suggest new products or services that may be of interest to customers.
3. Finally, machine learning can be used to optimize pricing and promotions to maximize customer satisfaction and profitability

**Conclusion**

<table><tbody><tr><th><p>Clusters</p></th><th><p>Customer Types</p></th><th><p>RFM Insights</p></th><th><p>Recommendation</p></th></tr><tr><td><p>0</p></td><td><p>Potentially Loyal Customers</p></td><td><p>Customers purchase somewhat regularly (average 21.61 orders) but haven't purchased recently (average 239.99 days since last purchase).</p><p>They tend to spend a decent amount per purchase (average $374.32).</p></td><td><ul><li>Encourage them to become high value customers with targeted campaigns.</li><li>Offer discounts on bulk purchases or bundled products.</li><li>Provide personalized product recommendations based on their purchase history and browsing behaviour.</li></ul></td></tr><tr><td><p>1</p></td><td><p>Loyal Customers with High Potential Value</p></td><td><p>These are likely your most valuable customers (average $1889.86 per purchase).</p><p>They tend to purchase often (average 108.12 orders) with an average recency of 44.85 days.</p></td><td><ul><li>Retain these valuable customers and increase their spending</li><li>Reward their loyalty with exclusive discounts, early access to new products, or personalized birthday offers.</li><li>Offer them personalized product recommendations based on their purchase history.</li></ul></td></tr><tr><td><p>2</p></td><td><p>Needs Engagement (Potentially at Risk)</p></td><td><p>Despite recent purchases (average 50.36 days ago), these customers purchase infrequently (average 33.44 orders) and spend less per purchase (average $577.41). They might be at risk of churn.</p></td><td><ul><li>Win them back with targeted campaigns Send them special offers or highlight products they might be interested in based on past purchases.</li><li>Offer them a discount or loyalty program points to incentivize a purchase.</li></ul></td></tr></tbody></table>

**Reference**

**GitHub repository:** As outlined in a GitHub repository on EDA.

**Medium article:** As discussed in a Medium article about K-mean Clustering techniques.

**Kaggle Dataset:** As discussed in a Kaggle dataset on Online Retail.
