# Pizzeria-Sales

## [Excel Dashboard]()


### Project Overview
The project intends to conduct a thorough analysis of the sales of a pizzeria for 2015 using Microsoft Excel.

The idea is to help the pizzeria understand its business better by identifying key metrics like seasonal sales and revenue trends, average customer headcount, average check size, effect of promotional offers, product popularity, etc.

Gaining and presenting useful insights that are easy to understand via charts and interactive dashboards will allow the pizzeria's stakeholders to make informed decisions about the pizzeria's future businesses.

### Tools and Environments
Microsoft Excel 365: Data organization, data cleaning and validation, data analysis, and visualization were done using powerful tools and features of Microsoft Excel

### Initial Data Inspection and Organization
Several .csv files were opened in Microsoft Excel 

The dataset for analysis was spread over four Excel workbooks one for each of the following:
  1. Pizza_Types: The menu of the Pizzeria detailing the available items including the ingredients list
  2. Pizza_Price: Details about the prices of various pizzas of different sizes
  3. Order_DateTime: Date and Time of pizza orders
  4. Order_Detail: Gives OrderID, PizzaID, and quantity sold

The data from these four workbooks was compiled into a single worksheet to facilitate analysis.
  Lookup functions (VLOOKUP, XLOOKUP) and INDEX/MATCH were utilized to do this

### Data Cleaning and Validation
#### Missing Values
<b>Tool:</b> `COUNTBLANK` and Filters were used over the data range to identify any missing values

<b>Result:</b> No missing values were found

#### Removing Duplicates
<b>Tool:</b> Excel's `Remove Duplicates` feature was used extensively<br>
      First, on the entire dataset using unique column combinations to check for repeated records<br>
      Second, to get a list of unique ingredients/toppings used by the pizzeria

<b>Result:</b> The dataset had all unique order IDs, no repeats

#### Data Standardization
<b>Date and Time Standardization:</b> The date format was changed to make it `mm/dd/yyyy`
                      <br>The date and time were then parsed into its components and some parts were formatted as text using `YEAR`, `MONTH`, `DAY`, `HOUR`, and `TEXT` functions

<b>Text Standardization:</b> `TRIM` function was used to remove leading and trailing whitespaces in certain columns
                      <br> `PROPER` function was used to achieve correct capitalization

#### Data Transformation
<b>Splitting Columns:</b> The Pizza size (S, M, L) was split from pizza_ID into its column using the `RIGHT` function, and the abbreviations were expanded<br>
The list of toppings was split using `TEXTSPLIT` into individual columns (as many as 8)

<b>New Columns:</b> Discounts were introduced into the dataset <br>

The `IF`  and `COUNTIF` functions were used extensively for the above processes

### Data Analysis
- Total Sales Amount was calculated
- Total pizzas ordered per OrderID was computed
- Based on the number of pizzas purchased per order, Discounts were applied
- Number of Toppings on each pizza was calculated
- Topping popularity was analyzed and `conditional formatting` was applied to get the `TOP 10`
- Pizza popularity was analyzed to get the TOP 10 best-selling items on the menu
- `Pivot Tables` were used to get the following: Annual, Monthly, Hourly Sales and Revenue trends





