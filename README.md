# Retail-Sales-Analysis-with-SQL
A portfolio project demonstrating SQL data analysis skills on a retail sales dataset. The analysis uses aggregate functions, CTEs, and advanced window functions to uncover insights into sales trends, top-performing products, and customer segment value.

## Analysis & Key Findings

I wrote 6 SQL queries to extract key insights from the sales data, progressing from basic aggregations to advanced analytical functions.

**1. What were our total sales?**
* **Result:** The total sales for the entire period were approximately $2.3 million.

**2. Which were the top 5 best-selling product Sub-Categories?**
* **Result:**
*
* | Item    | Amount      |
|:--------|:------------|
| Phones  | 327782.448  |
| Chairs  | 322822.731  |
| Storage | 219343.392  |
| Tables  | 202810.628  |
| Binders | 200028.785  |
* **Insight:** The business's revenue is primarily driven by high-ticket items.

**3. Which customer segment is most valuable?**
* **Result:** The Consumer segment had the highest sales (1148060.531), followed by Corporate (688494.0748), and then Home Office (424982.1769).
* **Insight:** Our largest customer base is the general consumer, which should be the focus of our primary marketing efforts.

**4. How did our sales perform year over year?**
* **Key Finding:** The business demonstrated healthy and consistent growth, with sales increasing from $484,247 in 2014 to over $733,215 in 2017.
* **Supporting Visual:**
    ![Line chart showing sales growth from 2014 to 2017]![A chart showing sales trends over the years](https://github.com/Premv123/Retail-Sales-Analysis-with-SQL/blob/main/sales_trend.png)
---

### Advanced Analysis

To showcase more advanced SQL capabilities, I also answered two deeper questions:

**5. What is the average value of each unique order?**
* **Result:** The Average Order Value (AOV) was approximately $459.475169179195.
* **Insight:** This key metric shows the average transaction size. This could be improved with strategies like product bundling or up-selling.
* **SQL Skill Demonstrated:** Calculated a key business metric using `SUM()` and `COUNT(DISTINCT ...)`.

**6. Who are the top 3 best-selling Sub-Categories *within each Region*?**
* **Result:** The top performers vary significantly by region, as shown in the table below.
* **Insight:** This deep-dive analysis shows that customer preferences are not uniform across the country. While 'Phones' dominate in the East, 'Binders' are a top seller in the Central region. This is a crucial insight for localized marketing and inventory management.
* **SQL Skill Demonstrated:** This was achieved using an advanced Window Function (`ROW_NUMBER()`) inside a Common Table Expression (CTE) to create a ranked list for each region.

| Region  | Sub-Category | Total Sales  |
| :------ | :----------- | -----------: |
| Central | Chairs       | $82,372.78   |
| Central | Phones       | $71,939.95   |
| Central | Binders      | $56,865.01   |
| East    | Phones       | $99,884.66   |
| East    | Chairs       | $95,687.51   |
| East    | Storage      | $69,428.66   |
| South   | Phones       | $58,098.34   |
| South   | Machines     | $53,890.96   |
| South   | Chairs       | $44,739.25   |
| West    | Chairs       | $100,023.20  |
| West    | Phones       | $97,859.50   |
| West    | Tables       | $81,016.23   |
