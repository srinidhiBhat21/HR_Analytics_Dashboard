# HR Analytics Dashboard | Power BI

## 📌 Overview

The HR Analytics Dashboard is an interactive Power BI report designed to explore workforce data and present HR-related metrics in a clear, visual format.

The dashboard uses employee data from `HRDATASET.csv` and department information from `Department.xlsx`.

It demonstrates the use of business intelligence tools to organize workforce information and support descriptive analysis.

## 🛠️ Tools Used

- Microsoft Power BI
- Power Query
- DAX (Data Analysis Expressions)
- CSV data source
- Microsoft Excel

##  Dashboard Objectives

- Summarize workforce information using KPIs.
- Compare employee counts across departments.
- Explore income patterns across employee groups.
- Analyze job satisfaction and work-life balance ratings.
- Examine company environment ratings and training frequency.
- Enable interactive exploration using filters and slicers.

##  Suggested Dashboard Components

The available dataset supports the following visuals, depending on the report implementation.

### 1. KPI Cards
Display high-level workforce metrics, such as:
- Total Employees
- Average Monthly Income
- Permanent Employees
- Contractual Employees

### 2. Department Analysis
Use bar charts to compare employee distribution across departments.

### 3. Employment Type Analysis
Compare permanent and contractual employee counts.

### 4. Income Analysis
Explore monthly income by department, grade, or employment type.

### 5. Employee Satisfaction
Visualize job satisfaction and company environment ratings.

### 6. Work-Life Balance
Compare the distribution of work-life balance ratings.

### 7. Training Analysis
Explore the recorded training frequency across employee groups.

### 8. Workforce Demographics
Use charts to examine employee age distribution and hiring-date patterns.

## 📐 Example DAX Measures

The following measures are examples. Adjust the table and column names if your Power BI model uses different names.

### Total Employees

```dax
Total Employees =
DISTINCTCOUNT(HRDATASET[Employee_ID])
```

### Average Monthly Income

```dax
Average Monthly Income =
AVERAGE(HRDATASET[MonthlyIncome])
```

### Permanent Employees

```dax
Permanent Employees =
CALCULATE(
    DISTINCTCOUNT(HRDATASET[Employee_ID]),
    HRDATASET[Job Type] = "Permanent"
)
```

### Contractual Employees

```dax
Contractual Employees =
CALCULATE(
    DISTINCTCOUNT(HRDATASET[Employee_ID]),
    HRDATASET[Job Type] = "Contractual"
)
```

## Data Model

The dashboard uses two source files:

- `HRDATASET.csv`
- `Department.xlsx`

Recommended relationship:

`HRDATASET[Dept_ID]` → `Department[Department_ID]`

The department lookup should contain one unique row per department ID. Use a one-to-many relationship from the department lookup to the employee table where appropriate.

##  Skills Demonstrated

- Data cleaning and transformation
- Data modeling and relationships
- DAX measure creation
- KPI development
- Data visualization
- Dashboard design
- Business-oriented HR analysis


