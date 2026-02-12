# 🍴 Zomato Global Restaurant Intelligence

![Power BI](https://img.shields.io/badge/Data_Viz-Power_BI-yellow) 
![SQL](https://img.shields.io/badge/Database-MySQL-blue) 
![Excel](https://img.shields.io/badge/Analysis-Excel-green) 
![Status](https://img.shields.io/badge/Status-Complete-success)

A comprehensive data analysis project on Zomato restaurant data across 15 countries. This project demonstrates end-to-end data analytics from SQL database creation to interactive dashboards and presentations.

## 📊 Project Overview

This project analyzes restaurant data from Zomato across multiple countries including India, Australia, Brazil, Canada, Indonesia, New Zealand, Philippines, Qatar, Singapore, South Africa, Sri Lanka, Turkey, UAE, United Kingdom, and United States.

### Key Objectives

1. **Data Structuring** - Create normalized database tables (Country Map, Calendar)
2. **Exploratory Analysis** - Analyze restaurant distribution, ratings, and opening trends
3. **Business Insights** - Understand pricing patterns, delivery capabilities, and table booking features
4. **Visualization** - Create interactive dashboards and presentations for stakeholders

## 📁 Project Structure

```
zomato-analysis/
├── README.md                          # Project documentation
├── .gitignore                         # Git ignore file
├── requirements.txt                   # Python dependencies (if applicable)
│
├── data/                              # Data files
│   ├── raw/
│   │   ├── zomato_original_data.xlsx        # Main Zomato dataset
│   │   ├── country_codes.xlsx               # Country reference table
│   │   └── currency_codes.xlsx              # Currency reference data
│
├── sql/                               # SQL scripts
│   └── zomato_analysis.sql            # All SQL queries and table creation
│
├── analysis/
│   ├── excel/
│   │   └── zomato_analysis.xlsx       # Excel analysis workbook
│   ├── power-bi/
│   │   └── zomato_analysis.pbix       # Power BI dashboard
│   └── tableau/
│       └── zomato_analysis.twbx       # Tableau workbook
│
├── presentation/
│   └── zomato_analysis.pptx           # Final presentation
│
└── docs/
    └── project_guidelines.docx        # Project requirements & guidelines
```

## 🗂️ File Descriptions

### Data Files (`data/raw/`)
- **zomato_original_data.xlsx** - Main dataset containing restaurant information (RestaurantID, Name, City, Country, Ratings, Average Cost, etc.)
- **country_codes.xlsx** - Reference table mapping country codes to country names
- **currency_codes.xlsx** - Currency conversion reference data

### SQL Scripts (`sql/`)
- **zomato_analysis.sql** - Complete SQL implementation including:
  - `ZOMATO_ANALYSIS` database creation
  - `country_map` table (15 countries)
  - `calendar` table with derived columns
  - 8+ analytical queries

### Analysis Files (`analysis/`)

#### Excel (`excel/`)
- **zomato_analysis.xlsx** - Pivot tables, formulas, and basic analysis charts

#### Power BI (`power-bi/`)
- **zomato_analysis.pbix** - Interactive Power BI dashboard with:
  - Restaurant distribution by country/city
  - Opening trends analysis
  - Ratings distribution
  - Price bucket analysis
  - Feature adoption metrics

#### Tableau (`tableau/`)
- **zomato_analysis.twbx** - Interactive Tableau workbook with:
  - Geospatial visualizations
  - Time-series analysis
  - Rating and price analysis
  - Cuisine-based insights

### Presentation (`presentation/`)
- **zomato_analysis.pptx** - Executive presentation including:
  - Project overview
  - Key findings
  - Visual dashboards
  - Recommendations

### Documentation (`docs/`)
- **project_guidelines.docx** - Original project requirements and KPI specifications

## 📊 Key Analyses & KPIs

### 1. Geographic Analysis
- Number of restaurants by city and country
- Country-wise market penetration
- Urban vs emerging markets analysis

### 2. Temporal Analysis
- Restaurant openings by year, quarter, and month
- Seasonal trends
- Growth trajectory analysis

### 3. Quality Metrics
- Distribution of ratings (1.0 - 5.0 scale)
- Rating vs. pricing correlation
- High-rated restaurant concentrations

### 4. Pricing Analysis
- Price bucket distribution:
  - **Low** (<500)
  - **Medium** (500-1000)
  - **High** (1000-2000)
  - **Premium** (>2000)

### 5. Feature Adoption
- Table booking availability (Yes/No percentage)
- Online delivery availability (Yes/No percentage)
- Feature adoption by geography and price segment

### 6. Cuisine Analysis
- Popular cuisines by country
- Cuisine diversity metrics
- Cuisine-rating correlations

## 🛠️ Technologies Used

- **Database:** MySQL
- **Data Analysis:** Excel, SQL
- **Visualization:** Power BI, Tableau
- **Documentation:** PowerPoint

## 📋 Database Schema

### country_map Table
```sql
CountryCode (INT, PRIMARY KEY)
CountryName (VARCHAR(50))
```

### calendar Table
```sql
FullDate
Year
MonthNo
MonthFullName
Quarter (Q1, Q2, Q3, Q4)
YearMonth (YYYY-MMM format)
WeekdayNo
WeekdayName
FinancialMonth (FM1-FM12, April = FM1)
FinancialQuarter (FQ1-FQ4)
```

### zomato1 Table (Original)
- RestaurantID
- RestaurantName
- City
- Country
- Cuisines
- Average_Cost_for_two
- Currency
- Has_Table_booking
- Has_Online_delivery
- Date
- Rating
- [Additional columns]

## 🚀 How to Use

### Option 1: Using SQL
1. Create database and tables using `sql/zomato_analysis.sql`
2. Load data from `data/raw/zomato_original_data.xlsx`
3. Run analytical queries to generate insights

### Option 2: Using Excel
1. Open `analysis/excel/zomato_analysis.xlsx`
2. Review pre-built pivot tables and charts
3. Modify as needed for specific analysis

### Option 3: Using Power BI
1. Open `analysis/power-bi/zomato_analysis.pbix`
2. Connect to your data source or use embedded data
3. Interact with dashboards and create new visualizations

### Option 4: Using Tableau
1. Open `analysis/tableau/zomato_analysis.twbx`
2. Explore pre-built dashboards
3. Create custom views and filters

### Option 5: View Presentation
1. Open `presentation/zomato_analysis.pptx`
2. Review executive summary and key findings
3. Use for stakeholder presentations

## 📈 Key Findings (Expected Insights)

- India and USA represent the largest markets
- Restaurant openings peaked in specific years/quarters
- Premium restaurants concentrated in major cities
- Table booking more common in developed countries
- Online delivery adoption varies by geography
- Strong correlation between price and ratings in certain markets

## 📝 Project Requirements

Original requirements specified in `docs/project_guidelines.docx`:
1. Build country map table ✅
2. Build calendar table with derived columns ✅
3. Find restaurants by city and country ✅
4. Analyze restaurant openings by time periods ✅
5. Count restaurants by rating ✅
6. Create price bucket analysis ✅
7. Analyze table booking percentage ✅
8. Analyze online delivery percentage ✅
9. Develop visualizations by cuisines, city, ratings ✅

## 🔄 Workflow

```
Raw Data (Excel) → SQL Database → Analysis (SQL Queries) 
  ↓
Excel Pivot Tables → Power BI Dashboard → Tableau Dashboard
  ↓
PowerPoint Presentation → Stakeholder Review
```

## 📊 Data Completeness

- **Countries Covered:** 15
- **Data Points:** Multiple restaurant attributes
- **Time Period:** Varies by restaurant opening date
- **Quality:** Cleaned and validated for analysis

## 🤝 Contributing

To extend this analysis:
1. Add new SQL queries for additional insights
2. Create new Power BI/Tableau visualizations
3. Update presentation with new findings
4. Add predictive analysis (ML models for rating prediction, growth forecasting, etc.)

## 📧 Contact & Support

For questions or improvements, please refer to `docs/project_guidelines.docx` for project specifications.

## 📜 License

This project is for educational and analytical purposes.

---

**Project Status:** ✅ Complete - Database, Analysis, Visualizations, and Presentation Ready

**Time Period:** Sept-Nov 2025

**Last Updated:** February 2026

**Deliverables Summary:**
- ✅ SQL Database & Queries
- ✅ Excel Analysis Workbook
- ✅ Power BI Dashboard
- ✅ Tableau Dashboard
- ✅ Executive Presentation
- ✅ Project Documentation
