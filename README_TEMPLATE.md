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
7. [Analysis & Metrics](#7-analysis--metrics)
8. [Key Insights](#8-key-insights)
9. [Recommendations](#9-recommendations)
10. [Assumptions & Limitations](#10-assumptions--limitations)
11. [Future Enhancements](#11-future-enhancements)
12. [Deliverables](#12-deliverables)
13. [Author](#14-author)

---

## 1. Project Overview


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


- **Primary Objective:** To analyze customer shopping data in order to uncover sales trends, customer behavior patterns, and key business performance insights that support data-driven decision-making.
- **Secondary Objective 1:** To clean and transform raw transactional data into a structured and analysis-ready dataset using Excel data cleaning techniques.
- **Secondary Objective 2:** To develop an interactive dashboard that visualizes key metrics such as total sales, category performance, customer segments, and payment method distribution.
- **Secondary Objective 3:** To generate actionable business insights and recommendations that can help improve marketing strategies, inventory management, and overall business performance.

> 💡 *Every analysis decision in this project traces back to one of these objectives.*

---

## 3. Project Scope & Tools

### Scope

| Dimension | Details |
|-----------|---------|
| **In Scope** | Customer transactional data analysis including sales trends, customer demographics, product category performance, payment methods, and shopping mall performance using Excel-based analysis and dashboarding. |
| **Out of Scope** | Predictive modeling, machine learning, real-time data integration, and external market/economic analysis were excluded due to limited dataset scope and project requirements. |
| **Time Period** | The dataset covers customer shopping transactions recorded within the available invoice date range provided in the dataset.
| **Granularity** | Transaction-level analysis where each row represents an individual customer purchase/invoice record. |

### Tools & Technologies


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

4. **Removed unnecessary spaces and hidden characters using:**
TRIM(), PROPER(), & CLEAN()

   Missing Values:
   No significant missing values were identified in the dataset.

5. **Transformation:** Additional transformations were performed to support analysis and dashboard development.\\
   
   New Fields Created:
   Total Sales:
            Total Sales = Quantity × Price

   Data Structuring:
   Organized data into analysis-ready tables.
   Created summary tables using Pivot Tables.
   
   Grouped data by:
   Category, Gender, Shopping Mall, Payment Method, & Time Period.

6. **Analysis:** The dataset was analyzed using descriptive and visual analysis techniques.
   Analysis Methods:
   Pivot Table Analysis.

   Aggregations:
   SUM, COUNT,
   AVERAGE, Trend Analysis, Comparative Category Analysis, Customer Segmentation, Dashboard Visualization, & Visual Analysis.

   The following visualizations were created:
   Bar Charts, Line Charts, Pie Charts, & KPI Cards.

7. **Output:** The final outputs of the project include:

   Excel Deliverables:
   Raw_Data Sheet, Clean_Data Sheet, Analysis Sheet, & Interactive Dashboard.

   Documentation:
   Project Report (Word/PDF) & GitHub README Documentation.

   Presentation:
   PowerPoint Slide Deck.

8. **Business Outcomes:**
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

**The workflow included:**

1. Cleaning and validating raw transactional data.

2. Exploring sales performance across categories, locations, and customer demographics.

3. Comparing customer purchasing behavior across segments.

4. Visualizing KPIs and trends through an interactive dashboard.

5. Generating actionable business insights and recommendations.


**The analysis was designed to answer business-focused questions such as:**

1. Which product categories generate the most revenue?

2. Which customer segments contribute most to sales?

3. Are there seasonal trends in purchasing behavior?

4. Which payment methods are most preferred?

5. Which shopping locations perform best?

---

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

1. Descriptive Analysis
2. Summary statistics
3. Revenue aggregation
4. Customer counting
5. Average calculations
6. Trend Analysis
7. Time-based performance comparison
8. Segmentation & Group Comparison

**Customer segmentation by:**
1. Gender
2. Age group
3. Shopping location
4. Product category performance comparison

**Visual Analysis**
1. Bar charts for category comparison
2. Line charts for sales trends
3. Pie charts for payment method distribution
4. KPI cards for business performance indicators
5. Data Transformation & Aggregation
6. Pivot Tables for summarization

**Custom calculated field:**
1. Total Sales = Quantity × Price
2 Dashboard Techniques
3 Interactive slicers and filters

**KPI highlighting**
  Conditional formatting for performance emphasis

**Excel Functions Used**
1. SUM()
2. AVERAGE()
3. COUNT()
4. IF()
5. IFERROR()
6. TRIM()
7. PROPER()
8. CLEAN()

---

## 8. Key Insights

**Insight 1: Clothing and Shoes Dominate Revenue Generation**
The analysis revealed that the Clothing and Shoes categories generated the highest share of total sales compared to other product categories. This suggests that customers consistently spend more on fashion-related products, making these categories key revenue drivers for the business. The strong performance indicates an opportunity to prioritize inventory availability, promotions, and targeted marketing campaigns within these product segments.

**Insight 2: Customer Purchasing Behavior Shows Seasonal Trends**
Sales performance fluctuated across different transaction periods, with noticeable increases during certain months. This pattern suggests the presence of seasonal buying behavior, likely influenced by holidays, promotional periods, or consumer shopping cycles. Understanding these trends can help businesses better plan marketing campaigns, staffing, and inventory management during peak demand periods.

**Insight 3: Female Customers Contribute More to Total Sales**
Customer segmentation analysis showed that female customers accounted for a larger proportion of transactions and overall revenue. This suggests that female shoppers are either purchasing more frequently or spending more per transaction across multiple product categories. The finding highlights the importance of designing personalized campaigns and product offerings tailored toward this customer segment.

**Insight 4 (if applicable): Credit Card Payments Are the Preferred Transaction Method**
The payment method analysis showed that credit cards were used more frequently than other payment options. This indicates that customers prefer convenient and flexible payment methods, especially for higher-value purchases. The trend suggests that businesses can improve customer experience and potentially increase sales by offering card-related incentives such as cashback offers, discounts, or loyalty rewards.
 

---

## 9. Recommendations


| Priority | Recommendation | Based On | Suggested Owner |
|----------|---------------|----------|-----------------|
| High | Increase inventory levels and promotional campaigns for high-performing categories such as Clothing and Shoes. | Insight 1: Clothing and Shoes dominate revenue generation | Sales & Inventory Management Team |
| High | Develop targeted marketing campaigns focused on female customers to improve engagement and customer retention. | Insight 3: Female customers contribute more to total sales | Marketing Team |
| High | Plan seasonal marketing campaigns and inventory allocation ahead of peak shopping periods. | Insight 2: Customer purchasing behavior shows seasonal trends | Marketing & Operations Team |
| Medium | Introduce incentives for card payments such as cashback offers, discounts, or loyalty rewards. | Insight 4: Credit card payments are the preferred method | Finance & Customer Experience Team |
| Medium | Focus business expansion and promotional activities on top-performing shopping mall locations. | Location-based sales performance analysis | Business Development Team |
| Medium | Implement bundle deals and quantity discounts to encourage higher-volume purchases. | Bulk purchase behavior identified during sales analysis | Sales Strategy Team |
| Low| Conduct deeper customer segmentation analysis using additional demographic and behavioral data. | Customer behavior and segmentation findings | Data Analytics Team |
| Low | Expand future analysis using Power BI or SQL-based reporting for advanced insights and automation. | Overall project analysis workflow | Data & Business Intelligence Team |

---

## 10. Assumptions & Limitations

### Assumptions

-**Data Accuracy Assumption**
The analysis assumes that the transactional records provided in the dataset are accurate, complete, and correctly recorded at the point of collection. Invoice numbers were treated as unique transaction identifiers without independent verification.
The analysis assumes that the transactional records provided in the dataset are accurate, complete, and correctly recorded at the point of collection. Invoice numbers were treated as unique transaction identifiers without independent verification.

- **Consistent Business Definitions**
It was assumed that:

Product categories were correctly assigned

Payment methods were consistently recorded

Shopping mall names accurately represented transaction locations.

These business definitions were accepted as provided in the dataset.

- **Customer Identification Assumption**
Customer IDs were assumed to uniquely represent individual customers, even though additional customer profile information was not available for validation.

- **Time-Based Assumption**
The transaction dates in the dataset were assumed to reflect the actual purchase dates and were treated as reliable for trend analysis and time-based insights.

- **Scope Simplification**
To maintain project feasibility and align with the project scope:

External market factors were excluded

Economic conditions and competitor activity were not analyzed

Advanced predictive modeling and machine learning were not included

The project focused primarily on descriptive and exploratory analysis using Excel-based tools.

### Limitations

- **Limited Customer Demographics**

The dataset contains only basic demographic information (such as age and gender). Additional attributes like income level, customer loyalty status, geographic region, or occupation were unavailable, limiting deeper customer segmentation analysis.

-**Lack of External Context**
The analysis does not include external variables such as:

Seasonal events

Economic trends

Marketing campaign data

Competitor activity

These factors may influence customer purchasing behavior and sales performance.
  
- **Exploratory Rather Than Predictive Analysis**
The project focused on descriptive and exploratory analysis rather than predictive analytics. A more advanced version of the project could include:

Sales forecasting

Customer churn prediction

Market basket analysis

Recommendation systems

- **Tooling Constraints**
The analysis and dashboard were developed primarily in Microsoft Excel. While effective for exploratory analysis and reporting, Excel has limitations for:

Large-scale data processing

Automation

Real-time analytics

Advanced statistical modeling

- **Potential Data Collection Bias**
The dataset reflects only recorded transactions available in the source file. If certain transactions, customer groups, or shopping periods were underrepresented or excluded during data collection, the analysis results may not fully represent actual business performance.

- **Limited Validation of Source Data**
The project relied on the provided dataset without independent auditing or verification of source systems. Any inaccuracies in the original data source may affect the reliability of insights and conclusions.

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
