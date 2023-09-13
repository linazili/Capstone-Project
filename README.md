# Capstone-Project

Looker Dashboard can be accessed here:
https://lookerstudio.google.com/reporting/6c4a170b-bd87-4a06-9d75-5d7497927d95

Capstone project in pdf attached separately in this repository.

Executive Summary

TheLook is a fictitious E-Commerce clothing site developed by the Looker team and is based in the USA. The data source for this project is a public dataset found in the BigQuery platform, dataset ID: bigquery-public-data.thelook_ecommerce.

The targeted audience of this report is theLook marketing team. They want to determine if there are any traffic sources that should be discontinued or, conversely, require increased investment in terms of making the purchase. The marketing manager and team aim to obtain key insights regarding the traffic source that attracts the most clients and generates the highest revenue. Additionally, they want to identify which source is more likely to have returning customers.

The hypothesis I am going to test is that paid sources are more likely to bring more customers and revenue.

A comprehensive analysis was conducted, including general timeline analysis, customer segmentation using RFM, Cohort and Customer Lifetime Value (CLV) analysis.

Hypothesis that paid sources are more likely to bring more customers and revenue confirms partly.  Most revenue and clients are brought through Search registered clients (70%), however we need to acknowledge that those clients further make their purchases depending on different marketing campaigns, like Email and Adwords and then generate better CLV.

Paid registration traffic cohorts showed better user retention rates, Display having the best retention rate at month 12.

A deeper analysis is needed to evaluate marketing campaigns (Email, Adwords, Facebook, YouTube and Organic) separately based on other metrics like ROI, CAC. Recommended to improve customer retention in the onboarding stage and pay attention to customer segments that need attention and are at risk. It is always best to have a variety of traffic sources. This minimizes the risk of the website being decimated if the main traffic source dries up.
Project Background
Datasource

For this Capstone project I will follow the steps of the data analysis process: Ask, Prepare, Process, Analyze, Share, and Act.

Data cleaning, validation, initial exploration of datasets and further analysis done in SQL and Google Spreadsheets. Data visualization done using Google Looker Studio.

Targeted audience
The marketing department wants to determine if there are any marketing traffic sources that should be discontinued or, conversely, require increased investment in terms of making the purchase. The marketing manager and team aim to obtain key insights regarding the traffic source that attracts the most clients and generates the highest revenue. Additionally, they want to identify which source is more likely to have returning customers.

Hypothesis and Aim
Paid sources are more likely to bring more customers and revenue.

Business Task:
Analyze TheLook E-Commerce and gain insights into customers’ behavior after registering to the website through various user traffic sources and determine which  marketing campaigns are most effective in driving purchases. 

Business Objectives:
What are the traffic sources customers can register to the website through?
How do these sources differentiate during the timeline?
Sources ranking in terms of revenue and number of orders.
What is the customer segmentation according to the traffic sources?
What do customers’ cohorts look like? 
Do customers tend to make purchases after clicking on different marketing campaigns, or do they tend to stick to one particular campaign?
What is the customer lifetime value and does it depend on the registration source?

Context of the data
TheLook is a fictitious eCommerce clothing site developed by the Looker team. The dataset contains information about customers, products, orders, logistics, web events and digital marketing campaigns.

File can be accessed: https://console.cloud.google.com/marketplace/product/bigquery-public-data/thelook-ecommerce?project=tc-da-1&pli=1

Data contains 7 tables (1 figure), nearly 125K rows in the orders table and almost 2,418K rows in the events table, 100K distinct registered users, 125K orders, total revenue >10M USD.


The dataset contains events from 2019-01-02 until current date. Company is selling clothing categories for men and women, such as: Tops, Accessories, Socks, Swim, Outwear etc. Company is getting traffic from Google Adwords, Email campaigns, Youtube, Facebook and through organic searches.
