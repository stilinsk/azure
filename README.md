 This will be all the visualizations we will be doing in sql and azure synapse analytics

####  which branch has the most sales and we will look at the specific branch which  gender contributes more revenue
 ```

SELECT 
    branch,
    SUM(CASE WHEN Gender = 'Male' THEN Total ELSE 0 END) AS Male_Sales,
    SUM(CASE WHEN Gender = 'Female' THEN Total ELSE 0 END) AS Female_Sales,
    SUM(Total) AS Total_Sales
FROM data
GROUP BY branch
order by Total_Sales;
#### perfomance of gender per every  product line

```
## product line per gender
```
SELECT 
    Product_line,
    SUM(CASE WHEN Gender = 'Male' THEN Total ELSE 0 END) AS Male_Sales,
    SUM(CASE WHEN Gender = 'Female' THEN Total ELSE 0 END) AS Female_Sales
FROM data
GROUP BY Product_line;
```
### customer type and totals
```
select 
Customer_type,
avg(Total)as totals
from data 
GROUP by customer_type
select
```
## payment and totals
```
select 
payment,avg(Total)as totals
from data 
GROUP by payment
```
