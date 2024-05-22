# DataStage Project: Retail Industry Scenario

## Project Overview
This project demonstrates a typical star-schema data warehousing flow using IBM InfoSphere DataStage, applied to a "real world" retail industry scenario. The objective is to build a star-schema based sales analysis data warehouse, preserving versions of dimension attributes to deliver accurate query results.

## Project Description
Our scenario assumes a fictitious national department store that decides to construct a star-schema sales analysis data warehouse with the following dimensions:
- Customer
- Store
- Product

The fact table in this scenario is "transactions". Over time, dimension attributes are expected to change, and these changes need to be preserved in the star-schema data warehouse.

### Initial Setup
1. **Design the star-schema**: Create the structure for the fact and dimension tables.
2. **Populate the dimension and fact tables**: Load initial data into the tables.
3. **Setup for recurring tasks**: Prepare for regular data updates and maintenance.

### Star Schema Model
The star schema consists of three dimensions and a fact table:
- **Dimensions**: Product, Retail, Customer
- **Fact Table**: Transactions

## Project Requirements
1. **Modeling Process**: Translate the logical data model to a physical data model.
    - This step has been completed, and sample data has been loaded into the provided files.
2. **ETL Solution**: Create an ETL process to load data into files or databases, transforming it to meet business needs.

## Tasks and Questions
1. **Data Mart Creation**: 
    - Create a data mart named `RETAIL_DATA_MART` displaying each transaction for each customer, categorized by customer type ("citizen" or "foreign"). Include product information and stock details.
    - Transform the customer name column to uppercase.
    - Replace the dimension date table with a single date column.
    
2. **Business Needs Analysis**:
    - Read the data mart `RETAIL_DATA_MART` to:
        - Display the count of all transactions for each customer per store.
        - Display the maximum profit made by each customer type. For example, if foreign customers make 5 transactions and citizens make 3, foreign customers yield the maximum profit.
    - Create a data mart named `ACTIVATION_SALES_DATA_MART` based on this analysis.
    - Determine bonuses for customers based on profit made:
        - **Bonus Equation**: `Annual_Income(k$) * SpendingScore * 100`

## Files and Sample Data
The attached files include:
- Logical and physical data models
- Sample data for dimensions and fact tables

## Getting Started
1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/retail-datastage-project.git
    ```
2. Navigate to the project directory:
    ```sh
    cd retail-datastage-project
    ```
3. Follow the steps in the project requirements to set up and run the ETL process.
