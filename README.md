# Dimensional Modeling Project with Azure Postgre, dbt Core and Looker

## Overview

This project demonstrates the implementation of a dimensional model on a remote PostgreSQL database hosted on Azure, using DBeaver for ETL processes. Dimensional modeling is a data modeling technique used to structure data warehouses for efficient querying and reporting. The project includes the design and deployment of a star schema to support business intelligence and data analytics.

## Table of Contents

[Getting Started](#getting-started)
[Prerequisites](#prerequisites)
[Project tasks](#project-tasks)

## Getting Started

### Prerequisites
PostgreSQL client
Azure account with a PostgreSQL database instance
VSCode
git
DBeaver

### Project tasks
[Week 1](#Week1): Clone the repo and access it using VS Code
[Week 2](#week-2): Load data to PostgreSQL

### Week 1
Create new repository in GitHub, and launch VSCode
In VSCode open terminal  navigating to View > Terminal
Clone repository: git clone https://github.com/ksenia0301/modern_tools.git

### Week 2
Open DBeaver.

Click on the New Database Connection button or navigate to Database > New Database Connection.

Select PostgreSQL from the list of database drivers and click Next.

Enter the connection details:

   - Host: your-db-host
   - Port: 5432
   - Database: your-db-name
   - Username: your-db-user
   - Password: your-db-password

Create database and schema in DBeaver with SQL:

