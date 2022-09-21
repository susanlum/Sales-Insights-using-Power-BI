<img width="119" alt="Untitled" src="https://user-images.githubusercontent.com/105427308/188606715-5a74c902-93d6-43bc-9e1e-8ca8ee6f079c.png">

# Data Visualisation-using-Power-BI


### Problem statement <br>
* AtliQ Hardware is a  computer hardware & peripheral manufacturer based in Delhi, India. They have operations in various countries. 
* Their business is growing rapidly and they still rely on excel files for data analytics. Excel files are hard to consume and not effective in generating insights. 
* Due to the lack of effective analytics, the company faced a major loss in Latin America.
* Senior executives have decided to invest for automated dashboard to track sales performance across regions and generate real time sales insights. 

### Data Discovery <br>
Create AIMS grid to define purpose and success criteria of data analysis project. 

***Purpose***: To unlock sales insights that are not visible before sales team for decision support & automate them to reduced manual time spent in data gathering. 

***Stakeholders*** : Sales director, marketing team, customer service team, data & analytics team, IT

***End Result*** : An automated dashboard providing quick & latest sales insights in order to support data driven decision making

***Success Criteria*** : 
* Dashboard(s) uncovering sales order insights with latest data available 
* Sales team able to take better decisions & prove 10% cpst savings of total spend
* Sales Analysts stop data gathering manually in order to save 20% of their business time and reinvest its value added activity 

### Data Analysis Using SQL
*Show all customer records*: SELECT * FROM customers;

*Show total number of customers* : SELECT count(*) FROM customers;

*Show transactions for Chennai market (market code for chennai is Mark001)* : SELECT * FROM transactions where market_code='Mark001';

*Show distrinct product codes that were sold in chennai* : SELECT distinct product_code FROM transactions where market_code='Mark001';

*Show transactions where currency is US dollars* : SELECT * from transactions where currency="USD"

*Show transactions in 2020 join by date table* : SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;

*Show total revenue in year 2020* : SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";

*Show total revenue in year 2020, January Month* : SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");

*Show total revenue in year 2020 in Chennai* : SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";
