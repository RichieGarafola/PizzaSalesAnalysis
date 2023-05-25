# PizzaSalesAnalysis
This repository presents an extensive analysis and visualization of pizza sales data. The goal of this project is to delve into the dataset, uncover meaningful insights, and provide valuable information regarding pizza sales trends and patterns. The accompanying Jupyter notebook, PizzaSales_Analysis.ipynb, includes the complete code and detailed results of the analysis.

This project is an analysis of pizza sales data, aiming to find patterns, trends, and possibly to predict future sales. The analysis can be useful for pizzeria owners, business analysts, data scientists, and anyone interested in the dynamics of pizza sales.

The pizza industry is a thriving and competitive market, with countless pizzerias vying for customers' attention. To succeed in this industry, it is crucial for pizzeria owners, business analysts, and data scientists to understand the dynamics of pizza sales. By harnessing the power of data analysis and visualization techniques, this project aims to provide actionable insights that can drive strategic decision-making and enhance business performance.

---
## Dataset

The dataset comprises four tables:

**Table: orders**

Field: order_id (Unique identifier for each order placed by a table)
Field: date (Date the order was placed, entered into the system prior to cooking and serving)
Field: time (Time the order was placed, entered into the system prior to cooking and serving)


**Table: order_details**

Field: order_details_id (Unique identifier for each pizza placed within each order, with the quantity increasing for the same type and size)
Field: order_id (Foreign key that ties the details in each order to the order itself)
Field: pizza_id (Foreign key that ties the pizza ordered to its details, such as size and price)
Field: quantity (Quantity ordered for each pizza of the same type and size)


**Table: pizzas**

Field: pizza_id (Unique identifier for each pizza, constituted by its type and size)
Field: pizza_type_id (Foreign key that ties each pizza to its broader pizza type)
Field: size (Size of the pizza, options include Small, Medium, Large, X Large, or XX Large)
Field: price (Price of the pizza in USD)


**Table: pizza_types**

Field: pizza_type_id (Unique identifier for each pizza type)
Field: name (Name of the pizza as shown in the menu)
Field: category (Category that the pizza falls under in the menu, options include Classic, Chicken, Supreme, or Veggie)
Field: ingredients (Comma-delimited list of ingredients used in the pizza as shown in the menu. All pizzas include Mozzarella Cheese, even if not specified, and they all include Tomato Sauce unless another sauce is specified.)

---

## Getting Started
### Prerequisites
To run the notebook, you need to have Python and Jupyter Notebook installed on your computer. The project also uses the following Python libraries:

- pandas

- numpy

- matplotlib

- seaborn

You can install these packages using pip:

    pip install pandas numpy matplotlib seaborn jupyter

---

## Key Objectives

The analysis focuses on achieving the following key objectives:

Identify Sales Patterns: Uncover patterns and trends in pizza sales, such as popular pizza types, peak ordering times, and preferred pizza sizes.

Optimize Pricing Strategy: Analyze pizza prices, category-wise revenue distribution, and customer preferences to optimize pricing strategies and maximize profitability.

Explore Pizza Categories: Investigate the performance of different pizza categories (e.g., Classic, Chicken, Supreme, Veggie) and identify opportunities for menu optimization or new product development.

Customer Analysis: Perform customer segmentation based on order history and preferences to target specific customer segments with personalized marketing campaigns and promotions.

---

## Methodology

The analysis employs various data analysis and visualization techniques to extract insights from the dataset. These techniques include data merging, aggregation, time series analysis, statistical analysis, data sorting and ranking, and data visualization. Each step is thoroughly documented in the Jupyter notebook, providing transparency and reproducibility of the analysis.

---

## Code Breakdown

**Import necessary libraries:** The code starts by importing the required libraries, including pandas, matplotlib.pyplot, and seaborn.

**Read the datasets:** The code reads four CSV files into separate DataFrames: order_details, orders, pizza_types, and pizzas.

**Define a function to display dataset information:** A function named display_dataset_info is defined to print the information and null values of a given dataset.

**Display dataset information:** The code iterates through the datasets dictionary and calls the display_dataset_info function to print the information and null values of each dataset.

**Data merging:** The code merges the pizza_types and pizzas datasets based on the 'pizza_type_id' column. Then, it merges the order_details and pizzas datasets based on the 'pizza_id' column.

**Calculate the total revenue generated from pizza sales:** A new column 'total_price' is created in the merged_data_pizzaId DataFrame by multiplying the 'quantity' and 'price' columns. The sum of the 'total_price' column is calculated to obtain the total revenue.

**Data aggregation:**

- Calculate the total quantity of each pizza ordered by grouping the merged_data_pizzaId DataFrame by 'pizza_type_id' and summing the 'quantity' column.

- Map the day of the week to its respective name in the orders DataFrame.

- Count the number of orders for each day of the week.


**Time series-based analysis:**


-Convert the 'start_time' and 'end_time' variables to datetime type.

-Convert the 'start_date' and 'end_date' variables to datetime type.

-Convert the 'time' column in the orders DataFrame to datetime type.

-Filter orders based on a specific time range.

-Filter orders based on a specific date range.

-Extract the hour and month from the 'time' and 'date' columns, respectively, in the orders DataFrame.

-Count the number of orders for each hour of the day.

-Calculate the total revenue generated each month.


**Statistical analysis:**


-Calculate the average order size for each month.

-Determine the most popular pizzas based on the number of orders.

-Subset the pizzas dataset for large pizzas only.

-Calculate the mean and median price of pizzas.

-Calculate the correlation between quantity and price.

-Calculate summary statistics of pizza prices.

-Calculate the total revenue generated by each pizza size.

-Calculate the total number of unique ingredients in each category.

-Calculate the total revenue generated by each pizza category.

-Calculate the maximum and minimum prices of pizzas.

-Calculate the number of unique customers.

-Calculate the average quantity per customer.

-Calculate the average price for each pizza category.

-Calculate the percentage distribution of pizza sizes.

-Calculate the average price by size.

-Calculate the revenue by pizza type.


**Data sorting and ranking:**

- Sort pizzas by price in descending order.

- Subset the pizzas dataset for vegetarian pizzas only.

- Rank pizzas by quantity ordered.

**Visualization:**

Several visualization plots are created using matplotlib.pyplot and seaborn to explore and analyze the data. The plots include bar plots, box plots, line plots, and horizontal bar plots. They visualize various aspects such as the number of orders by hour, total quantity of each pizza ordered, pizza prices by category, average price of pizzas by size, revenue by pizza type, revenue by month, average price of pizzas by category, top commonly used ingredients, distribution of pizza sizes, and number of orders by day of the week.

---

## Installation

To get a copy of the project, clone the repository using the following command:

git clone https://github.com/RichieGarafola/PizzaSalesAnalysis.git

Then navigate to the downloaded directory:

cd PizzaSalesAnalysis

Open the notebook:

jupyter notebook PizzaSales_Analysis.ipynb

---

## Usage

After opening the Jupyter notebook, execute each cell sequentially to observe the analysis results. Carefully follow the provided instructions and ensure that the prerequisite libraries are installed before running the notebook.

---

## Contributing

Contributions, issues, and suggestions for improvement are highly encouraged. If you wish to contribute, please refer to the Issues page of the project repository to check for ongoing discussions or create a new issue.

Project Link: https://github.com/RichieGarafola/PizzaSalesAnalysis

By unlocking the insights hidden within the complexities of pizza sales data, this project aims to empower stakeholders in the pizza industry to make informed decisions and drive sustainable growth.