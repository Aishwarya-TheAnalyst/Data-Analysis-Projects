
<h1 align="center">Sales Insights using Power BI & SQL <a href="https://www.novypro.com/project/sales-insights-analysis-4" target="_blank" rel="noreferrer"> <img src="https://e7.pngegg.com/pngimages/252/727/png-clipart-power-bi-business-intelligence-microsoft-analytics-microsoft-text-rectangle-thumbnail.png" alt="PowerBI" width="40" height="40"/> </a> </h1>

### Problem Statement :bookmark:

The Sales Director at AtliQ Hardware, a company selling computer hardware and accessories across India, faces a crucial challenge. Despite ongoing discussions with regional managers to understand sales and market trends, the reliance on Excel files for data analysis creates frustration. This difficulty in interpreting numerical data delays the identification of business issues and limits informed decision-making. Consequently, there is a pressing need for a more user-friendly data analytics solution to improve performance evaluation and strategic planning across the organization.

## Technologies used ⚙️

* <p>Excel <img src="https://raw.githubusercontent.com/mrankitgupta/66DaysOfData/60139fb461ef56a19afd68ea4094f6069f27ce49/icons8-microsoft-excel%20(1).svg" alt="excel" width="25" height="25"/> </p>

* <p> MySQL <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" alt="mysql" width="35" height="35"/> </p>   

* <p> Power BI  <img src="https://e7.pngegg.com/pngimages/252/727/png-clipart-power-bi-business-intelligence-microsoft-analytics-microsoft-text-rectangle-thumbnail.png" alt="PowerBi" width="25" height="25"/> </p> 


* <p> Statistics <img src="https://raw.githubusercontent.com/mrankitgupta/66DaysOfData/c8c040f1c85d921db317152567f331354446286a/statistics-21.svg" alt="Statistics" width="25" height="25"/> </p>

  
#### [Power BI Dashboard Link](https://www.novypro.com/project/sales-insights-analysis-4) <a href="https://www.novypro.com/project/sales-insights-analysis-4" target="_blank" rel="noreferrer"> <img src="https://e7.pngegg.com/pngimages/252/727/png-clipart-power-bi-business-intelligence-microsoft-analytics-microsoft-text-rectangle-thumbnail.png" alt="tableau" width="20" height="20"/> </a>  🔗



## Approach - Project Planning & Aims Grid
<img src="https://github.com/Aishwarya-TheAnalyst/Sales-Insights-Data-Analysis-using-PowerBI-and-SQL/blob/main/images/AIMS%20grid%20sales%20insights.jpg" alt="AIMS Grid">

  

## Setup Process
  
Step 1: Download file: <code>[db_dump.sql](https://github.com/mrankitgupta/Sales-Insights-Data-Analysis-using-Tableau-and-SQL/blob/main/Databases/db_dump.sql)</code> 

Step 2: Import it in MySql do EDA(Exploratory Data Analysis)

Step 3: Download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) (Free) 
  
Step 4: Connect Power Bi with MySql database 
  
Step 5: Save the file as (.pbix)

  
## Data Analysis Using SQL
  
1. Show all customer records

    `SELECT * FROM customers;`

2. Show total number of customers

    `SELECT count(*) FROM customers;`

3. Show transactions for Chennai market (market code for chennai is Mark001)

    `SELECT * FROM transactions where market_code='Mark001';`

4. Show distrinct product codes that were sold in chennai.

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

5. Show transactions where currency is US dollars.

    `SELECT * from transactions where currency="USD"`

6. Show transactions in 2020 join by date table.

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

7. Show total revenue in year 2020.

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
8. Show total revenue in year 2020, January Month.

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

9. Show total revenue in year 2020 in Chennai.

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020and transactions.market_code="Mark001";`


## Data Analysis Using Power Bi 
  
#### Data Modelling in Power BI
	
<p  align="center"><a href="https://public.tableau.com/app/profile/mrankitgupta"><img width="80%" src="https://github.com/Aishwarya-TheAnalyst/Sales-Insights-Data-Analysis-using-PowerBI-and-SQL/blob/main/images/Data%20Modelling.JPG" /></a></p>

#### [Power BI Dashboard](https://www.novypro.com/project/sales-insights-analysis-4)
#### Key Insights
<p  align="center"><img width="100%" src="https://github.com/Aishwarya-TheAnalyst/Data-Analysis-Projects/blob/main/images/Key%20Insights.JPG" /></p>

#### Profit Analysis
<p  align="center"><img width="100%" src="https://github.com/Aishwarya-TheAnalyst/Data-Analysis-Projects/blob/main/images/Profit%20Analysis.JPG" /></p>

#### Performance Insights
<p  align="center"><img width="100%" src="https://github.com/Aishwarya-TheAnalyst/Data-Analysis-Projects/blob/main/images/Performance%20Insights.JPG" /></p>



  
## Project References: 🔗

|**Sr.No. 🔢**|**References 👨‍💻**| **Links :link:**|
|------|--------------------|---------------------|
|1| **Power BI Project Dashboard :** Sales Insights Analysis using Power BI | [Dashboard](https://www.novypro.com/project/sales-insights-analysis-4)|
|2| Tutorial | [YouTube 1](https://www.youtube.com/playlist?list=PLeo1K3hjS3utcb9nKtanhcn8jd2E0Hp9b) | 
|3| MySQL installation | [YouTube 2](https://www.youtube.com/watch?v=WuBcTJnIuzo) |
|4| Star Schema: Fact Table & Dimension Table | [Microsoft docs.](https://docs.microsoft.com/en-us/power-bi/guidance/star-schema) | 
  


