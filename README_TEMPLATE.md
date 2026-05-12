 # 📊 CUSTOMER SHOPPING DATA ANALYSIS REPORT
> This project presents an analysis of customer shopping behavior based on transactional data. The objective is to clean, analyze, and visualize the dataset to uncover meaningful insights that can support business decision-making.
The analysis focuses on identifying sales trends, customer preferences, and factors influencing revenue generation.
***

---
## Table of Contents
1. [Project Overview](#1-project-overview)
2. [Objectives](#2-objectives)
3. [Project Scope & Tools](#3-project-scope--tools)
4. [Repository Structure](#4-repository-structure)
5. [Data Workflow](#5-data-workflow)
6. [Data Model & Schema](#6-data-model--schema)
7. [Analysis & Metrics](#8-analysis--metrics)
8. [Key Insights](#9-key-insights)
9. [Recommendations](#10-recommendations)
10. [Assumptions & Limitations](#11-assumptions--limitations)
11. [Future Enhancements](#12-future-enhancements)
12. [Deliverables](#13-deliverables)
13. [Author](#14-author)

---

## 1. Project Overview

<!--
  Write 3–5 sentences in plain language.
  Cover: context → problem → approach → outcome.
  Read it out loud. If it sounds like a form - rewrite it.

  WHAT GOOD LOOKS LIKE:
  "A mid-size retail business was seeing inconsistent revenue across
  its regional stores but couldn't identify the root cause. This project
  explored 18 months of transaction data across five regions to determine
  whether underperformance was driven by sales volume, pricing, or return
  rates. The analysis revealed that one region's gap was almost entirely
  explained by an unusually high return rate on a single product category -
  a finding invisible in the company's top-level reporting."

  WHAT TO AVOID:
  "This project analyzes sales data to find trends and insights."
  (Too vague. Could describe 10,000 projects. Describes none of them.)
-->

**Context:** Retail businesses generate large volumes of transactional data daily, but without proper analysis, valuable insights about customer behavior, sales performance, and purchasing trends can remain hidden. This project was developed to explore customer shopping patterns and transform raw sales data into meaningful business intelligence that supports data-driven decision-making.

**Problem Statement:** The primary challenge was to identify key trends, customer preferences, and performance drivers within the shopping dataset. The project aimed to answer questions such as:

Which product categories perform best?
What trends exist over time?
Which customer segments contribute most to sales?
What factors influence revenue generation?

**Approach:** The project was completed using Microsoft Excel by following a structured data analysis workflow. The dataset was cleaned and standardized, analyzed using pivot tables and calculated metrics, and visualized through an interactive dashboard featuring KPIs, charts, and slicers.

**Outcome:** The project produced a cleaned and analysis-ready dataset, an interactive Excel dashboard, business insights, and strategic recommendations. The analysis revealed sales trends, high-performing categories, customer purchasing behavior, and payment preferences that can help improve business strategy and decision-making.

---

## 2. Objectives

<!--
  Write objectives that are specific enough to succeed or fail.
  Use action-oriented verbs: Identify, Determine, Quantify, Build, Evaluate.

  WHAT GOOD LOOKS LIKE:
  ✅ "Determine whether customer churn rate correlates with support ticket volume."
  ✅ "Identify the top three revenue-driving product categories across all regions."
  ✅ "Build a reproducible pipeline that ingests and cleans daily sales exports."

  WHAT TO AVOID:
  ❌ "Explore the data."
  ❌ "Gain insights."
  ❌ "Understand trends."
  (These can't fail - which means they can't succeed either.)
-->

- **Primary Objective:** To analyze customer shopping data in order to uncover sales trends, customer behavior patterns, and key business performance insights that support data-driven decision-making.
- **Secondary Objective 1:** To clean and transform raw transactional data into a structured and analysis-ready dataset using Excel data cleaning techniques.
- **Secondary Objective 2:** To develop an interactive dashboard that visualizes key metrics such as total sales, category performance, customer segments, and payment method distribution.
- **Secondary Objective 3:** To generate actionable business insights and recommendations that can help improve marketing strategies, inventory management, and overall business performance.

> 💡 *Every analysis decision in this project traces back to one of these objectives.*

---

## 3. Project Scope & Tools

### Scope

<!--
  WHAT GOOD LOOKS LIKE:
  In Scope: "Transaction-level data for Regions A–E, Jan 2023–Jun 2024.
             Analysis covers revenue, return rates, and product category performance."
  Out of Scope: "Customer demographics and marketing spend data were excluded -
                 demographic data was incomplete for two regions, and marketing
                 data sits in a separate system outside this engagement."

  WHAT TO AVOID:
  ❌ Leaving Out of Scope blank. This is the section that protects your credibility.
     If you don't define the fence, reviewers assume you missed things.
-->

| Dimension | Details |
|-----------|---------|
| **In Scope** | Customer transactional data analysis including sales trends, customer demographics, product category performance, payment methods, and shopping mall performance using Excel-based analysis and dashboarding. |
| **Out of Scope** | Predictive modeling, machine learning, real-time data integration, and external market/economic analysis were excluded due to limited dataset scope and project requirements. |
| **Time Period** | The dataset covers customer shopping transactions recorded within the available invoice date range provided in the dataset.
| **Granularity** | Transaction-level analysis where each row represents an individual customer purchase/invoice record. |

### Tools & Technologies

<!--
  List only what you actually used on this project.
  This is not your skills section - it's the project's technical context.
-->

| Category | Tool(s) Used |
|----------|-------------|
| Data Storage | CSV Files, Excel Workbook |
| Data Processing | Microsoft Excel, Power Query |
| Analysis | Pivot Tables, Excel Functions, Aggregations|
| Visualization | Excel Charts, Dashboard, Slicers |
| Version Control | Git / GitHub |
| Documentation | Markdown (README.md), Microsoft Word |
| Other | PowerPoint Presentation for project communication |

---

## 4. Repository Structure

```
customer-shopping-analysis/
│
├── data/
│   ├── raw/                  
│   │   └── customer_shopping_data.csv
│   │        # Original unmodified transactional dataset
│   │
│   ├── processed/            
│      └── cleaned_customer_data.xlsx
│        # Cleaned and transformed dataset used for analysis
│
├── scripts/                  
│   └── excel_cleaning_steps.md
│        # Documented reusable cleaning procedures
│
├── reports/                  
│   ├── customer_shopping_report.docx
│   ├── customer_shopping_report.pdf
│   └── customer_shopping_presentation.pptx
│        # Final project documentation and presentation
│
├── visuals/                  
│   ├── dashboard_screenshot.png
│   ├── sales_by_category_chart.png
│   └── payment_distribution_chart.png
│        # Exported dashboard visuals and charts
│
├── docs/                     
│   ├── data_dictionary.md
│   ├── project_notes.md
│   └── dashboard_design_notes.md
│        # Supporting documentation and referencese
│
└── README.md                 
     # Main project documentation
```

## 5. Data Workflow

<!--
  Show how data moved through your project - from source to output.
  Every transformation decision should be traceable here.

  WHAT GOOD LOOKS LIKE:
  1. Source: "Monthly CSV exports pulled from the internal POS system.
              Five files, one per region, covering Jan 2023–Jun 2024."
  2. Ingestion: "Loaded into Python using pandas. Files concatenated into
                 a single dataframe (approx. 340,000 rows)."
  3. Cleaning: "Removed 1.2% of rows with null transaction IDs.
                Standardised date formats across regional files.
                Resolved product category naming inconsistencies (3 variants → 1)."
  4. Transformation: "Created a returns_rate field at product-category level.
                      Aggregated to weekly and regional grain for trend analysis."
  5. Analysis: "Descriptive statistics, regional comparison, return rate
                segmentation by product category."
  6. Output: "Summary report (PDF), annotated notebook, processed CSV."

  WHAT TO AVOID:
  ❌ "Data was cleaned and analysed." (No chain. No decisions. No trust.)
-->

```
[Raw Data]
   ↓
[Data Cleaning]
   ↓
[Data Transformation]
   ↓
[Exploratory Analysis]
   ↓
[Dashboard Creation]
   ↓
[Insight Generation]
   ↓
[Business Recommendations]
```

1. **Source:** The dataset used for this project consists of customer shopping transaction records stored in CSV/Excel format. The data contains information such as invoice number, customer demographics, product categories, quantity purchased, price, payment methods, shopping malls, and transaction dates.
Format: CSV / Excel
Data Type: Structured transactional data.
Size: Multi-row customer purchase dataset.
Access Method: Imported directly into Microsoft Excel for analysis.
2. **Ingestion:** The dataset was imported into Microsoft Excel using:
Excel file import tools.
Power Query for structured loading and transformation.
The raw dataset was preserved in a separate worksheet to maintain data integrity.
3. **Cleaning:** Several data quality issues were identified and corrected during the cleaning process:
Issues Fixed:
a. Removed duplicate transaction records.
b. Standardized inconsistent text formatting.
   Example: “female” → “Female”
c. Corrected capitalization inconsistencies.
d. Applied proper date formatting.
e. Verified and corrected data types:
   Numbers,Text, & Dates.

5. **Removed unnecessary spaces and hidden characters using:**
TRIM(), PROPER(), & CLEAN()

Missing Values:
No significant missing values were identified in the dataset.

6. **Transformation:** Additional transformations were performed to support analysis and dashboard development.\\
   
New Fields Created:
Total Sales
            Total Sales = Quantity × Price

   Data Structuring:
   Organized data into analysis-ready tables.
   Created summary tables using Pivot Tables.
   
   Grouped data by:
   Category, Gender, Shopping Mall, Payment Method, & Time Period.

7. **Analysis:** The dataset was analyzed using descriptive and visual analysis techniques.
   Analysis Methods:
   Pivot Table Analysis.

   Aggregations:
   SUM, COUNT,
   AVERAGE, Trend Analysis, Comparative Category Analysis, Customer Segmentation, Dashboard Visualization, & Visual Analysis.

   The following visualizations were created:
   Bar Charts, Line Charts, Pie Charts, & KPI Cards.

8. **Output:** The final outputs of the project include:

   Excel Deliverables:
   Raw_Data Sheet, Clean_Data Sheet, Analysis Sheet, & Interactive Dashboard.

   Documentation:
   Project Report (Word/PDF) & GitHub README Documentation.

   Presentation:
   PowerPoint Slide Deck.

   **Business Outcomes**
   The analysis provided actionable insights into:
   Sales performance, Customer behavior Category, profitability, Payment preferences & Location-based performance trends.

---

## 6. Data Model & Schema

### Dataset / Table: `Customer_shopping_data`
| Field Name | Data Type | Description | Example Value |
|------------|-----------|-------------|---------------|
| `invoice_no` | string  | Unique identifier for each transaction/invoice | I138884 |
| `customer_id` | string  | Unique identifier assigned to each customer | C241288 |
| `gender` | string  | Gender of the customer | Female|
| `age` |  int  | Customer age | 28 |
| `category` | string | Product category purchased by the customer | Clothing |
| `quantity` |  int  | Number of units purchased in a transaction | 3 |
| `price` |  float | Unit price of the product purchased | 1500.50 |
| `payment_method` | string | Payment option used for the transaction | Credit Card |
| `shopping_mall` | string | Shopping mall/location where purchase occurred | Mall of Istanbul |
| `invoice_date` | date | Date the transaction occurred | 2023-03-15 |
| `invoice_year` |  int | Year the transaction occurred(Extracted from invoice_date) | 2023 |
| `invoice_month` | string | Month the transaction occurred (Extracted from Invoice_date) | January |
| `age_group` |  int | Age group of the customer (Ranging from 18 - 69, with interval of 10. Calaculated from age.) | 18-27 |
| `total_sales` | float | Calculated total transaction value (quantity × price) | 4501.50 |
> **Row count (approx.):** ~99,000+ rows.
> **Date range:** Based on available invoice transaction dates in the dataset.
> **Primary Key:** invoice_no.
> **Calculated Field:** total_sales = quantity × price

---

## 7. Analysis & Metrics

### Analytical Approach

This project followed an exploratory and descriptive data analysis approach to understand customer shopping behavior and sales performance. The analysis focused on identifying patterns, trends, and relationships within the transactional dataset rather than testing a formal statistical hypothesis.

The workflow included:
a. Cleaning and validating raw transactional data.
b. Exploring sales performance across categories, locations, and customer demographics.
c. Comparing customer purchasing behavior across segments.
d. Visualizing KPIs and trends through an interactive dashboard.
d. Generating actionable business insights and recommendations.

The analysis was designed to answer business-focused questions such as:
a. Which product categories generate the most revenue?
b. Which customer segments contribute most to sales?
c. Are there seasonal trends in purchasing behavior?
d. Which payment methods are most preferred?
e. Which shopping locations perform best?

### Key Metrics Defined

| Metric | Plain-Language Definition | Why It Matters |
|--------|--------------------------|----------------|
| `Total Sales` | The total revenue generated from all transactions (Quantity × Price) | Measures overall business performance and revenue generation |
| `Number of Customer` | The total number of customer records/invoices | Helps evaluate transaction volume and customer activity |
| `Average Order Value (AOV)` | The average amount spent per transaction | Indicates customer spending behavior and purchasing power |
| `Quantity Sold` | Total number of products/items purchased | Measures product demand and sales volume|
| `Sales by Category` | Revenue generated by each product category | Helps identify best- and worst-performing product groups |
| `Sales by Shopping Mall` | Revenue contribution from each shopping location | Supports location-based business decisions |
| `Payment Method Distribution` | Frequency of each payment method used | Helps understand customer payment preferences |
| `Customer Segment Contribution` | Sales contribution grouped by customer demographics (e.g., gender, age) | Supports targeted marketing and segmentation strategies |

### Methods Used

Descriptive Analysis
Summary statistics
Revenue aggregation
Transaction counting
Average calculations
Trend Analysis
Sales trend analysis across transaction dates
Time-based performance comparison

Segmentation & Group Comparison
Customer segmentation by:
Gender
Age group
Shopping location
Product category performance comparison

Visual Analysis
Bar charts for category comparison
Line charts for sales trends
Pie charts for payment method distribution
KPI cards for business performance indicators

Data Transformation & Aggregation
Pivot Tables for summarization

Custom calculated field:
Total Sales = Quantity × Price
Dashboard Techniques
Interactive slicers and filters

KPI highlighting
Conditional formatting for performance emphasis

Excel Functions Used
SUM()
AVERAGE()
COUNT()
IF()
IFERROR()
TRIM()
PROPER()
CLEAN()
---

## 8. Key Insights

<!--
  Findings + implications. Not just what happened - what it means.

  WHAT GOOD LOOKS LIKE:
  ✅ "Return rates, not sales volume, explain Region A's underperformance.
      Region A's return rate on home goods was 34% - more than double the
      company average. Revenue was not lost at the point of sale; it was
      lost post-sale through refunds. This points to a fulfilment or
      product quality issue specific to that region, not a demand problem."

  WHAT TO AVOID:
  ❌ "Region A had lower revenue than other regions in Q4."
     (That's an observation. It describes what happened.
      An insight says what it means and where to look next.)

  Aim for 3–6 insights. Quality over quantity.
-->

**Insight 1: [Short descriptive headline]**
[What you found + what it suggests. One short paragraph.]

**Insight 2: [Short descriptive headline]**
[What you found + what it suggests.]

**Insight 3: [Short descriptive headline]**
[What you found + what it suggests.]

**Insight 4 (if applicable): [Short descriptive headline]**
[What you found + what it suggests.]

---

## 9. Recommendations

<!--
  Action-oriented. Addressed to a real audience.
  Tied explicitly to the insight that supports each one.

  WHAT GOOD LOOKS LIKE:
  Priority: High
  Recommendation: "Conduct a fulfilment audit for home goods deliveries
                   in Region A - specifically investigating whether returns
                   correlate with a particular warehouse, carrier, or SKU batch."
  Based On: Insight 1 - return rate anomaly in Region A
  Owner: Operations / Supply Chain team

  WHAT TO AVOID:
  ❌ "Improve the return rate."
     (Not actionable. Doesn't say who, how, or where to start.)
  ❌ "Further analysis is needed."
     (This is a placeholder, not a recommendation.)
-->

| Priority | Recommendation | Based On | Suggested Owner |
|----------|---------------|----------|-----------------|
| High | [Specific, actionable step] | [Insight it comes from] | [Who should act] |
| Medium | [Specific, actionable step] | [Insight it comes from] | [Who should act] |
| Low | [Exploratory or longer-term suggestion] | [Insight it comes from] | [Who should act] |

---

## 10. Assumptions & Limitations

<!--
  WHAT GOOD LOOKS LIKE:
  Assumption: "Transaction records were assumed to be complete for all five regions.
               No validation was performed against source system record counts."
  Limitation: "The analysis cannot distinguish between returns initiated by
               the customer vs. returns initiated by the business (e.g., recalls).
               If business-initiated returns are concentrated in Region A, the
               return rate finding may reflect a policy decision, not a quality issue."

  WHAT TO AVOID:
  ❌ Leaving this section blank or writing "None known."
     Every project has limitations. Documenting them is a sign of
     analytical maturity - not a confession of failure.
-->

### Assumptions
- [What did you treat as true without being able to verify?]
- [What simplifications did you make for scope or feasibility?]
- [What domain rules or definitions did you accept as given?]

### Limitations
- [What gaps exist in the data?]
- [What analysis was out of scope but could affect interpretation?]
- [What would a more rigorous version of this project include?]
- [Are there known biases in the data source or collection method?]

> *The goal here is pre-emptive Q&A. What would a thoughtful skeptic push back on? Document the answer here, before they ask.*

---

## 11. Future Enhancements

<!--
  WHAT GOOD LOOKS LIKE:
  ✅ "Automate the monthly data pull from the POS export folder using
      a scheduled Python script, replacing the current manual process."
  ✅ "Expand the return rate analysis to include carrier-level data,
      which was unavailable in this dataset but exists in the logistics system."

  WHAT TO AVOID:
  ❌ "Add a machine learning model."
     (Vague, and disconnected from the actual findings of this project.)
  ❌ Listing aspirational features that don't follow logically from the work.
-->

- [ ] [Enhancement 1 - specific and traceable to a real gap in this project]
- [ ] [Enhancement 2]
- [ ] [Enhancement 3]
- [ ] [Enhancement 4]

---

## 12. Deliverables

| Deliverable | Description | Location |
|-------------|-------------|----------|
| [Name] | [What it contains] | [`/path/to/file`] |
| [Name] | [What it contains] | [`/path/to/file`] |
| [Name] | [What it contains] | [`/path/to/file`] |

---

## 13. Author

**[Your Name]**
[Your role or title - current or target]

- 🔗 [LinkedIn URL]
- 💼 [Portfolio or GitHub profile URL]
- 📧 [Email - optional]

---

*Last updated: [Month YYYY]*
*If this template helped you, consider starring the repository.*
