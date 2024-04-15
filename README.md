
Sales Insights - using Tableau & SQL  <img src="https://raw.githubusercontent.com/mrankitgupta/mrankitgupta/a768d6bf0a001f03327578ae12f8867e4056cbaf/tableau-software.svg" alt="tableau" width="55" height="40"/> </a> </h1>

**I am sharing India based Hardware company Sales Insights - A Data Analysis Project performed on Tableau & SQL in my journey into Data Science.** 

### About Project 👨‍💻

- Performed India based hardware company sales insights - A Data Analysis project.

- Developed a Tableau dashboard to perform analysis, producing quantitative visualizations in Tableau to draw valuable insights based on different parameters affecting the company performance year on year and further provide business solutions.

## Technologies used ⚙️

* Advance Excel

* MySQL

* Tableau

* Statistics

## Project - Hardware company Sales Insights - Data Analysis on Tableau & SQL
  
### [Tableau Dashboard Link](https://public.tableau.com/app/profile/aryan.gautam7093/viz/SalesInsights-DataAnalysisProjectusingTableau_17131731939740/Dashboard-RevenueAnalysis?publish=yes) <a href="https://public.tableau.com/views/SalesInsights-DataAnalysisProject/Dashboard-RevenueAnalysis?:language=en-US&:display_count=n&:origin=viz_share_link" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/mrankitgupta/mrankitgupta/a768d6bf0a001f03327578ae12f8867e4056cbaf/tableau-software.svg" alt="tableau" width="40" height="20"/> </a>  🔗

### Problem Statements
Sales director wants to know the performance of the company in various Indian states & accordingly provide some discount.

- Q1. Revenue breakdown by cities.

- Q2. Revenue brekdown by years & months.

- Q3. Top 5 customers by revenue & sales quantity.

- Q4. Top 5 Products by revenue.
  
- Q5. Net Profit & Profit Margin by Market

## Data Analysis Using SQL
  
1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001)

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distrinct product codes that were sold in chennai.

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

1. Show transactions where currency is US dollars.

    `SELECT * from transactions where currency="USD"`

1. Show transactions in 2020 join by date table.

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020.

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
1. Show total revenue in year 2020, January Month.

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

1. Show total revenue in year 2020 in Chennai.

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020and transactions.market_code="Mark001";`



  

