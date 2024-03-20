# INKAI-MARKETPLACE-ANALYSIS

## Table of contents
- [Inkai Market Place Overview](#inkai-market-place-overview)
- [Data Source](#data-source)
- [Tools](#tools)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data Analysis](#data-analysis)
- [Results](#results)
- [Recommendations](#recommendations)


## Inkai Market Place Overview
Inkai market place is an online platform that has varieties of ebooks such as ecommerce, affliate marketing, health, digital marketing, nutrition and lots more. This platform connects buyers who are online readers, that are interested in the collection of books, in order to aid easy buy and online studies. Sellers use the platform to showcase their products to potential buyer(readers) by uploading the available books and using different payment platform to interact with potential buyers.
It is a thriving platform that connects buyers and sellers and it continuously generates vast amounts of data regarding people and ebooks bought from the online market place. 
This report presents an analysis of this data to uncover valuable insights into customer behavior, product popularity, payment platforms, database of customers and online market trends. By leveraging advanced analytics techniques, i aim to provide actionable recommendations to enhance the marketplace's performance and improve the overall user experience.

## Data Source
The primary dataset used for this analysis is gotten from APPCLICK ACADEMY and it is confidential. It contains detailed information about activities such as sales, buyer's personal data, amount of products, most purchased items made by the company INKAI MARKET PLACE.

## Tools
- SQL server - Data Analysis
- Power Bi - Creating Report
   - [download here](https://powerbi.com)

## Exploratory Data Analysis
EDA involves exploring the dataset to answer key quesstions such as;

- Who are the last 20 login users?
- Who are the top 10 users with activation code
- What are the three market places with the most banner?
- Who are the top 15 users with ebook?
- What is the total number of views?
- Who are the top 10 users with the most ebook views?
- What is the most used payment platform?

## Data Analysis
Includes some interesting codes worked with 

```sql
select concat_ws(' ', first_name,last_name) as fullname, last_login
 from users
 group by fullname, last_login
 order by last_login desc
 limit 20;

select sum(viewed) as total_views
from ebooks;

select `type`as payment_platform,
count(*) as platform
from payment
group by `type`
order by payment_platform
limit 1;

select marketplace, 
count(marketplace) as most_banner
from banner 
group by marketplace
order by most_banner desc
limit 3;
 ```

## Results
1. The top three ebooks with the most banner in market place are affliate-marketing, digital_marketing and Ecommerce. Banner in this analysis means logo.
2. The total number of views of the ebook is 7086
3.  The most used payment platform is paypal with the total of 187

## Recommendations
Based on the analysis carried out, i recommend the following actions
- Invest in marketing and promotion during sales peak seasons especially for products with the highest sales such as digital-marketing in order to maximize sales potentials and yield more positive results.
- Focus on ensuring the most used payment platorm is always active on the website. Customers are impulse buyers and the faster they can get through with payment, the faster the ebook sells out.
- Implement a captivating and easy read through meethod on the website to increase ebook views and possibly increase buyers.
- view was created in the database to know the top users of the online marketplace.



















  
