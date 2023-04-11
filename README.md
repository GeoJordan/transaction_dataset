# Transaction Dataset
## Creating Customer Transaction Dataset¶

Once I was faced with a challenge of creating an ecommerce customer transaction dataset using multiple datasets on an eCommerce platform. This company wants to use the new dataset to analyze products and customers to support their marketing campaigns. From this dataset, the business I would create additional datasets containing transaction matrix like order data, customer data, and product data, to enable me perform modeling, analysis, and even reporting of my findings.

I demonstrate the approach using the [Brazilian E-Commerce Public Dataset by Olist on Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce). These dataset were selected because like the Olist is an eCommerce platform that connects small business with customers from all over Brazil hence has similar characteristis as the platform I carried out the task for. 

Baring in mind that the project aims to merge all the datasets on the platform into One dataset, to help understand customer activities on the platform, I considered thr following:
- working with a multiple and/or large datasets usually create problems including PC memory issues. Hence, these memory utilization issues must be avoided.
- create dataframes from the core list of dataframes of items purchased which can be used for analysis, modeling, or reporting.
- merge the dataframes into Customer dataframe¶

#### Prerequisites
- jupyter notebook,
- the eCommerce dataset,
- python.

#### The Datasets
The dataset consists of 100k orders from 2016 to 2018 made at multiple marketplaces in Brazil. Its features comprises of an order from multiple dimensions: from order status, price, payment and freight performance to customer location, product attributes, reviews written by customers, and geolocation that relates Brazilian zip codes to lat/lng coordinates. 

There is also a marketing funnel dataset from sellers which has information of 8k Marketing Qualified Leads (MQLs) that requested contact between June 1st 2017 and June 1st 2018. These were randomly sampled from the total of MQLs. The features of these datasets allows viewing a sales process from multiple dimensions: lead category, catalog size, behaviour profile, etc.

#### Technology 
Anaconda 

#### Required packages
Numpy, Pandas, Datetime, and Pickle for memory utilization when handling large files without memory utilization issues.

#### Outcome
We notice that the new dataframe contains 91,472 entries with 34 fields. Interestingly, only 24.4 MB of the memory was used. I save the new dataframe as a pickle file to speed up the storage/retrival and use i.e. merging the datasets into a larger dataset without memory utilization issues. After this, I dump/delete the origional dataFrame from the drive. The business will use new pickle dataframe for to create any dataset required for their marketing campaign activities.
