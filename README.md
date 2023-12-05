# MultinationalRetailDataCentralisation

Multinational Retail Data Centralisation
Table of Contents
Description
Prerequisites
Installation
File Structure
Usage
License
Description
The Multinational Retail Data Centralisation project is designed to centralise and organize sales data from a multinational company, creating a unified source of truth for easy access and analysis by team members. The project involves setting up a robust database to store the sales data and implementing a system that ensures data consistency and accessibility.

Prerequisites
Before using this project, make sure you have the following prerequisites installed and configured:

Python:

This project is written in Python. Ensure you have Python installed on your machine. You can download Python from here.
Verify your Python installation by running python --version in a new terminal.
Java and JAVA_HOME:

This project utilizes Tabula, a tool for extracting tables from PDFs. Tabula relies on Java. You can download Java from here
Verify your Java installation by running java -version in a new terminal.
AWS CLI:

The AWS Command Line Interface (CLI) is used for interacting with Amazon S3. Install the AWS CLI by following the instructions here.
Verify your AWS CLI installation by running aws --version in a new terminal.
PGAdmin 4 and PostgreSQL:

Download and install PG4Admin and PostgreSQL. You can download PGAdmin 4 from here and PostgreSQL from here
Create a sales_data database in PG4Admin for later use.
VSCODE with Python and SQLTools:

Ensure Visual Studio Code (VSCode) is installed on your machine. You can download VSCODE from here
Install the Python extension for VSCode for a smooth development experience.
Install SQLTools extension in VSCode to facilitate SQL query execution.
Miniconda3 for Virtual Environments:

Install Miniconda3 to manage virtual environments easily. You can download Miniconda3 from here

Verify Miniconda3 installation by running conda --version in a new terminal.

The relevant Python libraries are pre-configured in mrdc_env.yaml. Complete the installation by executing:

conda env create -f mrdc_env.yaml
conda activate mrdc
Installation
Clone this repository to your local machine:

git clone https://github.com/KannanThuvakaran/AiCore-Multinational-Retail-Data-Centralisation.git
File Structure
milestone_2_utils

data_cleaning.py: Script for cleaning user, card, store, product, date and order data.
data_extraction.py: Script for extracting data from RDS tables, PDFs, APIs, and S3.
database_connector.py: Script for connecting to and uploading data to a PostgreSQL database.
milestone_3_star_schema_sales_database

modify_table_data_types : Modify each table structure and data
dim_card_details.sql
dim_date_times.sql
dim_products.sql
dim_store_details.sql
dim_users_table.sql
orders_table.sql
primary_foreign_keys
foreign_keys.sql: Add Foreign Keys for orders_table.
primary_keys.sql: Add Primary Keys for the other tables.
display_table_contents.sql: Display contents for all tables.
milestone_4_data_querying

business_queries.sql: SQL script for business-related queries.
.gitignore: Gitignore file which include the database credentials and sales_data_credentials files.

README.md: Documentation file.

create_database_credentials.yaml: Database credentials configuration file.

mrdc_env.yaml: Conda environment configuration file.

mrdc_main_script.py: Main script for executing the centralization process.

Usage
Setting up
Ensure you have activated the Conda environment:

conda activate mrdc
Ensure you have the Aicore database creds and your own. An empty version can be found in the create_database_credentials.yaml file.

Uploading Data to PostgreSQL and Centralising Data
Execute the main script to centralise data to PostgreSQL. You will have to put your own database credentials and Aicore credentials in the Python script:

python mrdc_main_script.py
This script will read and clean the sales data from the specified sources and create the central database and upload it to PostgreSQL.

Creating a Star Schema Sales Database
In PGAdmin 4 or using SQLTools in VSCode, connect to the PostgreSQL database to view the sales data. Run all the files in the milestone_3_star_schema_sales_database/modify_table_data_types directory to ensure all the tables in PostgreSQL are of the correct data types.
Run the primary keys and foreign key files in milestone_3_star_schema_sales_database/primary_foreign_keysto create primary and foreign keys to complete the star-based schema.
Queries
Once the star-based schema is complete, run the business SQL queries to extract up-to-date metrics for the business. The queries from the business can be found in the milestone_4_data_querying directory.

License
This project is open to the public.
