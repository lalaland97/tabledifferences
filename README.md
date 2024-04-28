Executive Summary: Data Comparison Tool

Purpose:
The Data Comparison Tool is designed to efficiently compare two sets of tabular data stored in CSV files or obtained through teradata. Its primary objectives are to identify:

-Duplicate primary keys within each dataset.
-Missing rows in either dataset.
-Differences between the datasets in terms of column values.

Functionality:
Loading Data: The tool allows users to load two CSV files containing tabular data into Pandas DataFrames.
Primary Key Validation: It ensures that a specified primary key or keys exist in both datasets. If not, it raises a ValueError.
Duplicate Check: The tool checks for duplicate primary keys within each dataset and raises an error if duplicates are found.
Data Comparison: It compares the datasets, identifying differences in column values between rows sharing the same primary key.
Missing Data Identification: The tool identifies rows present in one dataset but missing in the other, providing clarity on data completeness.
Reporting: It generates a comprehensive report summarizing the identified differences, missing rows, and any duplicate primary keys.
Output: The tool saves the generated report to a CSV file for further analysis and reference.

Usage:
1)Load two CSV files containing tabular data from any source.
2)Specify the primary key column name(s) to be used for comparison.
3)Run the tool, which will perform the comparison and generate a detailed report.
4)Review the report to gain insights into differences, missing rows, and data integrity issues between the datasets.

Benefits:
Enhances data quality assurance processes by automating the comparison of large datasets.
Saves time and effort by quickly identifying discrepancies and missing data.
Facilitates data reconciliation and ensures consistency across datasets.

Conclusion:
The Data Comparison Tool streamlines the process of comparing tabular data from any source, enabling users to quickly identify discrepancies and ensure data integrity. By automating the comparison process and providing detailed reports, the tool empowers users to make informed decisions based on accurate and consistent data.
