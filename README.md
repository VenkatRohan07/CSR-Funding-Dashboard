# CSR Funding Companies Across India – Power BI Dashboard

An interactive Power BI dashboard built during my **Data Analyst Internship at StepUp for SDG (Pavdhan Technologies)**. It shows where CSR-funding companies are located across India, how large they are, and which UN Sustainable Development Goals (SDGs) they support.

![CSR Funding Companies Across India dashboard](images/dashboard.png)

---

## Table of Contents

- [Overview](#overview)
- [Internship Details](#internship-details)
- [Problem Statement](#problem-statement)
- [Dashboard Features](#dashboard-features)
- [Key Insights](#key-insights)
- [Data Model](#data-model)
- [Tools and Technologies](#tools-and-technologies)
- [Repository Structure](#repository-structure)
- [How to Run](#how-to-run)
- [Key Learnings](#key-learnings)
- [Author](#author)

---

## Overview

Information about companies that fund Corporate Social Responsibility (CSR) activities usually sits in large spreadsheets, which makes patterns hard to see. This project turns such a dataset into a single-page, interactive dashboard so that a user can understand CSR activity across India at a glance and filter it by state, SDG goal and company size.

## Internship Details

| | |
|---|---|
| **Organization** | Pavdhan Technologies (StepUp for SDG), Visakhapatnam, Andhra Pradesh |
| **Role** | Data Analyst Intern |
| **Duration** | 1 June 2026 – 31 July 2026 |
| **Mode** | Remote, about 24 hours per week |
| **Mentor** | Pavan Tarak Siddanathi |

Responsibilities during the internship included data collection, cleaning and analysis, building reports and dashboards, supporting business intelligence projects, documentation, and completing assigned learning modules.

## Problem Statement

Build an interactive dashboard that answers questions such as:

- How many CSR-funding companies are there, and in how many states?
- Which states have the most companies?
- Which SDG goals receive the most company support?
- What is the distribution of companies by size?

## Dashboard Features

- **KPI cards:** Total Companies, Total States, Total Websites and Total SDGs covered.
- **Shape map of India:** shades each state by its number of CSR-funding companies (uses a custom India map).
- **State bar chart:** company count by state for easy comparison.
- **SDG bar chart:** company count by SDG goal.
- **Company size donut chart:** distribution of companies by size.
- **Cross-filtering:** selecting a state, SDG goal or company size updates the other visuals.
- **Data quality:** blank (null) values are excluded from the SDG and company-size visuals using locked filters.
- **Custom design:** background, icons and a consistent colour theme on a 1280 x 720 canvas.

## Key Insights

Figures below are as shown on the dashboard.

- The dataset covers **7 states** and about **4K companies**, with about **4K company websites**.
- **Karnataka** has the most CSR-funding companies (about 1.6K), followed by Uttarakhand (0.7K), Himachal Pradesh (0.6K) and Punjab (0.5K). Bihar, Kerala and Assam follow with 0.3K–0.4K each.
- **SDG 3** (Good Health and Well-being) is the most-supported goal with 571 companies, followed by **SDG 9** (490), SDG 12 (196), SDG 7 (191) and SDG 8 (165).
- The largest company-size group is **100–500** (512 companies, 16.4%).

## Data Model

The report uses a single table (`Sheet1`) with these fields:

| Field | Description |
|---|---|
| State | State where the company is located |
| Company Size | Size category of the company |
| Certain SDG Goal | SDG goal the company supports |
| Websites | Company website |
| Company Count | Number of companies (used for all counts) |

> **Data quality note:** the source values for SDG goals and company size contain many overlapping or inconsistently written labels (for example, several variants of "SDG 9" and a long tail of company-size categories). Standardizing these categories would be a natural next improvement.

Measures created for the KPI cards: **Company Count**, **Total States**, **Total SDGs** and **Websites**.

## Tools and Technologies

- Microsoft Power BI Desktop
- Spreadsheet (Excel) data source
- Custom TopoJSON India map and image assets
- Slack and a timesheet for daily reporting during the internship

## Repository Structure

```
.
├── CSR_Funding_Dashboard.pbix   # Power BI report
└── README.md
```

## How to Run

1. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (Windows).
2. Clone this repository:
   ```bash
   git clone https://github.com/VenkatRohan07/CSR-Funding-Dashboard.git
   ```
3. Move into the project folder:
   ```bash
   cd CSR-Funding-Dashboard
   ```
4. Open `CSR_Funding_Dashboard.pbix` in Power BI Desktop and use the map and charts to filter the data interactively.

## Key Learnings

- Cleaning and preparing data for reporting
- Creating measures and KPIs in Power BI
- Choosing suitable visuals (map, bar, donut) for different questions
- Designing a clean, interactive single-page dashboard
- Working independently in a remote setup with daily progress updates and documentation

## Author

**Vattikonda Venkata Rohan Sasi Vardhan**
B.Tech, Computer Science & Engineering, KL University (Aziznagar Campus), Hyderabad

---

*Built as part of the Data Analyst Internship at StepUp for SDG (Pavdhan Technologies).*
