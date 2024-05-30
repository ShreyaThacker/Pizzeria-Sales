# Pizzeria-Sales

## [Excel Dashboard]()


### Project Overview
The project intends to conduct a thorough analysis of the sales of a pizzeria for 2015 using Microsoft Excel.

The idea is to help the pizzeria understand its business better by identifying key metrics like seasonal sales and revenue trends, average customer headcount, average check size, effect of promotional offers, product popularity, etc.

Gaining and presenting useful insights that are easy to understand via charts and interactive dashboards will allow the pizzeria's stakeholders to make informed decisions about the pizzeria's future businesses.

### Tools and Environments
Microsoft Excel 365: Data organization, data cleaning and validation, data analysis, and visualization were done using powerful tools and features of Microsoft Excel

### Initial Data Inspection and Organization
Several `CSV` files were opened in Microsoft Excel 

The dataset for analysis was spread over four Excel workbooks one for each of the following:
  1. <b>Order_DateTime:</b> Date and Time of pizza orders
  2. <b>Order_Detail:</b> Gives OrderID, PizzaID, and quantity sold
  3. <b>Pizza_Price:</b> Details about the prices of various pizzas of different sizes
  4. <b>Pizza_Types:</b> The menu of the Pizzeria detailing the available items including the ingredients list

The data from these four workbooks was compiled into a single worksheet to facilitate analysis.
Lookup functions (`VLOOKUP`, `XLOOKUP`) and `INDEX/MATCH` were extensively utilized.

<p align="center">
  <img width="1000" height="310" src="https://github.com/ShreyaThacker/Pizzeria-Sales/blob/main/Images%20and%20GIFs/Four_tables.png">
</p>


`VLOOKUP`, `XLOOKUP` and `INDEX/MATCH`
<p align="center">
  <img width="1000" height="410" src="https://github.com/ShreyaThacker/Pizzeria-Sales/blob/main/Images%20and%20GIFs/LOOKUPS.gif">

### Data Cleaning and Validation
#### Missing Values
<b>Tool:</b> `COUNTBLANK` and `Filter` were used over the data range to identify any missing values

#### Removing Duplicates
<b>Tool:</b> Excel's `Remove Duplicates` feature was utilized.<br>
First, on the entire dataset using unique column combinations to check for repeat records.<br>
Second, to get a list of unique ingredients/toppings used by the pizzeria.

#### Data Standardization
<b>Date and Time Standardization:</b> The date format was changed to make it `mm/dd/yyyy`
                      <br>The date and time were then parsed into its components and formatted as text using `YEAR`, `MONTH`, `DAY`, `HOUR`, and `TEXT` functions.

<p align="center">
  <img width="1000" height="410" src="https://github.com/ShreyaThacker/Pizzeria-Sales/blob/main/Images%20and%20GIFs/date_parsing.gif">

<b>Text Standardization:</b> `TRIM` function was used to remove leading and trailing whitespaces in certain columns.
                      <br> `PROPER` function was used to achieve correct capitalization.
   
#### Data Transformation

<b>Splitting Columns:</b> The pizza sizes (S, M, L) were split from pizza_ID into a new column using the `RIGHT` function, and their abbreviations expanded.<br>
The column of pizza toppings was split using `TEXTSPLIT` into individual columns for each topping (as many as 8).

 <p align="center">
 <img width="1000" height="200" src="https://github.com/ShreyaThacker/Pizzeria-Sales/blob/main/Images%20and%20GIFs/right_textsplit_counta.gif">

<b>New Columns:</b> Discounts were introduced into the dataset. <br>

The `IF`  and `COUNTIF` functions were used extensively for the above processes.

### Data Analysis
- Total Sales Amount per item and order was calculated using `SUMIFS` 
- Total pizzas ordered per OrderID was computed
- Based on the number of pizzas purchased per order, Discounts were applied
- The number of Toppings on each pizza was calculated
- Topping popularity was analyzed and `conditional formatting` was applied to get the `TOP 10`
- Pizza popularity was analyzed to get the TOP 10 best-selling items on the menu
- `Pivot Tables` were used greatly to get the following:
  1. Monthly, Daily, and Hourly Sales and Revenue trends
  2. Count of various % discounts applied to each pizza size
 
<p align="center">
  <img width="920" height="470" src="https://github.com/ShreyaThacker/Pizzeria-Sales/blob/main/Images%20and%20GIFs/pivot%20table-chart.png">
</p>

<p align="center">
  <img width="470" height="470" src="https://github.com/ShreyaThacker/Pizzeria-Sales/blob/main/Images%20and%20GIFs/conditional%20formatting.png">
</p>





