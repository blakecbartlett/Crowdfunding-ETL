# Crowdfunding_ETL
For the ETL mini project, you will work with a partner to practice building an ETL pipeline using Python, Pandas, and either Python dictionary methods or regular expressions to extract and transform the data. After you transform the data, you'll create four CSV files and use the CSV file data to create an ERD and a table schema. Finally, you’ll upload the CSV file data into a Postgres database.
(Original Repository located here: https://github.com/C-Duke0/Crowdfunding_ETL)

Instructions

Create the Category and Subcategory DataFrames
  1. Extract and transform the crowdfunding.xlsx Excel data to create a category DataFrame that has the following        columns:
  2. A "category_id" column that has entries going sequentially from "cat1" to "catn", where n is the number of unique      categories
  3. A "category" column that contains only the category titles
  4. Extract and transform the crowdfunding.xlsx Excel data to create a subcategory DataFrame that has the following  columns:
  5. A "subcategory_id" column that has entries going sequentially from "subcat1" to "subcatn", where n is the number of unique subcategories
  6. A "subcategory" column that contains only the subcategory titles

Create the Campaign DataFrame
  1. Extract and transform the crowdfunding.xlsx Excel data to create a campaign DataFrame has the following columns:
  2. The "cf_id" column
  3. The "contact_id" column
  4. The "company_name" column
  5. The "blurb" column, renamed to "description"
  6. The "goal" column, converted to the float data type
  7. The "pledged" column, converted to the float data type
  8. The "outcome" column
  9. The "backers_count" column
  10. The "country" column
  11. The "currency" column
  12. The "launched_at" column, renamed to "launch_date" and with the UTC times converted to the datetime format
  13. The "deadline" column, renamed to "end_date" and with the UTC times converted to the datetime format
  14. The "category_id" column, with unique identification numbers matching those in the "category_id" column of the  category DataFrame
  15. The "subcategory_id" column, with the unique identification numbers matching those in the "subcategory_id" column of the subcategory DataFrame

Create the Contacts DataFrame
  1. Import the contacts.xlsx file into a DataFrame.
  2. Iterate through the DataFrame, converting each row to a dictionary.
  3. Iterate through each dictionary, doing the following:
    - Extract the dictionary values from the keys by using a Python list comprehension.
    - Add the values for each row to a new list.
  4. Create a new DataFrame that contains the extracted data.
  5. Split each "name" column value into a first and last name, and place each in a new column.

Create the Crowdfunding Database
  1. Use the information from the ERD to create a table schema for each CSV file.
  ![image](https://github.com/C-Duke0/Crowdfunding_ETL/assets/162658233/0e051516-43a4-4db8-932a-d192a6b97b61)
  2. Create a new Postgres database, named crowdfunding_db.
  3. Using the database schema, create the tables in the correct order to handle the foreign keys.
  4. Verify the table creation by running a SELECT statement for each table.
  5. Import each CSV file into its corresponding SQL table.
  6. Verify that each table has the correct data by running a SELECT statement for each.
