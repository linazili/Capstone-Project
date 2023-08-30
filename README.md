# Capstone-Project


Contents
Contents	1
Executive Summary	2
1. Project Background	3
Datasource	3
Targeted audience	3
Hypothesis and Aim	3
Context of the data	4
2. Analysis	5
RFM Analysis	9
Cohort Analysis	14
Customer Lifetime Value	16
3. Results	20
4. Conclusion	22
5. Recommendations	22


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

Analysis
70 % of the users have registered  through Search traffic source, 15 % through Organic search, the rest are taking 5 % each (Facebook, Email and Display advertising).

Now we can dig in to see how this is reflecting in marketing campaigns used for purchases and customer dynamics. Even though a customer registered through Facebook, for the purchase he might still use any other marketing campaign, like Youtube or Adwords. 




Figure 2.1. Purchase traffic source totals

Most of the orders and revenue 5,8 M eventually come from Email Marketing. Google Adwords also play an essential role and generate 3,8 M gross revenue. YouTube and Facebook both have very similar metrics and both take 22 % of the business. Organic source, being in second place by registrations, gets only 5 % of the purchase generated revenue. 

It is not uncommon for paid ads to generate more business compared to organic searches. Paid ads have the advantage of being  strategically placed in front of targeted audiences, allowing business to reach potential customers who may not have discovered them through organic searches. In our case we must admit that Organic registrations can provide long-term benefits, as a well-optimized website can attract consistent organic traffic over time without ongoing advertising costs.

Canceled and returned orders are taking 25% of all orders in monetary value.

Figure 2.2. Order status

Revenue, including Shipped, Complete, Processing, Canceled and Returned orders is considered as Gross Revenue. 
Revenue, excluding Canceled and Returned orders is considered as Net Revenue. 

Returned and Canceled  orders excluded from Looker revenue tables, now showing that most of the Net_revenue is generated through Email and Adwords campaigns.

Figure 2.3. Purchase traffic source Net revenue


There is an increase in Net revenue month by month and high increase since February 2023 due to increasing daily revenue. Also dramatical increase in May 2023 from 369K in February to 605K Net Revenue, 64% more orders.

Figure 2.4. Revenue increase


Comparing year to date results to the previous year, there is also significant revenue increase in 2023 both by revenue and by number of orders. There is only half month data for June, but so far we can see that sales are growing.


Figure 2.5. Revenue comparison


Search registration traffic source stands out, taking 70 % of the revenue, leaving all the rest of traffic way behind.

Figure 2.6. Sales by registration traffic source

There is an increase in all purchase traffic sources, however Email  and Adwords are taking 75% of all Net revenue.


Figure 2.7. Purchase traffic source revenue
To compare with other channels (Facebook, Youtube, and Organic)  both Email and Adwords have similar Shipped, Completed  and Processing orders ratio vs Cancelled and Returned, approximately 3.00. Therefore no excessive cancellations or returns are expected in either source, that might be considered a bad result.


Figure 2.8. Purchase traffic source by status

RFM Analysis
I wanted to have a look at how customers are behaving in different traffic sources in terms of purchase frequency, revenue and days since last order,  this is why RFM analysis was chosen to be processed.
Customers segmented into following groups: 
Champions, 
Loyal Customers, 
Potential Loyalists, 
Recent Customers,
Promising,
Need  Attention,
About to Sleep,
At Risk,
Lost.

Customers not active for 533-1579 days are considered as Lost.

Figure 2.9. Customer segmentation


Lost customers take 20% of total customers. Best customers - Champions take only 12,6 %, however generate 35% of total revenue.


Figure 2.10. Customer segmentation treemap


Highest average monetary value belongs to Champions. These are our best customers having the biggest item basket, buying most frequently (3,1 times) and placing orders not long ago. Second and third positions go to segments At Risk and Loyal Customers. Their baskets are also expensive and they tend to buy frequently to compare to other segments.

Figure 2.11. Customer segmentation values

In the following chart we can see that Lost customers are separated from the rest of the group. They were lost some 2,5 years ago. Company should pay attention to customers Needing Attention  and At Risk, as it has been nearly a year since the last order.

Figure 2.12. Customer segmentation bubbles.
 Bubble size shows  average monetary value


The company’s most valuable customers are Champions and Loyal Customers. To attract Champions, introduce new products and implement loyalty programs. For Loyal Customers focus on upselling higher-value products, ask for reviews and engage them in different ways.
There are 2 segments that need most of the attention at the moment. Segment At Risk needs to get personalized emails to reconnect, offer them renewals and provide helpful resources. Segment Need Attention need to get limited time offers. Send them reminder emails with offers what was trending and similar items to what was bought in the past.

There is a main difference between Search  and Facebook registration traffic sources, where Search Champions on average spend $565 and Facebook Champions - $278. In general there is more revenue generated from Loyal Customers in Facebook source, rather than best customers Champions.

Order frequency by purchase traffic source is shown in the table below. Despite the fact that our best customers Champions have an average frequency of 2.95 and we have 5280 of them, numbers below show that customers do not stay 4 times in a row with the same marketing source a lot. 
All five sources are mostly used for singular purchase, then clients tend to buy using different channels. However Email and Adwords got few clients attention 4 times in a row to make a purchase. Facebook and YouTube both have very similar results.

Figure 2.13. Purchase traffic order frequency

Among the customers from registration traffic sources, the results are very consistent. Regardless of the traffic source, the second purchase is made by 22 %, the third by 3%, and the fourth  by 0.3%. Email cohort stands out, as its customers have never made more than three purchases.

Figure 2.14. Registration traffic order frequency

Among all purchase traffic sources, customers tend to most frequently buy items with values ranging between $10 and $100. This trend is consistent for both Facebook and YouTube, as they show similar results. Additionally, items priced up to $10 exhibit comparable popularity across the entire customer population.  

Figure 2.15. Single item value frequency


Cohort Analysis
It is important to understand our users, when and what they do, but also why they do it. Cohort analysis comes handy here to understand which cohorts were most successful and which struggled. 

The table below indicates that after the registration, 5% of customers never made a purchase. Cohorts from 2022-04 until 2022-07 are having relatively better retention rates. Overall cohorts of 2022-04 and 2022-05 have best retention results for the first 4 months, cohorts of  2022-06 to 2022-08 have good results for the first 3 months, 2022-09 and 2022-10 for the first 2 months. 2022-08 cohort starts having really bad retention in month 8. All cohorts are struggling when 2023 March and April comes. Could be the offseason months. Need to check what marketing campaigns were used for cohorts of 2022-04 and 2022-05 and what were the most popular items sold between April and August to check if the summer season may have influenced customer activity.



Figure 2.16. Retention rate for the previous year


Looking at the average churn rates, we can observe that churn rates are relatively high in the early months (month_0, month_1, month_2). This suggests that the onboarding phase, where customers are new and still familiarizing themselves with the products or service, occurs within the first few months.
As the months progress, the churn rates gradually decrease and stabilize to lower percentages. This indicates that the nurture stage, where customers have become more engaged and accustomed to the product or service, starts around the 4th or 5th month and extends beyond the first year.
Therefore we can say that the onboarding phase lasts approximately for the first 2-3 months, and the nurture stage  begins around the 4th or 5th month onwards.
It is important to note that the onboarding stage retention rate is getting worse. Improving onboarding stage retention is crucial for setting a strong foundation for long-term customer engagement. 

It is necessary to have a look at how customers behave if we compare them registering from different user traffic sources (Search, Facebook, Organic, Email and Display). To compare user retention rate month by month and by user traffic sources we can see that there is no significant difference among paid and non paid traffic sources, however paid traffic sources tend to have slightly better retention rates, Display showing the best result at month 12.


Figure 2.17. Retention rate for the previous year

Customer Lifetime Value

This approach calculates the average value of a cohort of customers who registered through the same traffic source during a specific time period. It tracks the collective behavior and value generated by that group of customers over time. 
This approach will help us understand how much time needs to pass for the customer to start buying. It will also help us measure the effectiveness of marketing campaigns and customer acquisition strategies. It still helps identify the most valuable customers and tailor retention strategies accordingly.
Cohort lifetime value is used to evaluate the performance of specific cohorts or assess the impact of marketing campaigns. And  with customer lifetime value we focus  on understanding the long-term value and behavior of individual customers. Both approaches in conjunction help gain a comprehensive understanding of our customers' value and behavior.

In the table below we can see that since 2022-11 registration customers started to buy more on month 0. Sales increase is very well reflected in the last cohorts of 2023, where we can see the increasing revenue per customer. Customers tend to buy most in the first 4 months after the registration, and the average customer lifespan is 15 months, where the start date counted from customer registration date.


Figure 2.20. Customer Lifetime Value Cohorts


Paid versus non paid traffic sources have lower customer value (CV) at month 1, however later numbers show that non paid sources are more consistent and eventually bring higher CLV.

Figure 2.21. Customer Value in different user traffic sources


Seach CLV prediction table shows that the 2023-05 cohort will generate 4 times more revenue than the year before. All monthly cohorts average prediction for the 15 months is $246. Facebook predicted CLV is $211.


Figure 2.22. Predicted Customer Lifetime Value 

Overall, more customers wait a bit for their first order rather than buying products just after the registration. Email registered clients buy least straight after the registration but they show best results for the next 3 months.

For the selected period from 2022-01-01 to 2023-05-31, the number of users and CLV generated by each traffic source is as follows:

Traffic source
CLV
Predicted CLV
Growth
Search
$218
$246
12.84%
Facebook
$208
$211
1.44%
Organic
$217
$236
8.76%
Email
$214
$217
1.40%
Display
$201
$220
9.45%


Non paid traffic sources generated better CLV than paid, and predicted growth is on average 10%. 

The Display traffic source has a relatively lower CLV compared to other user traffic sources. However, the predicted CLV is higher, indicating potential growth and improved customer value in the future. This suggests that the Display campaign is performing well and has the potential to yield higher returns over the next 15 months.

Focusing on optimizing Email and Facebook campaigns and nurturing customer relationships could lead to higher CLV in the future, however predicted growth is quite low and should be investigated further.

While the number of users for each traffic source varies significantly, it is important to consider the quality of those users and their CLV. In this case, the Search traffic source has the highest predicted CLV at $246, followed closely by Organic traffic at $236.

However, making a conclusive judgment solely based on these numbers would be premature. To fully assess which traffic source is better, we should consider additional metrics such as conversion rates, customer acquisition costs, and overall return on investment (ROI) for each traffic source.

Additionally, it is essential to conduct statistical analysis to determine if the observed differences in CLV are statistically significant. Factors like seasonality, market trends, and other external factors should also be taken into account to make a well-informed decision.

Therefore, it is not possible to definitely state which source is better in terms of CLV. Further analysis and consideration of multiple factors are necessary to draw meaningful conclusions.


3. Results

Business task to analyze TheLook E-Commerce and gain insights into customers’ behavior after registering to the website through various user traffic sources and to determine which  marketing campaigns are most effective in driving purchases was analyzed.

The following questions were raised and analyzed:
What are the traffic sources customers can register to the website through?
Customers can register through various traffic sources: Search, Organic, Facebook, Email and Display.
70% of the customers used Search traffic source, 15% Organic, Facebook, Email and Display - 5%.
Purchase though is processed through Email, Adwords, Facebook, Youtube, and Organic traffic, Email getting 45% of the revenue and Adwords - 30.

       2.   How do these sources differentiate during the timeline?
As the number of customers increases, so does the revenue. Most new customers originate from Search registration traffic source, and there is a significant increase in customer acquisition starting from February 2022. Another notable peak occurs in February 2023, indicating further growth in customer augmentation.
Purchase traffic sources exhibit a similar trend of growth, however there are two marketing categories that predominantly attract customers to make a purchase: Email and Adwords. 

       3.   Sources ranking in terms of revenue and number of orders.
Search registration traffic source generates 70% of the revenue and number of orders. Organic 15%, Facebook 6%, Email 4.8 % and Display 4.2%.
Following the number of customers distribution during the registration (70/15/5/5/5) we can see that Facebook customers generated a bit more revenue, whereas Email and Display customers - less.
Purchase traffic sources sequence is as follows: Email 45% revenue, Adwords 30%, Facebook 10%, YouTube 10%, Organic 5%.
Highest ARPU value belongs to Email purchase campaign - $98 and lowest to Organic purchase campaign - $73.

        4.   What is the customer segmentation according to the traffic sources?
Only general customer segmentation was counted, revealing that the company has 20% Lost customers. The best customers are named Champions and Loyal Customers, we have 26% of them. The third category to be mentioned is customers who need attention at the moment, and they take 21% out of the total.
All five purchase traffic sources are mostly used for singular purchase, then clients tend to buy using different channels. However Email and Adwords got few clients attention 4 times in a row to make a purchase. Facebook and YouTube both have very similar results.

       5.   What do customers’ cohorts look like?
Although revenue is increasing, cohort analysis revealed that customer retention has been dropping down in the past cohorts. Retention experiences significant drop during the months of March and April throughout all cohorts.
The onboarding stage takes 3 months, when 30% of the customers churn.
Paid registered traffic source cohorts have slightly better retention rates.
Acquisition cohorts used to identify when new users are churning. Most new users churn during the first 3 onboarding months.

       6.    Customer Lifetime Value
Analysis revealed that CLV increases significantly after February 2023.
Organic and Email registered cohorts have better CLV for the first 5 months, however Organic continues to have the best results throughout the whole period.

4. Conclusion
Hypothesis that paid sources are more likely to bring more customers and revenue confirms partly.  Most revenue is brought through Search registered clients, and this source brings the highest CLV. However, we need to acknowledge that those acknowledged clients further make their purchases depending on different marketing campaigns, like Email and Adwords; Email having the highest ARPU - 98$, while Organic purchases lowest - $73.

A deeper analysis is needed to include conversion rates, bounce rates, and additional marketing metrics, such as ROI, CAC, CPC and others.
5. Recommendations

Further analysis is needed to analyze good and bad performing marketing campaigns. Compare the content of what was published, including impressions and clicks, conversion rates, acquisition costs, ROI and other relevant metrics to make informed decisions about the effectiveness of each campaign. Additionally, conducting A/B testing and monitoring the performance of different campaigns over time can provide a more accurate understanding of their relative impact on customer lifetime value.

Improve customer retention in the onboarding stage. Despite increasing sales, the retention of customers might be declining. If customers are not staying engaged with the business for as long as expected, it can lower the CLV eventually. Enhance the customer experience, implement loyalty programs, offer personalized recommendations, and provide exceptional customer service to increase customer loyalty and lifetime value. Gather feedback from customers during and after the onboarding process to understand their pain points, challenges, or suggestions for improvement.

Pay attention to customer segments that Need Attention and are At Risk. Engage Loyal and Potential To Loyal to become champions.

It is always best to have a variety of traffic sources. This minimizes the risk of website being decimated if the main traffic source dries up.

