# Data-projects-TripleTen-

Zomato Analysis

Questions to be answered:

1.	What's the revenue distribution over time?
2.	What cuisines are popular and which ones have the highest revenue?
3.	Is there a relationship between number of orders and revenue?
4.	What's the revenue distribution over time for the popular cuisines?
5.	What are the top 20 highest revenue restaurants and how are they performing year over year?

Hypothesis:

1.	Popular cuisines would have more restaurants available for the public to accommodate demand.
2. Restaurants with more locations would generate higher average revenue.

Data preparation : 

The cost column will be cleaned and a clean cost will be created to dismiss ascii characters in excel. The restaurant sheet will be used as the main sheet. The menu and the orders sheet will be left joined to the restaurant. The food sheet will be joined to the menu sheet.
Missing values and necessary data cleaning will be handled in tableau by filters.

Calculated fields : 
1.	‘ Net revenue’ to calculate sum of revenue for relationships between number of orders and revenue. 
sales amount - cleaned cost
2.	‘Average restaurant revenue’ to calculate year over year sales.
sum of revenue / number of restaurants

3.	‘Percent of total’ to calculate percent of difference.
Sum of sales amount / total sum of sales amount

4.	‘Percent difference’ to calculate year-over-year sales.
Calculate percentage change using lookup and zn in percent total.
(ZN([percent of total])-LOOKUP(ZN([percent of total]),-1)) / ABS(LOOKUP(ZN([percent of total]), -1))

5.	‘Total revenue’ to calculate total revenue.
Total sum of net revenue.

Tableau will be used for the visualization.
The analysis will display three dashboards.
1.Total Market
2.Most Sales
3.Highest Revenue

1.	The Total Market dashboard will display a line chart of weekly revenue and a total KPI, a year over year sales table and a revenue by sales scatter chart
2.	The Most Sales dashboard will display a pie chart to display the seven most popular cuisines by order quantity, a bar chart to display the number of restaurants by cuisines that are popular, aline chart that represents revenue over the period of quarters with a corresponding revenue KPI, popular restaurants year over year table.
3.	The Highest Revenue Table will display a bar chart with the twenty highest revenue restaurants by average revenue, a table with the Year Over Year Sales for Top 20 Highest Revenue Restaurants by Average Revenue

Dates will be visible in all three dashboards to visualize as desired. Highlighters will only be used in the Most Sales dashboard. None of the dashboards will explore customer behavior or product preferences. Explanations will be provided on the dashboards.
