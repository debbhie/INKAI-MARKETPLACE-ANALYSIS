# INKAI-MARKETPLACE-ANALYSIS

## Table of contents
- [Inkai Market Place Overview](#inkai-market-place-overview)
- [Data Source](#data-source)
- [Tools](#tools)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data Analysis](#data-analysis)
- [Visualization with powerBi of each Data Analysis](#visualization-with-powerbi-of-each-data-analysis)
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

## Visualization with powerBi of each Data Analysis
With the use of sql to analyze the database, i was able to use powebi to visualize the most valuable exploratory data. Kindly note that no dax function was used in powerbi as most of the analysis has been carried out in sql server.

![IMG_2258](https://github.com/debbhie/INKAI-MARKETPLACE-ANALYSIS/assets/161854079/f221b0a1-472d-408a-b0a0-3db76d81d3db)

From this visualization, these are the few steps taken to achieve this
- Using sql, i was able to query the most used payment platform on the database which is paypal and it has been used by 187 buyers.
- Banner in this project means logo and from the database, there are so many marketplace with different banners. From my query, i was able to the the marketplace that has the more banner than the others, i limited this search to 3 which are affliate marketing with the highest, digital marking and ecommerce share same result.
- The total views gotten from the ebook is 7086
- I checked the views individually from each users and i was able to get from the highest which is 1085 and the viewer"s name is Sarah Lee.

All the dataset worked on are visualized on the chart above and they are uploaded individually in assets folder.


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



















  
