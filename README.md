# Data Cleaning Workflow
Detailed review of the data cleaning workflow for datasets.

## 1. Define Analytical Requirements
Begin by understanding the specific analyses required and the desired outcomes. Clearly define the questions you aim to answer and the problems to be solved. Filter out irrelevant observations, ensuring focus on relevant data subsets, such as SUV owners in a car dataset. Remove extraneous elements like URLs, hashtags, and HTML tags unless integral to the analysis.

## 2. Remove Duplicates
Identify and eliminate duplicate entries using tools like Excel. Removing duplicates is crucial for obtaining well-balanced and accurate results.

* Removing Duplicates

You can either highlight duplicate data, or delete it entirely from the workbook. Using conditional formatting across the entire workbook, duplicate values can be highlighted or by selecting the entire dataset, you can go to Data -> Remove duplicates, checking the relevant boxes for the fields where data should be deleted.

## 3. Fix Structural Errors
Address structural errors such as misspellings, inconsistent naming conventions, improper capitalization, and incorrect word usage. Standardize data elements like 'women' and 'female' columns to ensure uniformity. Also, standardize formats for dates, addresses, phone numbers, etc., enhancing data consistency and aiding computer interpretation. Examples include:
* Extra Spaces using the Cell Reference.

This will remove all leading and tailing spaces as well as the additional spaces found within words (excluding those with only one space).
```
TRIM(text)
```
* Blank cells.

Blank cells in a dataset can be corrected using defaults. By defaulting all blank cells with a common value i.e. "0" or "Not Available". Select all the dataset, press F5, Special, Blanks and fill the dialog box with the required output. Be sure to use Control+Enter to apply to the whole dataset, not just the selected cell.

* Datatype Correction

When recieving datasets, ensure the fields are being read as the correct datatype. I.e. Numbers may be read as a string and further impede downstream analysis. This can be corrected using a blank cell, typing 1, selecting the cell with "1" and Control+C, pasting as special using the multiply operator, this will convert all of the string numbers into numeric values.

* Highlight Errors

Control+A, Conditional formatting, new rule. Use the new formatting rule and format cells that only contain "errors" in the dropdown. This will allow for all errors to be highlighted and either amended/deleted.

Control+A, F5, Special, Formulas, Errors will do the same.

*Lower/uppercase

When you inherit a workbook or import data from text files, often the names or titles are not consistent. Sometimes all the text could be in lower/upper case or it could be a mix of both. You can easily make it all consistent by using these three functions:

```
LOWER() –  Converts all text into Lower Case.
UPPER() – Converts all text into Upper Case.
PROPER() – Converts all Text into Proper Case.
```
* Text to Column
To split up a cell into multiple components i.e. Address/name. You can use the 


## 4. Handle Missing Data
Evaluate missing data's impact on the dataset. Decide whether a column with missing values undermines the entire entry; if so, consider deletion or manual correction. Otherwise, assess whether to amend missing values or leave them unaltered based on the analysis's context.

## 5. Filter Out Data Outliers
Identify and filter out data outliers, ensuring that the dataset's statistical integrity is maintained. Outliers can significantly skew results; removing them enhances the dataset's reliability.

## 6. Validate Data Integrity
Thoroughly validate the data to ensure it meets predefined criteria. Verify that all data elements align with the established standards, ensuring high quality, consistency, and proper formatting. This validation process prepares the data for utilization in SQL and other querying programs, guaranteeing accurate and reliable results.
