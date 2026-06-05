# Supply Chain Analytics Automation using n8n, Supabase & Quadratic

## Project Overview

This project automates the ingestion, storage, and analysis of supply chain data using n8n, Supabase PostgreSQL, and Quadratic.

Supply chain CSV files received through Gmail are automatically processed using n8n workflows, loaded into PostgreSQL hosted on Supabase, and analyzed in Quadratic to generate KPIs and business insights.

---

## Architecture

```text
Gmail (CSV Files)
        ↓
   Gmail Trigger
        ↓
     n8n ETL
        ↓
Supabase PostgreSQL
        ↓
Quadratic Analytics
        ↓
KPI Dashboard & Insights
```

---

## Tech Stack

- n8n
- Gmail Trigger
- PostgreSQL
- Supabase
- Quadratic
- CSV Data Processing

---

## Database Design

### Dimension Tables

- dim_customers
- dim_products
- dim_targets_orders

### Fact Tables

- fact_order_line
- fact_aggregate

---

## ETL Workflow

### Extract

- Automatically monitors Gmail for incoming CSV attachments.
- Reads and extracts supply chain datasets from emails.

### Transform

- Parses CSV files.
- Cleans and structures the data.
- Maps fields to the database schema.
- Creates business metrics such as On-Time, In-Full, and OTIF flags.

### Load

- Loads transformed records into PostgreSQL tables hosted on Supabase.
- Maintains centralized storage for analytics and reporting.

---

## Supply Chain KPIs

The following KPIs were calculated:

- Total Orders
- Total Order Lines
- Line Fill Rate %
- Volume Fill Rate %
- On Time Delivery %
- In Full Delivery %
- OTIF % (On Time In Full)

### KPI Results

| KPI | Value |
|------|------|
| Total Orders | 572 |
| Total Order Lines | 1000 |
| Line Fill Rate | 96.54% |
| Volume Fill Rate | 96.54% |
| On Time Delivery | 71.8% |
| In Full Delivery | 62.3% |
| OTIF | 45.9% |

---

## Customer Analysis

Generated customer-level business insights including:

- Top 5 Customers by Order Value
- Customer OTIF %
- Customer In Full %
- Customer On Time %

### Top Customer Insights

The analysis identified the highest-value customers and evaluated service performance using:

- Order Value
- OTIF %
- IF %
- OT %

---

## Business Value

This solution helps organizations:

- Automate manual data ingestion processes
- Improve data accuracy
- Track supply chain performance
- Monitor delivery effectiveness
- Identify high-value customers
- Support data-driven decision making

---

## Screenshots

### n8n Workflow

![n8n Workflow](screenshots/01_n8n_workflow.png)

### Supabase Database

![Supabase Database](screenshots/02_supabase_database.png)

### KPI Dashboard

![KPI Dashboard](screenshots/03_kpi_dashboard.png)

### Top Customers Table

![Top Customers Table](screenshots/04_top_customers_table.png)

### Top Customers Chart

![Top Customers Chart](screenshots/05_top_customers_chart.png)

---

## Workflow File

The exported n8n workflow is included in this repository:

```text
workflow/n8n_workflow.json
```

---

## Key Learnings

Through this project, I gained hands-on experience in:

- ETL Pipeline Development
- Workflow Automation using n8n
- PostgreSQL Database Management
- Cloud Database Integration using Supabase
- Supply Chain Analytics
- KPI Development
- Data Visualization
- Business Intelligence

---

## Future Enhancements

- Automated Data Validation
- Error Handling Workflows
- Real-Time KPI Monitoring
- Power BI Dashboard Integration
- Advanced Supply Chain Forecasting

---

## Author

Swapnavelan

Aspiring Data Analyst | SQL | PostgreSQL | n8n | Data Analytics | Business Intelligence
