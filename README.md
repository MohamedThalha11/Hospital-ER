# Hospital Emergency Room Power BI Dashboard

## Problem Statement
Emergency departments handle high, unpredictable patient volumes, which can lead to long wait times, uneven resource allocation, and reduced patient satisfaction.  
Hospital leaders need a clear, data‑driven view of ER performance to identify bottlenecks, plan staffing, and improve patient experience.

## Objective
- Monitor the volume and profile of ER patients over time.  
- Track operational KPIs such as wait time, admission rate, and referrals to departments.  
- Evaluate patient satisfaction and timeliness of service.  
- Provide drill‑down views at monthly and patient‑level granularity for deeper analysis.

## My Role
- Defined analytical requirements and KPIs for the ER dashboard.  
- Performed data understanding and basic cleaning.  
- Designed the data model (fact table + date table).  
- Created DAX measures and calculated columns for metrics and segmentation.  
- Built and formatted the Power BI dashboards (Consolidated, Monthly, and Patient Details).  
- Documented insights and business implications.

## Tools Used
- Power BI Desktop – data modeling, DAX, and dashboard development.  
- SQL – data exploration and validation (optional for host DB).  
- Excel – initial data review and sanity checks.  

## Dataset Summary
- Records: One row per ER visit.  
- Time period: Multiple months across 2023–2024 (can be filtered by date range or month).  
- Key fields:
  - Patient Id  
  - Patient Admission Date  
  - Patient Gender  
  - Patient Age and derived Age Group  
  - Patient Race  
  - Department Referral  
  - Patient Admission Flag (Admitted / Not Admitted)  
  - Patient Satisfaction Score  
  - Patient Wait Time (minutes)  
  - Case Manager (Patients CM)  

A separate Date table is used to support Year, Month, Month & Year, Weekday, and other time‑intelligence calculations.

## Key Insights & Business Impact

- A significant share of visits occur during evening hours, indicating a need to strengthen late‑shift staffing.  
- Average wait time is highest on specific weekdays, suggesting scheduling or triage improvements for those days.  
- Certain departments (e.g., General Practice and Orthopedics) receive the highest referrals, highlighting where additional physicians or beds may be required.  
- Roughly half of ER visitors are not admitted, implying opportunities to optimize triage protocols and outpatient pathways.  
- Most patients are seen within 30 minutes, but a measurable segment breach the target, directly impacting satisfaction scores.

## Metrics, DAX Measures, and Analytical Logic
The dashboard is driven by core DAX measures (stored in a separate `dax/` subfolder):

Main metrics:
- **Total Patients** – counts total ER visits.  
- **Total Patients Referred** – counts visits where a department referral is present.  
- **Average Wait Time** – average of Patient Wait Time.  
- **Average Satisfaction Score** – average of Patient Satisfaction Score.  
- **Admitted Patients** – count where Admission Flag = TRUE.  
- **Not Admitted Patients** – count where Admission Flag = FALSE.  
- **Patients Seen Within 30 Minutes** – count where Wait Time ≤ 30 minutes.  
- **% Seen Within 30 Minutes** – ratio of patients within target to total patients.  
- **Age Group** – calculated column to bucket patients into 10‑year ranges.

These measures power:
- KPI cards and monthly trend lines.  
- Donut charts for gender and admission split.  
- Bar charts by age group and department.  
- A heatmap for patients by day and hour to reveal peak times.

## What Decisions Can Be Made from the Findings
- **Staffing decisions:** Adjust number of doctors, nurses, and triage staff by day and hour based on peak volume patterns.  
- **Resource allocation:** Allocate beds, diagnostic equipment, and support staff to high‑referral departments.  
- **Process optimization:** Improve check‑in and triage flow on days/hours with long waits or low satisfaction.  
- **Strategic planning:** Use admission vs non‑admission patterns to evaluate the need for observation units or fast‑track outpatient services.

## Business Problems Addressed
- Lack of visibility into when and where ER congestion happens.  
- Difficulty in quantifying the relationship between wait time and satisfaction.  
- Limited understanding of which patient segments (age, gender, race) drive ER demand.  
- No consolidated view combining operational KPIs and patient‑level details for root‑cause analysis.

## Learning Outcomes
By working through this project, the following skills are demonstrated:

- Translating a real‑world healthcare problem into measurable KPIs and visuals.  
- Building a simple star schema (fact + date dimension) for reporting.  
- Writing DAX measures for counts, averages, percentages, and segmentation.  
- Designing slicer‑driven, multi‑page Power BI dashboards (KPI cards, bar charts, donut charts, heatmaps, and tables).  
- Communicating insights and business impact in a portfolio‑ready format.

## Contact
If you have feedback or would like to discuss this project:

- **Name:** *Mohamed Thalha* 
- **Email:** *mohamedthalha110@gmail.com*  
- **LinkedIn:** *www.linkedin.com/in/mohamed-thalha-8b6a18267*  
- **Portfolio / GitHub:** *https://github.com/your‑username*

