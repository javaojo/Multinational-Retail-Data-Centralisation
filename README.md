# MultinationalRetailDataCentralisation

# Description
The Multinational Retail Data Centralisation project is designed to centralise and organize sales data from a multinational company, creating a unified source of truth for easy access and analysis by team members. The project involves setting up a robust database to store the sales data and implementing a system that ensures data consistency and accessibility.

Prerequisites
Before using this project, make sure you have the following prerequisites installed and configured:

Python:

This project is written in Jupyter Notebook. Ensure you have Python and Jupyter Notebook  installed on your machine. You can download Python from here.
Verify your Python installation by running python --version in a new terminal.

# Java and JAVA_HOME:

This project utilizes Tabula, a tool for extracting tables from PDFs. Tabula relies on Java. You can download Java from here
Verify your Java installation by running java -version in a new terminal.

# AWS CLI:

The AWS Command Line Interface (CLI) is used for interacting with Amazon S3. Install the AWS CLI by following the instructions here.
Verify your AWS CLI installation by running aws --version in a new terminal.
PGAdmin 4 and PostgreSQL:

Download and install PG4Admin and PostgreSQL. You can download PGAdmin 4 from here and PostgreSQL from here
Create a sales_data database in PG4Admin for later use.

# JupySQL - Jupyter Notebook SQL Magic

JupySQL is a Jupyter Notebook magic command that allows you to execute SQL queries directly within Jupyter Notebooks. This simplifies the workflow for data analysis and manipulation when working with SQL databases.

## Installation

To install JupySQL, run the following command in a Jupyter Notebook cell:

```python
!pip install jupyter-sql
```

Load the JupySQL extension:

%load_ext SQL

Connect to your SQL database:

```python
%sql sqlite:///:memory:  # Replace this URL with your database connection string
```
Write and execute SQL queries:
```python
%%sql

SELECT * FROM your_table
WHERE condition;
```

The relevant Python libraries are pre-configured in mrdc_env.yaml. Complete the installation by executing:

# Installation

Clone this repository to your local machine:

git clone https://github.com/javaojo/MultinationalRetailDataCentralisation.git
File Structure

README.md: Documentation file.

create_database_credentials.yaml: Database credentials configuration file.

Please make sure you have the Aicore database creds and your own. An empty version can be found in the create_database_credentials.yaml file.

Uploading Data to PostgreSQL and Centralising Data
Execute the main script to centralise data to PostgreSQL. You will have to put your database credentials and Aicore credentials in the Python script:

# Creating a Star Schema Sales Database
In PGAdmin 4 or using SQLTools in VSCode, connect to the PostgreSQL database to view the sales data. Run all the files in the milestone_3_star_schema_sales_database/modify_table_data_types directory to ensure all the tables in PostgreSQL are of the correct data types.
Run the primary keys and foreign key files in milestone_3_star_schema_sales_database/primary_foreign_keysto create primary and foreign keys to complete the star-based schema.
Queries
Once the star-based schema is complete, run the business SQL queries to extract up-to-date metrics for the business. The queries from the business can be found in the milestone_4_data_querying directory.

# License
This project is open to the public.
