# Ford Sales Analysis 2023

## Table of content

- [Project Overview](project-overview)
- [Data Sources](data-sources)
- [Tools](tools)
- [Data Cleaning/Preparation](data-cleaning/preparation)
- [Exploratory Data Analysis](exploratory-data-analysis)
- [Data Analysis](data-analysis)
- [Results](results)
- [References](references)

## Project overview

This data analysis project aims to provide into the sales perfomance of a Ford company in the year 2023. By analyzing various aspects of the sales data, we seek to identify trends, make data-driven recommendations, and gain deeper understanding of the company's performance. 

## Data sources

Sales Data: The primary dataset used for this analysis is the "Ford 2023 Sales data.xlsx" file containing detailed information about each sale made by the company.


## Tools

- Excel - Data cleaning [Download Here](https://microsoft.com)
- SQL Server - Data analysis

## Data Cleaning/Preparation

In the intial data preparation phase, we performed the following tasks:
1. Data loading and inspection.
2. Handling missing values.
3. Data cleaning and formatting.


## Exploratory Data Analysis

EDA involved exploring the sales data to answer key question, For instance:
- What is the overall sales trend?
- Which car was top sellers?
- What are the peak sales periods?


## Data Analysis

Include some code/features worked with

```sql
CREATE TABLE ford_sales_2023 (
    id SERIAL PRIMARY KEY,
    model VARCHAR(50),
    sales_q4 INT,
    sales_total INT,
    percentage_increase DECIMAL(5, 2)
);

INSERT INTO ford_sales_2023 (model, sales_q4, sales_total, percentage_increase) VALUES
('F-150 Lightning', 25937, 72608, 18.00),
('Mustang Mach-E', NULL, 40771, 3.00),
('E-Transit', NULL, 7672, 18.00),
('Total', 50929, 1995912, 7.10);

-- Retrieve all sales data
SELECT * FROM ford_sales_2023;

-- Retrieve specific model data
SELECT model, sales_total FROM ford_sales_2023 WHERE model = 'F-150 Lightning';

-- Retrieve models with sales increase greater than 10%
SELECT model, sales_total, percentage_increase
FROM ford_sales_2023
WHERE percentage_increase > 10.00;

```

## Results

1. Ford sold 1,995,912 vehicles overall in 2023, a 7.1% increase over 2022.
2. F-150 Lightning: Sales increased by 18% to 25,937 units in Q4 of 2023 and 72,608 units overall.
3. Mustang Mach-E: Sales of 40,771 were achieved, a 3% rise over the prior year.
4. With significant expansion in the electric and hybrid industries, Ford maintained its leadership position in a number of markets, including trucks and commercial vehicles.

## References

1. [Ford Sales](https://s201.q4cdn.com/693218008/files/doc_news/2023/06/ford-may-2023-u-s-sales-data.pdf)




