# Complaint Management System

## 📌 Project Overview

The Complaint Management System is a MySQL-based database project designed to store, manage, track, and analyze customer complaints.

The system helps manage complaints from registration to assignment, resolution, feedback, escalation, and SLA monitoring.

## 🎯 Project Objectives

- Store customer and employee information
- Record and manage customer complaints
- Assign complaints to employees
- Track complaint status and priority
- Manage complaint resolutions
- Collect customer feedback
- Track escalated complaints
- Monitor SLA violations
- Generate useful reports using SQL

## 🛠️ Technologies Used

- MySQL
- MySQL Workbench
- SQL

## 🗄️ Database Tables

The project contains the following tables:

1. Departments
2. Users
3. Employees
4. Complaint_Category
5. Priority
6. Complaint_Status
7. Complaints
8. Complaint_Assignment
9. Resolution
10. Feedback
11. Escalation
12. SLA

## 📊 SQL Concepts Used

- SELECT
- INSERT
- UPDATE
- DELETE
- WHERE
- ORDER BY
- GROUP BY
- HAVING
- Aggregate Functions
- Joins
- Subqueries
- CTEs
- Window Functions
- Views
- Stored Procedures
- Triggers
- Date Functions

## 📈 Reports

The project includes reports for:

- Complaint Summary by Priority
- Complaint Summary by Category
- Department Performance
- Employee Performance
- SLA Violation Report

## 🔍 Project Analysis

The database can be used to analyze:

- Number of complaints
- Complaint categories
- Complaint priorities
- Employee performance
- Department performance
- Complaint resolutions
- Customer feedback
- SLA violations

## 🚀 How to Run the Project

1. Install MySQL and MySQL Workbench.
2. Open MySQL Workbench.
3. Create or select a database.
4. Open the `complaint_management_correct.sql` file.
5. Execute the SQL script.
6. The database tables, data, views, procedures, and other SQL objects can then be used for analysis.

## 📚 Learning Outcomes

Through this project, I practiced database design, SQL queries, joins, aggregations, subqueries, CTEs, window functions, views, stored procedures, and data analysis.

## 👩‍💻 Author

**Punidhasri S**

Aspiring Data Analyst  
Skills: Excel | SQL | Python | Power BI | Data Analytics
## 🗂️ Database Structure

The Complaint Management System consists of 12 related tables:

| Table | Purpose |
|---|---|
| Departments | Stores department details |
| Users | Stores customer/user information |
| Employees | Stores employee details |
| Complaint_Category | Stores complaint categories |
| Priority | Stores complaint priority levels |
| Complaint_Status | Stores complaint status |
| Complaints | Stores customer complaints |
| Complaint_Assignment | Stores complaint assignments |
| Resolution | Stores complaint resolutions |
| Feedback | Stores customer feedback |
| Escalation | Stores escalated complaints |
| SLA | Stores Service Level Agreement details |

### 🔗 Main Relationships

- Users → Complaints
- Complaint_Category → Complaints
- Complaint_Status → Complaints
- Priority → Complaints
- Employees → Complaint_Assignment
- Complaints → Complaint_Assignment
- Complaints → Resolution
- Complaints → Feedback
- Complaints → Escalation
- Departments → Employees
- 
- ## ⭐ Key Features

- Customer complaint registration
- Complaint category and priority management
- Complaint status tracking
- Employee complaint assignment
- Complaint resolution tracking
- Customer feedback management
- Complaint escalation tracking
- SLA monitoring
- Employee performance analysis
- Department performance analysis
- SQL-based reports and analysis

- ## 📊 Project Reports

The project includes the following SQL reports:

1. **Complaint Summary by Priority**
   - Analyzes complaints based on priority levels.

2. **Complaint Summary by Category**
   - Analyzes the number of complaints in each category.

3. **Department Performance**
   - Analyzes complaint handling across departments.

4. **Employee Performance**
   - Analyzes complaints handled by employees.

5. **SLA Violation Report**
   - Identifies complaints that exceeded the SLA.

## 🔎 Sample SQL Analysis

### 1. Total Number of Complaints

```sql
SELECT COUNT(*) AS total_complaints
FROM Complaints;

SELECT 
    p.priority_name,
    COUNT(c.complaint_id) AS total_complaints
FROM Complaints c
JOIN Priority p
    ON c.priority_id = p.priority_id
GROUP BY p.priority_name
ORDER BY total_complaints DESC;

SELECT 
    employee_id,
    COUNT(complaint_id) AS total_complaints,
    RANK() OVER (
        ORDER BY COUNT(complaint_id) DESC
    ) AS employee_rank
FROM Complaint_Assignment
GROUP BY employee_id;

## 📌 Project Insights

Using SQL analysis, the project can help identify:

- Which complaint categories receive the most complaints
- Which priorities have the highest number of complaints
- Employee complaint handling performance
- Department-level complaint performance
- Complaints that exceed SLA limits
- Complaint resolution and customer feedback patterns
- Areas where complaint management can be improved

## 🚀 Future Enhancements

The project can be further enhanced by:

- Adding a Power BI dashboard
- Adding more advanced SQL analysis
- Automating complaint reports
- Adding real-time complaint tracking
- Improving SLA monitoring
- Adding additional performance metrics
