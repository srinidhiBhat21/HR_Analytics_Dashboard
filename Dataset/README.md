# HR Analytics Dataset

## 📌 Overview

This folder contains the source data used for the HR Analytics Dashboard project built using Microsoft Power BI.

The dataset supports the analysis of workforce composition, employee satisfaction, income, employment type, training frequency, and work-life balance.

##  Dataset Details

- **Employee records:** 1,480
- **Columns:** 16
- **Department lookup entries:** 5
- 
##  Department Lookup

The `Department.xlsx` file maps department IDs to department names.

The department categories include:

- Sales
- Marketing
- Human Resource
- Tech
- Commercial

Use the department ID to connect the employee dataset to the department lookup table.

##  Data Preparation

The following preparation steps are recommended before analysis:

1. Import the CSV using Power BI's **Get Data → Text/CSV** option.
2. Check data types for all columns.
3. Convert `Hire_Date` into a Date data type.
4. Standardize gender labels, such as `M` and `Male`, and `F` and `Female`, after confirming the intended mapping.
5. Check for duplicate employee IDs.
6. Validate missing values and inconsistent categories.
7. Create a relationship between `HRDATASET[Dept_ID]` and `Department[Department_ID]`.
8. Verify employee counts and income calculations before building visuals.

## Potential Analysis

The dataset can be used to explore:

- Employee distribution by department
- Permanent versus contractual employees
- Monthly income patterns
- Job satisfaction ratings
- Work-life balance ratings
- Company environment ratings
- Training frequency
- Age and hiring-date distributions
- Workforce composition by country and grade

