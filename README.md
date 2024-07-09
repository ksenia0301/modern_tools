# Setting up Azure PostgreSQL Database with DBeaver

## Connecting to Azure PostgreSQL Database

1. **Open DBeaver:**
   - Launch the DBeaver application on your computer.

2. **Create a New Connection:**
   - Click on the "New Database Connection" button in the toolbar at the top left side, or click on the "Database" menu and select "New Database Connection".

3. **Select PostgreSQL:**
   - In the "Connect to a database" dialog, choose "PostgreSQL" from the list of available databases and click "Next".

4. **Configure Connection Details:**
   - **General Tab:**
     - **Name**: Azure PostgreSQL
   - **Connection Tab:**
     - **Host**: surfalytics-prod.postgres.database.azure.com
     - **Port**: 5432 (or 6432 if using PgBouncer)
     - **Database**: postgres
     - **Username**: surfalyticsadmin
     - **Password**: Data2024!
   - **SSL Tab:**
     - Check "Use SSL" for secure connections.

5. **Test Connection and Save:**
   - Click "Test Connection" to ensure connectivity.
   - Click "Finish" to save the connection.

## Creating Database and Schema, Ingesting Tables

1. **Create a New Database:**
   - Execute `CREATE DATABASE SURFALYTICS_DW_<YOUR_UNIQUE_NAME>;` in the SQL Editor.

2. **Create Schema:**
   - Execute `CREATE SCHEMA STG;` in the SQL Editor.

3. **Create `orders` Table:**
   ```sql
   CREATE TABLE STG.orders (
       Row_ID SERIAL PRIMARY KEY,
       Order_ID INT,
       Returned BOOLEAN,
       Order_Date DATE,
       Period VARCHAR(50),
       Ship_Date DATE,
       Ship_Mode VARCHAR(50),
       Customer_ID INT,
       Customer_Name VARCHAR(100),
       Segment VARCHAR(50),
       Country VARCHAR(50),
       City VARCHAR(50),
       State VARCHAR(50),
       Postal_Code VARCHAR(20),
       Region VARCHAR(50),
       Person VARCHAR(50),
       Product_ID INT,
       Category VARCHAR(50),
       Sub_Category VARCHAR(50),
       Product_Name VARCHAR(100),
       Sales DECIMAL(10, 2),
       Quantity INT,
       Discount DECIMAL(5, 2),
       Profit DECIMAL(10, 2),
       OrderCount INT,
       CustomerCount INT
   );
