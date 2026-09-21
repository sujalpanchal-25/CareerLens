<div align="center">

# 🔮 CareerLens — AI & Tech Job Market Analytics

### *Transforming Global Tech Labor Data into Strategic Talent & Compensation Intelligence*

[![Power BI](https://img.shields.io/badge/Power_BI-Desktop_Report-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![DAX](https://img.shields.io/badge/DAX-Data_Analysis_Expressions-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)](https://learn.microsoft.com/en-us/dax/)
[![Data Model](https://img.shields.io/badge/Data_Model-Star_Schema-7928CA?style=for-the-badge&logo=databricks&logoColor=white)](#-data-model--entity-relationship-architecture)
[![Python](https://img.shields.io/badge/Python-Data_ETL_%26_Viz-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-22c55e?style=for-the-badge&logo=open-source-initiative&logoColor=white)](LICENSE)
[![Author](https://img.shields.io/badge/Created_By-Sujal_Panchal-9333ea?style=for-the-badge&logo=github&logoColor=white)](https://github.com/sujalpanchal-25)

<br/>

<img src="assets/banner.png" alt="CareerLens Job Analytics Banner" width="100%" style="border-radius: 12px; box-shadow: 0 8px 30px rgba(124, 58, 237, 0.35);"/>

<br/>

**[📁 Folder Structure](#-project-directory--folder-structure)** •
**[📸 Dashboard Gallery](#-dashboard--report-gallery)** •
**[🏗️ Data Modeling & Relations](#-data-model--entity-relationship-architecture)** •
**[🧠 Market Insights](#-executive-summary--market-findings)** •
**[📐 DAX Measures](#-dax-measures--analytical-formulas)** •
**[🚀 Setup Guide](#-quick-start--setup-guide)**

---

</div>

## 📌 Executive Summary

**CareerLens** is an end-to-end, multi-page business intelligence and data analytics suite developed in **Microsoft Power BI**. Designed for tech leaders, hiring managers, talent strategists, and candidates, it delivers actionable clarity on the rapidly evolving artificial intelligence, machine learning, and data science job markets.

Through an intuitive, cyber-purple glassmorphic interface, CareerLens deciphers hiring demand across top AI innovators (**OpenAI, Google DeepMind, HuggingFace, NVIDIA, DataCamp**), mapping global salary variance, remote flexibility adoption, experience-level requirements, and skill stack prerequisites.

---

## ⚡ High-Level Market KPIs

<div align="center">

| 💼 Analyzed Roles | 💰 Average Salary | 🎯 Median Salary | 🚀 Max Comp Peak | 🌐 Remote Ratio | 👑 Top Skill Moat |
| :---: | :---: | :---: | :---: | :---: | :---: |
| **10 Positions** | **$93,400 / yr** | **$102,500 / yr** | **$132,000 / yr** | **59% Remote** | **Python (90%)** |

</div>

---

## 📁 Project Directory & Folder Structure

The repository is modularly structured to maintain strict separation of concerns between raw transactional data sources, compiled visual presentation assets, and the central Power BI report model:

```plaintext
CareerLens/
│
├── 📂 Dataset/                                    # 📊 Raw Dimension & Fact CSV Sources
│   ├── 📄 Companies.csv                          # Metadata on hiring firms (size, industry, ratings)
│   ├── 📄 Jobs.csv                               # Transactional job openings, comp, dates & remote ratio
│   ├── 📄 Job_Skills.csv                         # Associative M:N bridge mapping Job IDs to Skill IDs
│   ├── 📄 Locations.csv                          # Geographic hierarchy (City, Country, Region)
│   └── 📄 Skills.csv                             # Master dictionary of recognized technical competencies
│
├── 📂 assets/                                     # 🎨 High-Resolution Visual Presentation Assets
│   ├── 🖼️ banner.png                             # Official CareerLens presentation & hero banner
│   ├── 🖼️ overview_dashboard.png                 # Page 1: Executive Overview Dashboard UI
│   ├── 🖼️ location_insights.png                  # Page 2: Global Compensation & Location Report UI
│   ├── 🖼️ company_role_insights.png              # Page 3: Employer Profiles & Role Insights UI
│   ├── 🖼️ skills_hiring_insights.png             # Page 4: Technical Skills & Demand Analytics UI
│   └── 🖼️ data_model_diagram.png                 # Power BI Model View: Entity Relationships & Star Schema
│
├── 📊 Job_Market_Dashboard.pbix                   # 🚀 Core Power BI Desktop File (Data Model, DAX & Visuals)
├── 📜 LICENSE                                     # Open-source MIT License
└── 📄 README.md                                   # Comprehensive Project Documentation & Visual Guide
```

### 🗃️ Component Breakdown

| Folder / File | Type | Purpose & Details |
| :--- | :--- | :--- |
| **`Dataset/`** | Data Layer | Stores normalized CSV files acting as the single source of truth (SSOT) ingested via Power Query. |
| **`assets/`** | Presentation | Contains high-definition screenshots, UI banners, and architectural diagrams rendered for GitHub showcase. |
| **`Job_Market_Dashboard.pbix`** | BI Application | The production Microsoft Power BI file comprising the data model, DAX engine, theme tokens, and interactive canvas. |
| **`README.md`** | Documentation | Production-ready documentation covering data architecture, metrics, findings, and usage instructions. |

---

## 📸 Dashboard & Report Gallery

The Power BI report contains **4 distinct analytical pages** equipped with dynamic cross-filtering, bookmark navigation, slicers, and interactive drill-downs.

---

### 1️⃣ Page 1: Executive Overview Dashboard
> *A bird's-eye view of macro employment metrics, experience segmentation, hiring timelines, and regional compensation variance.*

<div align="center">
  <img src="assets/overview_dashboard.png" alt="CareerLens Executive Overview Dashboard" width="100%" style="border-radius: 10px; border: 1px solid #3d286e;"/>
</div>

#### 🔍 Key Visual Elements:
- **KPI Stat Cards**: Instant readouts for *Total Jobs (10)*, *Average Salary ($93.4K)*, *Average Salary by Experience ($103.8K)*, *Median Salary ($102.5K)*, and *Remote Job % (59%)*.
- **Monthly Job Openings Trend (Line Chart)**: Tracks volume fluctuations across hiring cycles from May through September 2024.
- **Jobs by Experience Level & Work Mode (Clustered Column)**: Highlights remote vs. hybrid/on-site distributions for Entry, Mid, and Senior positions.
- **Job Distribution by Experience (Donut Chart)**: Visualizes the seniority split (**Mid-Level 40%**, **Senior 30%**, **Entry-Level 30%**).
- **Job Count by City & Salary (Waterfall Chart)**: Illustrates how salary benchmarks build up across global hubs from Bengaluru to San Francisco.
- **Sidebar Slicers**: Instant filtering by *City* and *Month* with smooth bookmark navigation.

---

### 2️⃣ Page 2: Location & Geographic Compensation Insights
> *Geospatial intelligence analyzing geographical pay disparities, regional headcount density, and cross-border salary efficiency.*

<div align="center">
  <img src="assets/location_insights.png" alt="CareerLens Location Insights Report" width="100%" style="border-radius: 10px; border: 1px solid #3d286e;"/>
</div>

#### 🔍 Key Visual Elements:
- **Global Choropleth & Bubble Map Visual**: Displays average salary levels across key tech territories (**North America, Europe, Asia**) with bubble radii scaled by compensation magnitude.
- **Country Salary Performance (KPI Gauge)**: Evaluates compensation performance against targeted industry baselines.
- **Job Distribution by Country & City (Treemap)**: Hierarchical decomposition showcasing talent concentration in San Francisco (USA), London (UK), Bengaluru (India), Toronto (Canada), and Berlin (Germany).
- **Country, City & TotalJobs Matrix**: Deep multi-level pivot grid detailing total roles, seniority breakdowns, and average compensation by geography.
- **Sidebar Slicers**: Multi-select filtering for *Region*, *Country*, and *Reporting Period*.

---

### 3️⃣ Page 3: Company & Role Insights
> *Competitive employer intelligence dissecting hiring profiles, company ratings, remote openness, and role-specific compensation.*

<div align="center">
  <img src="assets/company_role_insights.png" alt="CareerLens Company and Role Insights Report" width="100%" style="border-radius: 10px; border: 1px solid #3d286e;"/>
</div>

#### 🔍 Key Visual Elements:
- **Jobs by Company & Experience Level (100% Stacked Column)**: Analyzes talent seniority distribution across industry leaders:
  - **Google DeepMind**: Heavy focus on Senior ML Engineers and Senior Computer Vision Specialists.
  - **OpenAI**: Balanced hiring across Mid Data Scientists and AI Product Managers.
  - **NVIDIA**: High-leverage Senior Deep Learning Specialists and Mid NLP Engineers.
  - **HuggingFace**: Ground-floor investment in Entry AI Researchers and ML Interns.
  - **DataCamp**: Core data infrastructure across Data Engineers and Data Analysts.
- **Jobs by Role & Experience Level (Clustered Column Chart)**: Headcount breakdown grouped by job family and career stage.
- **Company Rating Change (Waterfall Chart)**: Correlates Glassdoor/internal satisfaction ratings (ranging from 4.5 to 4.9) across enterprises.
- **Salary vs. Remote Work by Job Role (Scatter Plot)**: Multi-dimensional bubble matrix plotting *Remote Ratio (%)* vs. *Salary (USD)* with bubble size indicating required *Skill Usage Count*.

---

### 4️⃣ Page 4: Skill Demands & Hiring Dynamics
> *Technical competency analysis identifying essential programming languages, ML specializations, and skill-to-compensation correlations.*

<div align="center">
  <img src="assets/skills_hiring_insights.png" alt="CareerLens Skill and Hiring Insights Report" width="100%" style="border-radius: 10px; border: 1px solid #3d286e;"/>
</div>

#### 🔍 Key Visual Elements:
- **Top Competency Cards**: Highlights *Total Jobs (10)*, *Avg Skills Required per Role (3.0)*, *Top Moat Skill (Python @ 90%)*, and *Highest-Paid Skill Specialization (Deep Learning @ $132,000)*.
- **Salary & Seniority Curve by Role (Spline & Area Chart)**: Visual progression of earnings starting from ML Intern ($30K) up to Deep Learning Specialist ($132K).
- **Top Skills Frequency (Horizontal Bar Chart)**: Clear ranking of market requirements: **Python (9)**, **Machine Learning (5)**, **Cloud Computing (3)**, **Data Visualization (3)**, and **Deep Learning / NLP / CV / SQL (2 each)**.
- **Skill Distribution by Experience Level (100% Stacked Bar)**: Pinpoints when skills become mandatory (e.g., Cloud & Deep Learning surge in Senior roles, while SQL and Python dominate Entry/Mid).
- **Skill Usage Share (Modern Donut Chart)**: Percentage representation of overall skill mentions across active job postings.

---

## 🏗️ Data Model & Entity Relationship Architecture

CareerLens is architected on an enterprise-grade **Star Schema** dimensional model. In transactional enterprise systems, relationships between jobs and required technical skills represent a classic **Many-to-Many ($M:N$)** scenario. To ensure high VertiPaq engine compression, prevent ambiguous filter propagation, and maximize DAX performance, CareerLens uses an **associative bridge table (`Fact_Job_Skills`)**.

### 🌟 Power BI Model View Diagram
> *Exact entity-relationship diagram and table layout inside Microsoft Power BI Desktop's Model View:*

<div align="center">
  <img src="assets/data_model_diagram.png" alt="CareerLens Data Model & Entity Relationship Diagram" width="100%" style="border-radius: 12px; border: 1.5px solid #4c1d95; box-shadow: 0 10px 30px rgba(76, 29, 149, 0.4);"/>
</div>

---

### 📐 Entity-Relationship (ER) Schema Specification

```mermaid
erDiagram
    DIM_COMPANIES ||--o{ FACT_JOBS : "1 : N (Filters Fact)"
    DIM_LOCATIONS ||--o{ FACT_JOBS : "1 : N (Filters Fact)"
    DIM_DATE ||--o{ FACT_JOBS : "1 : N (Temporal Filter)"
    FACT_JOBS ||--o{ FACT_JOB_SKILLS : "1 : N (Job Details)"
    DIM_SKILLS ||--o{ FACT_JOB_SKILLS : "1 : N (Skill Catalog)"

    DIM_COMPANIES {
        string Company_ID PK "Unique Company Identifier"
        string Company_Name "Enterprise Name"
        string Company_Size "Small, Medium, Large"
        string Industry "AI Research, EdTech, Hardware"
        float Rating "Company Glassdoor / Review Rating"
    }

    DIM_LOCATIONS {
        string Location_ID PK "Unique Location Identifier"
        string City "City Location"
        string Country "Country"
        string Region "Continent / Territory"
    }

    DIM_DATE {
        date Date PK "Calendar Date Key"
        int Year "Posting Year"
        string MonthName "Month Name (e.g. August)"
        string YearMonth "Formatted Year-Month Period"
        string Quarter "Fiscal Quarter"
    }

    FACT_JOBS {
        string Job_ID PK "Unique Job Opening Identifier"
        string Company_ID FK "References Dim_Companies"
        string Location_ID FK "References Dim_Locations"
        date Posted_Date FK "References Dim_Date"
        string Job_Title "Role Title"
        string Experience_Level "Entry, Mid, Senior"
        string Employment_Type "Full-time, Contract, Internship"
        int Remote_Ratio "Workplace Flexibility (0-100%)"
        decimal Salary_USD "Annual Base Compensation ($USD)"
    }

    FACT_JOB_SKILLS {
        string Job_ID FK "References Fact_Jobs (Compound Key)"
        string Skill_ID FK "References Dim_Skills (Compound Key)"
    }

    DIM_SKILLS {
        string Skill_ID PK "Unique Skill Identifier"
        string Skill_Name "Technical Proficiency / Tool"
    }
```

---

### 🔗 Relationship Cardinality & Filter Flow Matrix

| From Table (Parent / Dim) | To Table (Child / Fact) | Primary Key (PK) | Foreign Key (FK) | Cardinality | Cross-Filter Direction | Architectural Role |
| :--- | :--- | :--- | :--- | :---: | :---: | :--- |
| **`Dim_Companies`** | **`Fact_Jobs`** | `Company_ID` | `Company_ID` | **`1 : N`** (One-to-Many) | Single (`Dim ➔ Fact`) | Filters employment facts by company metadata, industry & rating. |
| **`Dim_Locations`** | **`Fact_Jobs`** | `Location_ID` | `Location_ID` | **`1 : N`** (One-to-Many) | Single (`Dim ➔ Fact`) | Propagates geographic filters across cities, countries & continental regions. |
| **`Dim_Date`** | **`Fact_Jobs`** | `Date` | `Posted_Date` | **`1 : N`** (One-to-Many) | Single (`Dim ➔ Fact`) | Enables time-intelligence calculations, quarterly trends & month slicers. |
| **`Fact_Jobs`** | **`Fact_Job_Skills`**| `Job_ID` | `Job_ID` | **`1 : N`** (One-to-Many) | Single (`Fact ➔ Bridge`)| Decomposes job postings into individual skill requirements. |
| **`Dim_Skills`** | **`Fact_Job_Skills`**| `Skill_ID` | `Skill_ID` | **`1 : N`** (One-to-Many) | Single (`Dim ➔ Bridge`)| Filters skill demand facts by standardized skill naming conventions. |

> [!NOTE]
> **Why an Associative Bridge Table?**
> A single job requires multiple skills, and a single skill is required by many jobs ($M:N$). Rather than utilizing a messy bi-directional relationship or un-normalized delimited strings, `Fact_Job_Skills` bridges the two dimensions into clean `1:N` relationships, maintaining optimal DAX query speeds and preventing circular dependency deadlocks.

---

### 📋 Data Dictionary

| Table Name | Entity Type | Primary / Foreign Key | Description |
| :--- | :--- | :--- | :--- |
| **`Fact_Jobs`** | Fact Table | `Job_ID` (PK), `Company_ID` (FK), `Location_ID` (FK), `Posted_Date` (FK) | Core transactional fact table containing salary, experience level, remote ratio, and post dates. |
| **`Dim_Companies`** | Dimension Table | `Company_ID` (PK) | Corporate dimension table including firm name, industry segment, enterprise size, and employee rating. |
| **`Dim_Locations`** | Dimension Table | `Location_ID` (PK) | Geographic dimension table encompassing City, Country, and continental Region hierarchies. |
| **`Dim_Skills`** | Dimension Table | `Skill_ID` (PK) | Catalog dimension of recognized technical proficiencies (Python, TensorFlow, PyTorch, SQL, Cloud, etc.). |
| **`Fact_Job_Skills`** | Bridge / Fact | `Job_ID` (FK), `Skill_ID` (FK) | Resolves the many-to-many relationship between Job openings and required Skill tags. |
| **`Dim_Date`** | Dimension Table | `Date` (PK) | Temporal dimension facilitating time-intelligence analysis across months, quarters, and years. |

---

## 📐 DAX Measures & Analytical Formulas

The dashboard leverages custom **DAX (Data Analysis Expressions)** to calculate dynamic aggregations, ratios, and cross-table benchmarks:

### 1. Headcount & Ratio Metrics
```dax
TotalJobs = 
COUNTROWS(Fact_Jobs)
```

```dax
Remote_Job_% = 
AVERAGE(Fact_Jobs[Remote_Ratio])
```

```dax
AvgSkillPerJob = 
DIVIDE(
    COUNTROWS(Fact_Job_Skills),
    DISTINCTCOUNT(Fact_Job_Skills[Job_ID]),
    0
)
```

### 2. Compensation Aggregations
```dax
AvgSalary = 
AVERAGE(Fact_Jobs[Salary_USD])
```

```dax
MedianSalary = 
MEDIAN(Fact_Jobs[Salary_USD])
```

```dax
AvgSalaryByCountry = 
CALCULATE(
    AVERAGE(Fact_Jobs[Salary_USD]),
    ALLEXCEPT(Dim_Locations, Dim_Locations[Country])
)
```

```dax
AvgSalaryByExperience = 
CALCULATE(
    AVERAGE(Fact_Jobs[Salary_USD]),
    ALLEXCEPT(Fact_Jobs, Fact_Jobs[Experience_Level])
)
```

### 3. Employer & Skill Intelligence
```dax
CompanyAvgRating = 
AVERAGE(Dim_Companies[Rating])
```

```dax
SkillUsageCount = 
CALCULATE(
    COUNTROWS(Fact_Job_Skills)
)
```

---

## 💡 Executive Summary & Market Findings

<details open>
<summary><b>1. Deep Learning & Computer Vision Command Top Compensation</b></summary>
<br/>
Senior specialized roles lead the market compensation spectrum:
- **Deep Learning Specialist (NVIDIA)**: <code>$132,000</code>
- **ML Engineer (Google DeepMind)**: <code>$125,000</code>
- **Computer Vision Engineer (Google DeepMind)**: <code>$118,000</code>
- General data roles (Data Analyst at DataCamp) sit at <code>$45,000</code>, reflecting a <b>~3x salary multiplier</b> for deep AI specialization.
</details>

<details open>
<summary><b>2. Python is the Undisputed Core Industry Requirement</b></summary>
<br/>
Out of all 10 surveyed tech roles across all companies, <b>9 explicitly mandate Python (90% market penetration)</b>. Machine Learning (50%) is the secondary pillar, with specialized libraries (PyTorch, TensorFlow, Computer Vision) acting as key differentiators for senior compensation.
</details>

<details open>
<summary><b>3. Remote Work Has Stabilized into a Dominant Hybrid Reality</b></summary>
<br/>
The aggregate remote work ratio sits at <b>59%</b>:
- <b>Fully Remote (100%)</b>: Data Scientist (OpenAI)
- <b>High Remote (70% - 90%)</b>: Machine Learning Intern (HuggingFace, 90%), NLP Engineer (NVIDIA, 80%), AI Product Manager (OpenAI, 70%)
- <b>On-Site (0%)</b>: AI Researcher (HuggingFace, Bengaluru)
- Companies leverage high remote allowances to recruit top global talent without geographic constraints.
</details>

<details open>
<summary><b>4. Geographic Pay Arbitrage Remains Significant</b></summary>
<br/>
- **San Francisco, USA**: Average salary of <code>$113,333</code> across AI engineering and product roles.
- **Toronto, Canada**: Robust compensation at <code>$118,000</code> for specialized computer vision engineering.
- **Berlin, Germany & London, UK**: European tech hubs offer competitive salaries ranging from <code>$89,000</code> to <code>$107,000</code>.
- **Bengaluru, India**: Emerging AI talent hub averaging <code>$51,000</code>, offering significant cost-efficiency for early-stage AI research.
</details>

---

## 🚀 Quick Start & Setup Guide

### Prerequisites
- [Microsoft Power BI Desktop](https://powerbi.microsoft.com/desktop/) (August 2024 release or later recommended)
- Git installed on your local machine

### 1. Clone the Repository
```bash
git clone https://github.com/sujalpanchal-25/CareerLens.git
cd CareerLens
```

### 2. Open the Report in Power BI Desktop
1. Double-click on `Job_Market_Dashboard.pbix` or open Power BI Desktop and select **File > Open Report**.
2. If prompted for data sources, verify that the CSV file paths in the `Dataset/` folder match your local directory:
   - Go to **Transform Data > Data Source Settings**.
   - Select each file path and update the source path if your directory moved.
   - Click **Close & Apply**.

### 3. Explore & Interact
- Use the **left navigation bar** to switch between **Overview**, **Location Insights**, **Company & Roles**, and **Skill & Hiring Insights**.
- Click on any visual element (e.g., a bar, donut slice, or treemap tile) to trigger **interactive cross-filtering**.
- Use the **slicers** in the sidebar to filter data by City, Month, Experience Level, or Technical Skill.

---

## 🛠️ Technology Stack & Tools

<div align="center">

| Technology | Purpose | Usage in Project |
| :--- | :--- | :--- |
| **Microsoft Power BI** | Business Intelligence & Data Viz | Multi-page report design, interactive visuals, bookmark navigation |
| **DAX (Data Analysis Expressions)** | Data Modeling & Calculations | Dynamic KPI measures, median salary, conditional ratios |
| **Power Query (M Language)** | Data Extraction, Transform & Load | Data ingestion, type casting, schema structuring |
| **Python (Matplotlib, PIL, Pandas)** | Exploratory Analysis & Asset Gen | Statistical validation, metrics calculation, visual render generation |
| **Git & GitHub** | Version Control & Showcase | Source control, issue tracking, and interactive documentation |

</div>

---

## 🔮 Roadmap & Future Enhancements

- [ ] **Automated Web Scraping Pipeline**: Integrate an automated Python scraper (LinkedIn / Indeed / Glassdoor) to update `Dataset/` weekly.
- [ ] **Machine Learning Salary Predictor**: Embed an Azure ML / Python regression script to predict compensation based on skills, seniority, and location.
- [ ] **Power BI Service Deployment**: Publish report to Power BI Web Service with scheduled cloud refresh and role-based row-level security (RLS).
- [ ] **Cost of Living Index Adjustment**: Incorporate Numbeo Purchasing Power Parity (PPP) indices to compute real adjusted earnings.

---

## 👨‍💻 Author & Connect

**Sujal Panchal**  
*Data Analyst & Business Intelligence Specialist*

[![GitHub](https://img.shields.io/badge/GitHub-sujalpanchal--25-181717?style=flat-square&logo=github)](https://github.com/sujalpanchal-25)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat-square&logo=linkedin)](https://linkedin.com)
[![Email](https://img.shields.io/badge/Email-sujalpanchal257@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:sujalpanchal257@gmail.com)

---

<div align="center">

### ⭐ If you find this project insightful or helpful, please consider giving it a Star! ⭐

*Built with passion for data-driven decision making.*

</div>
