# Data Analysis Report: Customer Call List Data Cleaning and Optimization

# Overview
As a data analyst, I conducted a comprehensive data cleaning and optimization project using Python and Pandas within a Jupyter Notebook environment, focusing on the Customer Call List.xlsx dataset. The objective was to prepare a customer contact dataset for effective business use by addressing duplicates, inconsistencies, and irrelevant data. This report details the cleaning process, key insights, and recommendations .

# Data Analysis Process
# Dataset Description
Source: Customer Call List.xlsx containing 21 initial records.
Columns: CustomerID, First_Name, Last_Name, Phone_Number, Address, Paying Customer, Do_Not_Contact, Not_Useful_Column.
Objective: Clean and standardize the dataset to support customer outreach campaigns.
# Data Cleaning Process
1/ Duplicate Removal:
Identified and removed one duplicate entry for CustomerID 1020 (Anakin Skywalker) using df.drop_duplicates().
Result: Reduced dataset to 20 unique records.
2/ Column Elimination:
Dropped the Not_Useful_Column (irrelevant boolean data) twice during the process to ensure a clean dataset, using df.drop(columns="Not_Useful_Column").
Result: Removed unnecessary data, focusing on actionable fields.
3/ Address Standardization:
Replaced 'N/a' values in the Address column with an empty string using df['Address'].replace('N/a','').
Split Address into Street_Address, State, and Zip_Code by parsing commas, then dropped the original Address column.
Result: Structured address data for better geospatial analysis, though Zip_Code data was sparse.
4/ Phone Number Formatting:
Standardized Phone_Number by replacing 'N/a' and NaN with empty strings, and reformatted inconsistent separators (e.g., '/', '|') to '-' using string replacement.
Result: Ensured uniform phone number format for contact purposes.
5/ Categorical Data Normalization:
Standardized Paying Customer and Do_Not_Contact values to 'Y'/'N' format, replacing 'Yes'/'No', 'Y'/'N', and NaN with consistent single characters.
Result: Improved data consistency for filtering and analysis.
6/ Row Filtering:
Removed rows where Do_Not_Contact was 'Y' using a loop with df.drop(), eliminating 4 records (e.g., Abed Nadir, Ron Swanson, Creed Braton).
Result: Reduced dataset to 16 contactable customers.
# Key Findings
Data Quality: Initial dataset contained duplicates, inconsistent formatting (e.g., phone numbers, addresses), and irrelevant columns.
Contactability: 20% of records (4 out of 20) were marked as "Do Not Contact," reducing the effective contact list.
Payment Status: Approximately 60% of remaining customers (10 out of 16) are paying, indicating a strong base for retention efforts.
Address Coverage: Only 2 records included Zip_Code data, limiting detailed location analysis.

3 Recommendations
Data Validation: Implement upfront data entry checks to prevent duplicates and inconsistent formats.
Contact Strategy: Focus outreach on the 16 contactable customers, prioritizing the 10 paying ones for retention campaigns.
Address Enhancement: Collect missing Zip_Code and State data to enable targeted regional marketing.
Automation: Develop a script to automate future data cleaning, reducing manual effort.
# Analytical Skills Demonstrated
Data Cleaning: Expertly handled duplicates, null values, and inconsistent data using Pandas.
Data Transformation: Split and standardized complex fields (e.g., Address) into usable components.
Filtering: Applied conditional logic to exclude non-contactable customers effectively.
Problem-Solving: Addressed data quality issues with practical solutions, enhancing dataset usability.
Programming: Leveraged Python and Jupyter Notebook for scalable data manipulation.
# Conclusion
This project showcases my ability to clean, transform, and optimize a customer dataset using Python and Pandas, delivering a refined contact list for business use. The process highlights my skills in data preprocessing, problem-solving, and analytical thinking. Future enhancements could include integrating additional customer metrics for deeper insights.
