Sales Insights of an Indian Hardware sales company- data analysis project performed on Tableau & Sql 

The present text outlines a technical accomplishment in the realm of data management. 
Specifically, it describes the development of ETL mappings through SQL, which enabled data extraction from unstructured sources and its subsequent transformation for data-cleaning purposes.
Additionally, the text highlights the development of a star schema data model in Tableau. 
This achievement demonstrates a high level of technical skill and expertise in data management, which would be of value in any business or academic setting.

A Tableau dashboard was developed to conduct an in-depth company performance analysis.
The dashboard utilizes quantitative visualizations to draw valuable insights based on various parameters affecting the company's yearly performance.
Comprehensive business solutions are then generated from the insights produced.



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


