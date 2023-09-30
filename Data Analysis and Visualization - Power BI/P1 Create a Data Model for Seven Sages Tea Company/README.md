# **Create a Data Model for Seven Sages Tea Company**


## Project Description:
The goal is to manage the datasets and develop an effective data model for a small tea company. This model will enable the company to gain a deeper insight into which products are both popular and profitable. This information will empower them to make informed decisions regarding product prioritization as the company continues to expand. The project serves as evidence of grasping fundamental data modeling principles. These include the capacity to clean, structure, and organize data using Power Query, establish a date table, construct a data model with appropriate relationships and filters, and generate a straightforward report utilizing common visualizations and DAX measures.

Below is a brief overview of the project's steps.

### Get Data:
The files: `CFO Metrics Tracker.xlsx`, `Customer List (as of FY2021).txt`, `SSBC Product Offerings.pdf`, `USD-CAD Exchange Rates.csv`, `Monthly Sales Logs/` were provided by Udacity and can be found on `Source Files/` folder on this repo.


### ETL step:
We utilized Power Query to perform data cleaning and preprocessing on our datasets, which involved the following actions:

- Merged 12 monthly sales files into a single query called to facilitate more comprehensive analysis.
- Combined the data from "Customer List (as of FY2021).txt" and "SSBC Product Offerings.pdf" into a query to include all relevant product attributes.
- Promoted the first rows in the datasets as headers for clarity.
- Removed any NULL values present in all the datasets.
- Renamed both queries and columns with descriptive names for improved readability.
- Adjusted the data types of columns to more appropriate ones.
- Constructed a dynamic date table, which we will explore further in the following section of the project.


### Creating Date Table:
Generated a date table using Power Query, and it's designed to automatically update itself based on the start and end dates found in the fact table.

The date table includes standard fields:

  - Calendar month name and number
  - Calendar year
  - Fiscal period
  - Fiscal year
  - Fiscal quarter -Quarter - FY (e.g., Q1 - FY2021)


### Create Data Model:
Our final structure consists of a single fact table and four dimension tables that are linked to it through an active one-to-many relationship.

### DAX Measures:

To meet the CFO's specifications, we will create six measures to calculate Sales, Cost of Sales, and Gross Profit Margin, each in two different currencies.
The following measures have been created using DAX, are present on the data model, and are clearly labeled:

  - Sales in USD ($)
  - Cost of Sales USD ($)
  - Gross Profit Margin (or GPM) in USD (%)
  - Sales in CAD ($)
  - Unit Sales by Product (%)
  - Share of gross profit by Product type (%)


### Build a Report

To meet the CFO's requests, our initial report version consists of two tabs. The first tab will provide a summary of sales by customer and customer type across quarters. The second tab, offers a summary of the percentages of gross profit and unit sales by product. Each tab will include a concise executive summary at the bottom.