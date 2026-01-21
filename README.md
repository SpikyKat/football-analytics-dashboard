# ⚽ European Football Analytics Dashboard (Power BI + Python)

## 📌 Project Overview
This project is an end-to-end football analytics solution built using **Python and Power BI**, analyzing match-level data across **five major European football leagues** from **1993 to the present**.  
The dashboard enables historical and comparative analysis of team performance, league competitiveness, goal trends, and home vs away dynamics.

The project focuses on **data processing, modeling, and visualization best practices**, following a scalable analytics architecture suitable for real-world BI use cases.

---

## 🏆 Leagues Covered
- English Premier League  
- Spanish La Liga  
- Italian Serie A  
- German Bundesliga  
- French Ligue 1  

---

## 🗂️ Data Source
- Open football datasets sourced from **football-data.co.uk**
- Curated and maintained via the **datasets/football-datasets** GitHub repository
- Historical coverage from **1993 onwards**
- Data updated regularly via GitHub Actions

---

## 🧱 Project Architecture
Open Football Datasets (GitHub)

              ↓

Python Data Processing & Cleaning

              ↓

Fact & Dimension Tables

              ↓

Power BI Data Model (Star Schema)

              ↓

Interactive Dashboards & Insights


---

## 🛠️ Tools & Technologies
- **Python** (pandas, numpy)
- **Power BI**
- **GitHub**
- Open-source football datasets

---

## 📊 Data Modeling
The project uses a **star schema** design for efficient analysis and performance:

### Fact Table
- Match results (goals, outcomes, home/away teams, season, league)

### Dimension Tables
- Teams  
- Leagues  
- Seasons  
- Date  

This approach improves scalability, readability, and dashboard performance.

---

## 📈 Dashboard Features
- League-level performance analysis  
- Team performance trends across seasons  
- Home vs away goal and win comparison  
- Historical goal and match trends (1993–present)  
- Interactive filters by league, team, and season  

---

## 🔄 Data Refresh Workflow
- Python scripts are used to process and standardize the datasets
- Updated datasets can be regenerated and reloaded into Power BI
- Supports repeatable and reliable refresh cycles

---

## ⚖️ Data License
This project uses data released under the  
**Public Domain Dedication and License (PDDL 1.0)**  
(http://www.opendatacommons.org/licenses/pddl/1.0/)

---

## 📸 Dashboard Preview

<img width="1959" height="1099" alt="image" src="https://github.com/user-attachments/assets/7b80c1e9-4772-4ba6-9e86-ec99832be376" />


<img width="1959" height="1096" alt="image" src="https://github.com/user-attachments/assets/f53481fe-2682-48f4-8c71-c523973cfe2a" />


<img width="1955" height="1099" alt="image" src="https://github.com/user-attachments/assets/abdd18a5-5181-49bc-9efc-0518fb0609bc" />


---

## 🚀 Future Enhancements
- Advanced DAX measures (points tables, rankings, form analysis)
- Automated refresh scheduling
- Additional leagues or competitions
- Enhanced historical trend analysis

---

## 👤 Author
**Rahul Ghantasala**  
Data & Analytics | Power BI | Python  


