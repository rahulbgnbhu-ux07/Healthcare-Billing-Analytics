# Healthcare Billing Analytics

A data analytics project using **Python, Pandas, SQL, SQLite, and data visualization** to analyze healthcare billing, appointments, patient attendance, and no-show patterns.

## Project Overview

This project demonstrates an end-to-end healthcare data analytics workflow:

**Data Cleaning → Database Design → SQL Analysis → KPI Analysis → Visualization → Business Insights**

The project contains two Jupyter notebooks:

1. `Data_Cleaning_Healthcare_Project.ipynb`
   - Data loading and inspection
   - Duplicate checking and removal
   - Date conversion
   - Data quality checks
   - Preparation of cleaned datasets

2. `Healthcare_Billing_Analytics.ipynb`
   - SQLite database creation
   - Patients and Appointments tables
   - Healthcare Records table
   - SQL-based healthcare analysis
   - Billing analysis
   - Appointment and no-show analysis
   - KPI generation
   - Data visualization
   - Final business insights

## Key Areas of Analysis

### Appointment & No-Show Analysis

The project analyzes:

- Overall appointment attendance
- No-show rate
- No-show patterns by gender
- SMS reminders and no-show rates
- Waiting time and no-show behavior
- Neighbourhood-level analysis
- Patient appointment history
- Patients with mixed attendance
- Monthly appointment trends
- Hospital-level analysis

The dataset contains **110,527 appointments**, with an overall no-show rate of **20.19%**.

### Healthcare Billing Analysis

Billing analysis includes:

- Billing by medical condition
- Billing by insurance provider
- Billing by admission type
- Average billing analysis
- Highest-billing records
- Condition and admission-type comparisons
- Provider and condition analysis
- Provider × condition analysis
- Billing distribution
- Percentage contribution
- Comparison with overall average billing

## SQL Techniques Used

The project uses SQLite and demonstrates several SQL concepts:

- `SELECT`
- `WHERE`
- `GROUP BY`
- `HAVING`
- `ORDER BY`
- `JOIN`
- Subqueries
- Common Table Expressions (CTEs)
- Window functions
- `RANK()`
- `ROW_NUMBER()`
- `LAG()`
- `LEAD()`
- Running totals
- Percentage contribution
- Aggregation functions

## Key Billing Results

The healthcare billing dataset contains:

| Metric | Result |
|---|---:|
| Healthcare records | 54,966 |
| Medical conditions | 6 |
| Insurance providers | 5 |
| Total billing | ~$1.404 billion |
| Average billing | ~$25,544 |
| Minimum billing | -$2,008.49 |
| Maximum billing | $52,764.28 |

### Major Findings

- **Diabetes** has the highest total billing among the medical conditions.
- **Obesity** has the highest average billing per record.
- **Cigna** has the highest total billing among the insurance providers.
- Billing varies across medical conditions, admission types, and insurance providers.
- Average billing differences between groups are relatively small compared with differences in total billing.
- The analysis identified a negative billing value of approximately **-$2,008.49**, which should be investigated as a potential data-quality issue.

## Data Cleaning

The data cleaning notebook performs preprocessing before the SQL analysis.

The workflow includes:

- Loading healthcare and appointment datasets
- Checking duplicate records
- Comparing statistics before and after cleaning
- Converting date columns
- Checking invalid values
- Preparing final cleaned datasets

The cleaned datasets are then used to create the SQLite database for analysis.

## Database Structure

The analytics notebook creates a SQLite database containing:

```text
Patients
    │
    └── Appointments

Healthcare_Records
