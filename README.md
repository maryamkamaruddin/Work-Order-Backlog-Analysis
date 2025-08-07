# Work-Order-Backlog-Dashboard

- About this project : Guided Project
- Tools : Excel, Power BI

Goal

This project was developed as part of a tutorial from EffectiveDashboards.com, guided by Jason Davidson, a reliability engineer focused on using Power BI for maintenance and reliability reporting.

The goal of the Work Order Backlog Analysis Dashboard is to enable site managers and department team leaders to quickly understand and take action on :
- The number of overdue work orders
- The total man-hours tied to those work orders
- The risk exposure due to outstanding maintenance tasks
- Responsibility for pending work

A work order is in backlog if :
- The current date is greater than the work order target finish date.
- AND the work order has not been completed.
- The dashboard supports decision-making by identifying which backlog work orders should be prioritized for inclusion in the next weekly maintenance schedule.

Data

The data was manually exported from a CMMS (Computerized Maintenance Management System) and imported into Power BI via Excel. The business record required from CMMS is Work Order dataset. The key dataset includes :
- Work Order Key, Description, and Status
- Data Extract Date
- Target Finish Dates
- Discipline (craft)
- Department
- Criticality (Safety, Environmental, Production, Routine)

The dataset helps assess backlog from multiple operational perspectives, including time, responsibility, and risk level.

Data Transformation

No major transformation was required. The data export was already formatted to meet the project's needs. However, several calculated columns and measures were created within Power BI to enrich the analysis:

Calculated Columns :
 - IsInBacklog - Flags if a work order is overdue and incomplete
 - Day In Backlog - Days since the target finish date
 - Days In Backlog Grouping - Categorical bands (e.g., >100, 50–100, 11–49, 1–10, Not in backlog)

Measures:
 - Work Order Planned Hours
 - Backlog (count)
 - Backlog (hours)

Data Modeling

A single-table model was sufficient for this analysis. Because the dataset is clean and compact, no relationships or complex modeling were necessary. All key analysis elements were built directly within this table, keeping the solution straightforward and maintainable.

Data Visualization


Page 1 - Insight into the overall status of the work order backlog
- Work Orders by Criticality
- Backlog Age Distribution
- Work Orders by Department and Discipline
- Includes a bookmark button to jump to the detailed view

![Image Alt](https://github.com/maryamkamaruddin/Work-Order-Backlog-Dashboard/blob/f38e57d955d049e3293a970d3835777435cecb6b/Work%20Order%20Backlog-images-0.jpg)


Page 2 - Tabular view of all work orders in backlog
- Helps users track and manage backlog items individually

![Image Alt](https://github.com/maryamkamaruddin/Work-Order-Backlog-Dashboard/blob/f38e57d955d049e3293a970d3835777435cecb6b/Work%20Order%20Backlog-images-1.jpg)


Conclusion

This dashboard demonstrates an efficient and practical way to monitor and manage maintenance backlog using Power BI. It empowers maintenance teams to :
- Quickly assess backlog volume and risk
- Prioritize overdue tasks for scheduling
- Allocate resources more effectively
- Improve asset reliability and operational safety
By minimizing complexity and maximizing clarity, this tool is ideal for routine use in high-demand maintenance environments.

source: https://effectivedashboards.com/ 
