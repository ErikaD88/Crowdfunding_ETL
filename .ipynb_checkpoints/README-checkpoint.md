#Team 5 - Project 2 - ETL Mini Project 

    The project involves creating an ETL pipeline to extract, transform, and load data from Excel files into a PostgreSQL database. 
    The work is divided into specific tasks, assigned to team members to ensure efficient collaboration and progress tracking.
 
 ##Project Overview

    Goal: Build an ETL pipeline using Python and Pandas to process data, create CSV files, design an ERD, 
    define a PostgreSQL schema, and load the transformed data into the database.



##Task Assignments

1. Create the Category and Subcategory DataFrames
   Assigned to: Kaouther Abid
        
    Steps:
    
    1.    Load the crowdfunding.xlsx file into a Pandas DataFrame.
    
    2.    Extract and transform the category & sub-category column into two DataFrames:
          •    Category DataFrame:
          •    Columns: category_id (e.g., cat1, cat2, …) and category.
          •    Subcategory DataFrame:
          •    Columns: subcategory_id (e.g., subcat1, subcat2, …) and subcategory.
    
    3.    Export the DataFrames as:
          •    category.csv
          •    subcategory.csv

2. Create the Campaign DataFrame
   Assigned to: Sae Park/Myat Minn Khant

    Steps:
   
    1.   Load the crowdfunding.xlsx file into a Pandas DataFrame.
    
    2.   Extract and transform the data into the following columns:
         •    cf_id, contact_id, company_name, description, goal, pledged, outcome, backers_count, country, currency, launch_date, end_date, category_id, and subcategory_id.
    
    3.   Data type conversions:
         •    Convert goal and pledged to float.
         •    Convert launch_date and end_date to datetime format.
    
    4.   Merge the category and subcategory DataFrames to add category_id and subcategory_id columns.
    
    5.   Export the Campaign DataFrame as:
         •    campaign.csv

3. Create the Contacts DataFrame
   Assigned to: Charisse Robinson

    Steps:

Option 1: Python Dictionary Methods (Easiest):
    
    1.    Load contacts.xlsx into a Pandas DataFrame.
    2.    Iterate through each row, converting it into a dictionary.
    3.    Extract the contact_id, name, and email values.
    4.    Split the name column into first_name and last_name.
    5.    Create a new DataFrame with:
          •    Columns: contact_id, first_name, last_name, and email.
    6.    Export the DataFrame as:
          •    contacts.csv

Option 2: Regular Expressions (Advanced):
   
    1.    Load contacts.xlsx into a Pandas DataFrame.
    2.    Use regex to extract contact_id, name, and email from raw text.
    3.    Split the name column into first_name and last_name.
    4.    Create and export the DataFrame as:
          •    contacts.csv


4. Design the ERD and Set Up the Database
   Assigned to: Erika Dorsainvil / Melisa Hodzic
    
    Steps:
    
    1.    Design the ERD:
        •    Sketch relationships between category, subcategory, campaign, and contacts.
        •    Use QuickDBD to create the ERD.
        •    Save the schema as:
        •    crowdfunding_db_schema.sql
    
    2.    Set Up the Database:
        •    Create a PostgreSQL database named crowdfunding_db.
        •    Use the schema to define tables with primary and foreign keys.
    
    3.    Import CSV Files:
        •    Import the following CSVs into PostgreSQL:
        •    category.csv
        •    subcategory.csv
        •    campaign.csv
        •    contacts.csv
        •    Verify data by running SELECT * queries for each table.

    Deliverables
    
    1.    Transformed CSV Files:
        •    category.csv
        •    subcategory.csv
        •    campaign.csv
        •    contacts.csv
    
    2.    ERD:
        •    crowdfunding_db_schema.sql (includes table schema with relationships)
    
    3.    PostgreSQL Database:
        •    Populated with the data from the CSV files.
    
    4.    Verification:
        •    Results from SELECT * queries for all tables.


