#  Cricket Analysis – Power BI Dashboard

> A role-based player analysis and team selection dashboard built in Power BI. It shortlists players for each batting and bowling role using performance parameters, and puts together a **Final Playing XI**.

![Power BI](https://img.shields.io/badge/Tool-Power%20BI-F2C811?logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/Language-DAX-blue)
![Domain](https://img.shields.io/badge/Domain-Cricket%20Analytics-green)

---

---

##  Project Overview

This project analyses cricket player performance data to answer one question: **which players are the best fit for each role in a team?**

Instead of ranking players on raw runs or wickets alone, the dashboard evaluates them role by role (openers, anchors, finishers, all-rounders, fast bowlers). Each role is judged on the metrics that matter for it, such as strike rate and boundary % for power hitters, or economy and dot-ball % for bowlers. The analysis ends with a **Final 11** selection.

---

##  Problem Statement

Selecting a balanced playing XI means looking beyond headline numbers. The goals of this project are to:

- Identify **power hitters / openers** using strike rate, boundary % and batting average.
- Identify **anchors / middle-order** batters using average, balls faced and consistency.
- Identify **finishers and lower-order anchors** who can bat and bowl.
- Identify **all-rounders** who contribute with both bat and ball.
- Identify **specialist fast bowlers** using economy, bowling average, bowling strike rate and dot-ball %.
- Build the **final team** from the shortlisted players.

---
##  Dashboard Preview

> 📸 *Add the screenshots for each page below. Images should be saved in an `images/` folder.*

### Page 1 – Power Hitters / Openers

<img width="750" height="426" alt="image" src="https://github.com/user-attachments/assets/81ecde17-8ca0-44fa-934e-d1775a5de052" />




<br><br>

---

### Page 2 – Anchors / Middle Order

<img width="747" height="425" alt="image" src="https://github.com/user-attachments/assets/ef5d16b6-e582-48d9-9fc2-31db16fad01a" />


<br><br>

---

### Page 3 – Finisher / Lower Order Anchor
<img width="763" height="432" alt="image" src="https://github.com/user-attachments/assets/0b3dd407-4030-4c4f-8891-112e159f5eff" />


<br><br>

---

### Page 4 – All Rounders / Lower Middle Order
<img width="766" height="425" alt="image" src="https://github.com/user-attachments/assets/66cb2897-b961-41a3-a3eb-9386514ba068" />


<br><br>

---

### Page 5 – Specialist Fast Bowlers / Tail End
<img width="772" height="412" alt="image" src="https://github.com/user-attachments/assets/7e3d90f3-64b5-47b1-87ea-0ab1f5f4cfc8" />


<br><br>

---

### Page 6 – Final Team (The Final 11)

<img width="770" height="425" alt="image" src="https://github.com/user-attachments/assets/829ca7cd-1085-4c97-a1f5-a963407f0004" />


<br><br>

---

### Page 7 – Player Details by Match (Tooltip Page)
<img width="782" height="427" alt="image" src="https://github.com/user-attachments/assets/c6f1300b-7350-4dab-9b41-b267371b2abb" />

<br><br>

---

##  Data Model
<img width="822" height="642" alt="image" src="https://github.com/user-attachments/assets/fd8028d6-2942-4459-9a79-9f596fb51b29" />


<br><br>

---

## 📐 Key Measures (KPIs)

| Category | Measures |
|----------|----------|
| **Batting** | Total Runs, Batting Avg, Strike Rate, Boundary %, Total Innings Batted, Average Balls Faced, Total Balls Faced |
| **Bowling** | Wickets, Economy, Bowling Average, Bowling Strike Rate, Dot Ball %, Balls Bowled, Runs Conceded, Maidens, Total Innings Bowled |


---

##  Key Insights

>  *Fill this section in with your own findings after reviewing the dashboard. Suggested format:*

- **Best power hitter / opener:** `<player name>` – Strike Rate: `<value>`, Boundary %: `<value>`
- **Best anchor:** `<player name>` – Batting Avg: `<value>`
- **Best finisher:** `<player name>` – `<value>`
- **Best all-rounder:** `<player name>` – `<batting + bowling stats>`
- **Best fast bowler:** `<player name>` – Economy: `<value>`, Dot Ball %: `<value>`
- **Final XI:** `<list the 11 players>`

---



---

##  Tech Stack

- **Power BI Desktop** – visualisation and reporting
- **DAX** – measures and calculations
- **Power Query** – data cleaning and transformation
- **Data Modelling** – star schema with fact and dimension tables

--
##  Author

| | |
|---|---|
| **Name** | Atharva Lambde |
| **Email** | [atharvalambde@gmail.com](mailto:atharvalambde@gmail.com) |
| **LinkedIn** | [linkedin.com/in/atharva-lambde](https://www.linkedin.com/in/atharva-lambde/) |
| **GitHub** | [github.com/atharvagit22](https://github.com/atharvagit22) |



