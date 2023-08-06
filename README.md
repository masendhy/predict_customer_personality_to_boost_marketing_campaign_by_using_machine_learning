## **Predict Customer Personality to Boost Marketing Campaign by Using Machine Learning**

![Banner](images/img_1.jpg)

***
### **Customer Personality Analysis**
Customer Personality Analysis is a detailed analysis of a company’s ideal customers. It helps a business to better understand its customers and makes it easier for them to modify products according to the specific needs, behaviors and concerns of different types of customers.

Customer personality analysis helps a business to modify its product based on its target customers from different types of customer segments. For example, instead of spending money to market a new product to every customer in the company’s database, a company can analyze which customer segment is most likely to buy the product and then market the product only on that particular segment.

[Download Resources here](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis)
***
### **Goal**
Improving marketing campaign performance and target the right customers to be able to do transaction on company's platform
***
### **Objective**
Create a cluster prediction model using unsupervised learning so that it makes easier for companies to make decisions.
***
### **Data**
The dataset contains 2.240 data rows and 30 features of customers behavior features who made transactions and interactions on our platform.
### **Tools**
During this project I've use : <br>

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) <br>
`as programming language` <br> <br>
![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white) <br>
`as notebook` <br> <br>
![Visual Studio Code](https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white) <br>
`as IDE` <br> <br>
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)   ![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white) <br>
`as data preprocessing library` <br> <br>
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black) <br>
`as data visualization library`
***
### **Contents**

***Column Details***
Feature | Descriptions
--------|-------------
`ID`            | Unique ID of each customer
`Year_Birth`    | Customer's birth year 
`Education`     | Education Qualification of customer
`Marital_Status`| Marital Status of customer
`Income`        | Customer's yearly household income
`Kidhome`       | Number of children in customer's household
`Teenhome`      | Number of teenagers in customer's household
`Dt_Customer`   | Date of customer's enrollment with the company
`Recency`       | Number of days since customer's last purchase
`MntCoke`       | Amount spent on coke
`MntFishProducts` | Amount spent on Fish Products
`MntFruits` | Amount spent on Fruits
`MntSweetProducts` | Amount spent on Sweet Products
`MntGoldProds` | Amount spent on Gold Products
`NumDealsPurchases` | Number of purchases made with a discount
`NumCatalogPurchases`| The number of purchases made using a catalog (buying goods that will be sent by mail)
`NumStorePurchases` | Number of purchases made directly at the store
`NumWebPurchases` | Number of purchases made through the company website
`NumWebVisitsMonth` | Number of visits to the company's website in the past month
`Recency` | Number of days since last purchase
`Response` | 1 if the customer accepted the offer in the last campaign, 0 otherwise
<br>

***Exploratory Data Analysis***
On this section, there are few process such as :<br>
* handling missing values, 
* feature selection using Recency, Frequency, Monetary and Loyality (RFML) methods,
* feature transformations to selected features using minmaxscaler and standarscaler.

***Data Modeling***
* Modeling using K-Means Clustering with cross-validation elbow method on inertia and silhouette score <br>
* Principal Component Analysis for reduce dimensionality

### **Customer Personality Analysis for Marketing Retargeting**
**Based on my model, there are 4 customer clusters:**
1. High Spender Customer (Cluster 2)
* There are 413 customers (18.44% of total customers) on this cluster.
* Customers on this cluster have `average recency 22 days` and `average of total purchases 22 items` it's means they are frequent shoppers and `they spend a lot on our platform (around IDR 1,2M/year)`
<br>

2. Mid Spender Customer (Cluster 1)
* There are 538 customers (24.02% of total customers)on this cluster.
* Customers on this cluster have a little recency `average recency 72 days` and `average of total purchases 22 items` so it's means they are not frequent shoppers but `they spend on our platform around 1,1M/year `
<br>

3. Low Spender Customer (Cluster 0)
* The number of customers is highly dominated by this cluster, there are `652 customers` or `29.11% of total customers`.
* They are frequent shoppers `(average recency 24 days)` but only have `average of total purchase 10 items`, they are only spend on our platform `around 172K IDR/year`
<br>

4. Risk of Churn Customer (Cluster 3)
* The second most of our customers on this cluster, they are not frequent shoppers `average recency 74 days`, and they are just have `average of total purchases 9 items` and only `150K IDR/year` spend on our platform.

### **Business Recommendation**
***Actionable Insight***

1. Create membership tier program to keep customer retention also membership tier things will attract customers to shopping more on our platform. Let's say we have 3 membership tier (`Premium, Classic, Basic`) each membership tier has different privileges as customers. The highest membership tier they have, the greatest privileges they will get. On this case, we can give membership tier based on customer clusters (`Premium: High Spender and Mid Spender Customer, Classic: Low Spender Customer, Basic: Risk of Churn Customer`).
2. If we are focusing on `Premium Tier`, there are have a high amount of spending, `High Spender` frequent to shopping on our platform with 66% total accepted campaign, and `Mid Spender` there aren't frequent shoppers but more than 50% of campaign they are accepted. So we can review our campaign, which campaign prefer interesting by the customers, and we can change the campaign that's not interest the customers.
3. For the `low spender` customer, they are frequent shopping in our platform but just a little items they are purchases and they are have few accepted our campaign, it's can be our campaign are not suitable with them or we offer our campaign not at the right time (we can give our campaign near payday). `Low Spender Customer` can be a loyal customer, because they have high frequently recency shop on our customer.
4. The second most of our customer are `Risk of Churn Customer`, this is very unfortunate. May be we can give them a questionnaire to understand better what they need.

***Potential Impact (Quantitative)***
* Based on our clustering we still have potential Gross Merchandise Value (GMV) around `IDR 1.3B/year`, and it's can increased significantly if we can convert the `Low Spender Customer` with high spending.




