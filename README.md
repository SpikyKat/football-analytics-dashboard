# ⚽ European Football Analytics Dashboard (1993–2025)

An end-to-end **ETL and analytics project** that extracts historical European football match data, transforms it into an analytics-ready star schema using Python, and visualizes insights using **Power BI**.

This project demonstrates **real-world data engineering concepts**, analytical modeling, and dashboard storytelling.

---

## 📌 Project Objective

The goal of this project is to:

- Build a reproducible **ETL pipeline** for football match data
- Analyze **30+ years** of football history (1993–2025)
- Design a clean **fact–dimension data model**
- Deliver interactive dashboards for league, team, and historical analysis

---

## 🧱 ETL Architecture Overview

**Web Source (HTML pages)**  
⬇️  
**EXTRACT (BeautifulSoup)**  
⬇️  
**TRANSFORM (Python / Pandas)**  
⬇️  
**LOAD (Power BI)**  
⬇️  
**Analytics & Visualization**

---


## 🔍 EXTRACT (Data Collection)

### Data Source
- Public football statistics sources (e.g. football-data.co.uk)
- Season-wise match result tables

### Extraction Approach
- Web scraping using **BeautifulSoup**
- Each league and season extracted independently
- Raw match data persisted as structured CSV files

### Why BeautifulSoup?
- Lightweight and reliable for static HTML
- Fine-grained control over table parsing
- Suitable for repeatable ETL pipelines

### Output
- One CSV per league per season
- Consistent schema across seasons

---

## 🔄 TRANSFORM (Data Processing & Modeling)

Transformation is handled entirely in **Python (Pandas)**.

### Key Transformation Steps

#### 1. Data Standardization
- Unified column names across all seasons
- Standardized date formats
- Ensured consistent data types

#### 2. Data Enrichment
- Added metadata columns:
- `League`
- `Season`
- Converted date fields to datetime
- Derived analytical attributes (Year, Month, Era)

#### 3. Fact Table Creation
All season-level files are merged into a single **fact table**:

**FactResults**
- Grain: one row per match
- Covers all leagues and seasons

Key columns:
- Date
- League
- Season
- HomeTeam
- AwayTeam
- Goals (home & away)
- Match result

#### 4. Dimension Tables
Dimensions are derived directly from the fact table (best practice):

- **DimDate** – calendar attributes
- **DimTeams** – team & league mapping

This ensures consistency and avoids duplication.

---

## ⭐ Data Model (Star Schema)

### Fact Table
**FactResults**
- Date
- League
- Season
- HomeTeam
- AwayTeam
- FTHG
- FTAG
- FTR
- HTHG
- HTAG
- HTR

### Dimension Tables
**DimDate**
- Date
- Year
- Month
- Quarter
- Week
- DayName
- Era

**DimTeams**
- Team
- League

This model is optimized for:
- Query performance
- DAX simplicity
- Analytical flexibility

---

## 📥 LOAD (Power BI)

### Loading Strategy
- Clean CSVs generated via Python
- Loaded into **Power BI Desktop**
- Relationships defined in Model View

### Relationship Design
- FactResults → DimDate (Active)
- FactResults → DimTeams (Inactive for Home/Away)
- `USERELATIONSHIP` used in DAX for team-level metrics

---

## 📊 Dashboards & Analytics

### Page 1 – League Overview
- Matches Played
- Total Goals
- Average Goals per Match
- League-level comparisons

<img width="1959" height="1099" alt="image" src="https://github.com/user-attachments/assets/e13767de-2413-4bc6-b5b3-db7823ad6939" />


### Page 2 – Team Performance
- Points calculation
- Goal difference
- Team rankings
- League & season filtering

<img width="1959" height="1096" alt="image" src="https://github.com/user-attachments/assets/fb5d8d1a-7a2f-4c97-967c-e2b1f8d0d48a" />


### Page 3 – Historical Trends
- Goal trends from 1993–2025
- League evolution analysis
- All-time team dominance
- Era-based scoring insights

<img width="1955" height="1099" alt="image" src="https://github.com/user-attachments/assets/ce10b17c-68c7-4bd2-8803-afeae26f8661" />


---

## 🧠 Key Insights

- Football has become more attacking over time
- Scoring trends differ significantly by league
- Historical dominance patterns persist across decades
- Modern football shows higher scoring intensity

---

## 🛠️ Tech Stack

- **Python**
- Pandas
- BeautifulSoup
- Requests
- **Power BI**
- DAX
- Star schema modeling
- **Git & GitHub**
- Version control
- Documentation

