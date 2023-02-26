# Fetch-DataAnlytics-Takehome-test

**Description of Data**

**Users:** The users table describes the user demographics such as gender, state,date of birth,id and the platform used to shop such as ios,android.
The "sign up source" column in a table that includes values such as "Apple," "Google," "Email," and "Facebook" likely refers to the source from which a user signed up for a particular service or platform.
This information can be useful for analyzing user behavior and identifying trends in how users sign up for a particular service or platform.

**Receipts:** The receipts table describes re


**First: Review Existing Data and Diagram a New Structured Relational Data Model**
I used MySQL to draw the ER Diagram.
- Each user may have different receipts. So one user id in Users table will have multiple receipt ids in receipts table. So, I put **"One to many"**  relationship between Users and Receipts table.
- Each receipt will have many items tagged to it. So I put **"One to many"** relationship between Receipts and Receipt_Items table
- 
**Refererence : ER Diagram.pdf**


**Second: Write a query that directly answers question(s) from a business stakeholder**

I first installed **Microsoft Sql Server Management Studio 2014** and set up my local server. 
I also installed **Microsoft ACE OLEDB 12.0 drivers** to load data from csv into sql table.

I then imported csv files into **master** database and created tables for each of the files by clicking on Tasks-> Import Data. 
Then the SQL Server Import Wizard opens up to create a new destination table and then edit the mappings to load data from csv files.

After successful loading of data into master database, I have written the atached SQL queries for business questions given.

**Reference : SQL_Queries.pdf**

**Third: Choose something noteworthy about the data and share with a non-technical stakeholder**

