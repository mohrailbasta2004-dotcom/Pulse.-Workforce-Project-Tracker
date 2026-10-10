Pulse.Workforce & Project Tracker

# Every hour, traced back to a project.

A reporting layer over a normalized company schema — employees, departments and project hours all roll up into one view.

## Hours by project

# Who reports to whom.

Built from a single self-referencing `SupervisorId` column — no separate hierarchy table needed.

# Active work, by the hour.

Each project rolls up total hours logged and the people currently assigned to it.

# Headcount and pay, by department.

Aggregated straight from the employee table — no duplicated department data to keep in sync.

| Department | Employees | Avg. salary | Min | Max |
| --- | --- | --- | --- | --- |

# About this project

A reporting and management layer built on a classic company database: employees, departments and projects.

## The problem

A growing company needed visibility into who works where, who reports to whom, and how staff hours are actually distributed across active projects — without maintaining a separate org-chart tool by hand.

## What the schema covers

- A self-referencing `Employee → Supervisor` relationship, queried with a self-join
- A many-to-many `Employee ↔ Project` relationship carrying hours worked
- Aggregate reporting with `GROUP BY` — headcount and salary stats per department
- Views, triggers and stored procedures layered on top for day-to-day operations
- Formal normalization from a flat spreadsheet-style table through 1NF, 2NF and 3NF

## This demo

The dashboard, org chart and project totals above are reading from sample data shaped exactly like the underlying tables, simplified to run client-side for this showcase.

SQL Server / T-SQLSelf-JoinsAggregate Queries NormalizationViews & TriggersHTML / CSS / JS

Case study project — database design and T-SQL implementation by Mohrail Ezzat Basta.