# HCP Master Data Quality & Governance

**A Data Quality and Governance Project inspired by pharmaceutical commercial data management workflows.**

## Project Overview

Healthcare Professional (HCP) data plays an important role in pharmaceutical companies. Accurate and reliable HCP information helps organizations maintain effective customer records, improve data management, and ensure responsible marketing outreach.

This project demonstrates how to identify, validate, and monitor common HCP master data quality issues using Python, SQL, and data analysis.

The project focuses on improving data completeness, validity, uniqueness, consistency, and timeliness while checking marketing outreach against opt-out records.

## Business Problem

Pharmaceutical companies manage large volumes of Healthcare Professional information. Inaccurate or duplicate records can lead to:

- Incomplete HCP profiles.
- Duplicate healthcare professional records.
- Invalid phone numbers and postal codes.
- Inconsistent location information.
- Outdated or inactive provider records.
- Marketing outreach to opted-out HCPs.

This project demonstrates a structured approach to identifying these problems and generating actionable data quality reports.

## Project Objectives

- Validate HCP master data.
- Identify missing and invalid information.
- Detect duplicate NPI records.
- Identify inconsistent provider information.
- Check provider status and data timeliness.
- Detect marketing outreach violations using opt-out records.
- Generate data quality reports for monitoring.

## Technology Stack

| Technology | Purpose |
|---|---|
| Python | Data processing and validation |
| Pandas | Data cleaning and analysis |
| SQL | Data quality checks and queries |
| SQLite | Structured data storage |
| Excel | Data dictionary and documentation |
| Power BI | Dashboard development (next step) |

## Data Quality Checks

| Dimension | Validation |
|---|---|
| Completeness | Missing specialty and address |
| Validity | Invalid ZIP codes and phone numbers |
| Uniqueness | Duplicate NPI numbers |
| Consistency | State and ZIP code mismatches |
| Timeliness | Inactive or deactivated provider records |
| Compliance | Marketing outreach against opt-out records |

## Project Workflow

1. Load HCP master data.
2. Validate mandatory fields.
3. Identify missing and invalid records.
4. Detect duplicate provider identifiers.
5. Check provider status.
6. Compare marketing outreach records against the opt-out list.
7. Generate a data quality issue register.
8. Store results in CSV files and an SQLite database.
9. Prepare the results for dashboard visualization.

## Repository Structure

```text
hcp-master-data-quality-governance/
│
├── data/
│   ├── hcp_sample.csv
│   ├── synthetic_opt_outs.csv
│   └── marketing_outreach_sample.csv
│
├── src/
│   └── run_pipeline.py
│
├── sql/
│   └── quality_checks.sql
│
├── reports/
│   ├── data_quality_issues.csv
│   ├── quality_summary.csv
│   ├── hcp_quality.db
│   └── run_summary.txt
│
├── docs/
│   └── data_dictionary.xlsx
│
├── requirements.txt
├── .gitignore
└── README.md
```

## How to Run the Project

**1. Clone the repository**

```bash
git clone https://github.com/chandravarma21/hcp-master-data-quality-governance.git
```

**2. Navigate to the project directory**

```bash
cd hcp-master-data-quality-governance
```

**3. Install dependencies**

```bash
pip install -r requirements.txt
```

**4. Run the pipeline**

```bash
python src/run_pipeline.py
```

**5. Review the output**

Check the generated reports in the `reports/` directory.

## Sample Results

The current demonstration uses synthetic sample data.

| Metric | Result |
|---|---:|
| HCP records processed | 10 |
| Data quality issue rows | 8 |
| HCPs with data quality issues | 5 |
| Opt-out outreach violations | 3 |
| Illustrative quality score | 50% |

*These results demonstrate the validation workflow and are not actual Sanofi business data or performance metrics.*

## Business Impact

This project demonstrates how data quality management can help pharmaceutical organizations:

- Improve HCP master data accuracy.
- Reduce duplicate records.
- Identify incomplete provider profiles.
- Improve data reliability.
- Support compliant
