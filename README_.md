# 🏏 Cricket Analysis – Power BI Dashboard

> A role-based player analysis and team selection dashboard built in Power BI. It shortlists players for each batting and bowling role using performance parameters, and puts together a **Final Playing XI**.

![Power BI](https://img.shields.io/badge/Tool-Power%20BI-F2C811?logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/Language-DAX-blue)
![Domain](https://img.shields.io/badge/Domain-Cricket%20Analytics-green)

---

## 📑 Table of Contents

1. [Project Overview](#-project-overview)
2. [Problem Statement](#-problem-statement)
3. [Dashboard Preview](#-dashboard-preview)
4. [Data Model](#-data-model)
5. [Key Measures (KPIs)](#-key-measures-kpis)
6. [Report Pages](#-report-pages)
7. [Key Insights](#-key-insights)
8. [How to Use](#-how-to-use)
9. [Tech Stack](#-tech-stack)
10. [Project Structure](#-project-structure)
11. [Author](#-author)

---

## 📌 Project Overview

This project analyses cricket player performance data to answer one question: **which players are the best fit for each role in a team?**

Instead of ranking players on raw runs or wickets alone, the dashboard evaluates them role by role (openers, anchors, finishers, all-rounders, fast bowlers). Each role is judged on the metrics that matter for it, such as strike rate and boundary % for power hitters, or economy and dot-ball % for bowlers. The analysis ends with a **Final 11** selection.

---

## 🎯 Problem Statement

Selecting a balanced playing XI means looking beyond headline numbers. The goals of this project are to:

- Identify **power hitters / openers** using strike rate, boundary % and batting average.
- Identify **anchors / middle-order** batters using average, balls faced and consistency.
- Identify **finishers and lower-order anchors** who can bat and bowl.
- Identify **all-rounders** who contribute with both bat and ball.
- Identify **specialist fast bowlers** using economy, bowling average, bowling strike rate and dot-ball %.
- Build the **final team** from the shortlisted players.

---

## 🖼️ Dashboard Preview

> 📸 *Add the screenshots for each page below. Images should be saved in an `images/` folder.*

### Page 1 – Power Hitters / Openers

<!-- Replace the line below with your screenshot -->
![Power Hitters / Openers](images/page1_power_hitters_openers.png)

*(Screenshot placeholder – Page 1)*

<br><br>

---

### Page 2 – Anchors / Middle Order

<!-- Replace the line below with your screenshot -->
![Anchors / Middle Order](images/page2_anchors_middle_order.png)

*(Screenshot placeholder – Page 2)*

<br><br>

---

### Page 3 – Finisher / Lower Order Anchor

<!-- Replace the line below with your screenshot -->
![Finisher / Lower Order Anchor](images/page3_finisher_lower_order.png)

*(Screenshot placeholder – Page 3)*

<br><br>

---

### Page 4 – All Rounders / Lower Middle Order

<!-- Replace the line below with your screenshot -->
![All Rounders / Lower Middle Order](images/page4_all_rounders.png)

*(Screenshot placeholder – Page 4)*

<br><br>

---

### Page 5 – Specialist Fast Bowlers / Tail End

<!-- Replace the line below with your screenshot -->
![Specialist Fast Bowlers / Tail End](images/page5_fast_bowlers_tail_end.png)

*(Screenshot placeholder – Page 5)*

<br><br>

---

### Page 6 – Final Team (The Final 11)

<!-- Replace the line below with your screenshot -->
![Final Team](images/page6_final_team.png)

*(Screenshot placeholder – Page 6)*

<br><br>

---

### Page 7 – Player Details by Match (Tooltip Page)

<!-- Replace the line below with your screenshot -->
![Player Details by Match](images/page7_player_details_tooltip.png)

*(Screenshot placeholder – Page 7. This is a hidden tooltip page that appears when you hover over a player.)*

<br><br>

---

## 🗂️ Data Model

The report uses a star-schema-style model with the following tables:

| Table | Type | Description |
|-------|------|-------------|
| `dim_players` | Dimension | Player details: name, batting style, bowling style, playing role, image, description |
| `dim_match_summary` | Dimension | Match details including tournament **stage** (used as a slicer) |
| `fact_batting_summary` | Fact | Match-level batting records per player |
| `fact_batsman_summary` | Fact | Aggregated batting summary per player (position, innings, balls faced, team) |
| `fact_bowling_summary` | Fact | Bowling records per player (balls bowled, runs conceded, wickets, maidens) |
| `Key_Measures` | Measures table | Central table that stores all DAX measures |
| `Parameter` | Parameter table | What-if / field parameter used for the consolidated parameters filtering |

> 📸 *Add a screenshot of the Model view here:*

<!-- Replace the line below with your screenshot -->
![Data Model](images/data_model.png)

*(Screenshot placeholder – Data Model view)*

<br><br>

---

## 📐 Key Measures (KPIs)

| Category | Measures |
|----------|----------|
| **Batting** | Total Runs, Batting Avg, Strike Rate, Boundary %, Total Innings Batted, Average Balls Faced, Total Balls Faced |
| **Bowling** | Wickets, Economy, Bowling Average, Bowling Strike Rate, Dot Ball %, Balls Bowled, Runs Conceded, Maidens, Total Innings Bowled |

---

## 📄 Report Pages

| # | Page | Purpose | Main Visuals |
|---|------|---------|--------------|
| 1 | **Power Hitters / Openers** | Shortlist aggressive top-order batters | Parameters panel, shortlist table, scatter chart (Batting Avg vs Strike Rate), KPI cards |
| 2 | **Anchors / Middle Order** | Shortlist stable middle-order batters | Parameters panel, shortlist table, scatter chart, KPI cards (Avg, SR, Avg Balls Faced) |
| 3 | **Finisher / Lower Order Anchor** | Find lower-order batters who can also bowl | Table, scatter chart, cards for Batting Avg, Strike Rate, Economy, Bowling SR |
| 4 | **All Rounders / Lower Middle Order** | Shortlist players who contribute with bat and ball | Combined batting + bowling table, scatter chart, KPI cards |
| 5 | **Specialist Fast Bowlers / Tail End** | Shortlist pace bowlers | Bowling table, scatter chart (Economy vs Bowling SR), cards for Economy, Bowling Avg, Dot Ball % |
| 6 | **Final Team** | Display the final selected XI | Player table with images, roles and stats; player slicer |
| 7 | **Player Details by Match** *(Tooltip)* | Match-by-match drill-down on hover | Player image, description, batting and bowling match tables |

**Interactivity:** most pages have a **Stage slicer** (filter by tournament stage). Scatter charts and tables are cross-filtered, and the tooltip page shows match-level detail on hover.

---

## 💡 Key Insights

> ✏️ *Fill this section in with your own findings after reviewing the dashboard. Suggested format:*

- **Best power hitter / opener:** `<player name>` – Strike Rate: `<value>`, Boundary %: `<value>`
- **Best anchor:** `<player name>` – Batting Avg: `<value>`
- **Best finisher:** `<player name>` – `<value>`
- **Best all-rounder:** `<player name>` – `<batting + bowling stats>`
- **Best fast bowler:** `<player name>` – Economy: `<value>`, Dot Ball %: `<value>`
- **Final XI:** `<list the 11 players>`

---

## 🚀 How to Use

1. Download or clone this repository.
2. Open `cricket_analysis_bi.pbix` in **Power BI Desktop** (latest version recommended).
3. If prompted, click **Refresh** so the data loads.
4. Use the page tabs at the bottom to move through the roles.
5. Use the **Stage** slicer to filter by tournament stage.
6. Hover over a player in a table or scatter chart to open the match-by-match tooltip.

---

## 🛠️ Tech Stack

- **Power BI Desktop** – visualisation and reporting
- **DAX** – measures and calculations
- **Power Query** – data cleaning and transformation
- **Data Modelling** – star schema with fact and dimension tables

---

## 📁 Project Structure

```
cricket-analysis-bi/
│
├── cricket_analysis_bi.pbix      # Power BI report file
├── README.md                     # Project documentation
└── images/                       # Dashboard screenshots
    ├── page1_power_hitters_openers.png
    ├── page2_anchors_middle_order.png
    ├── page3_finisher_lower_order.png
    ├── page4_all_rounders.png
    ├── page5_fast_bowlers_tail_end.png
    ├── page6_final_team.png
    ├── page7_player_details_tooltip.png
    └── data_model.png
```

---

## 👤 Author

| | |
|---|---|
| **Name** | `<Your Full Name>` |
| **Role** | `<e.g. Data Analyst / Power BI Developer / Student>` |
| **Location** | `<City, State, Country>` |
| **Email** | `<your.email@example.com>` |
| **LinkedIn** | [`linkedin.com/in/<your-handle>`](https://linkedin.com/in/your-handle) |
| **GitHub** | [`github.com/<your-username>`](https://github.com/your-username) |
| **Portfolio** | `<your-portfolio-link>` |

---

## 📜 License

This project is for educational and portfolio purposes. Feel free to use it as a reference, and please give credit if you do.

---

⭐ *If you found this project useful, consider giving it a star!*
