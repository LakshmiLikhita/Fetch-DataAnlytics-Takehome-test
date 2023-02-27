# Fetch-DataAnlytics-Takehome-test

**Description of Data**

**Users:** The users table describes the user demographics such as gender, state, date of birth, id and the platform used to shop such as ios,android.
The "sign up source" column in a table that includes values such as "Apple," "Google," "Email," and "Facebook" likely refers to the source from which a user signed up for a particular service or platform.
This information can be useful for analyzing user behavior and identifying trends in how users sign up for a particular service or platform.

**Receipts:** The receipts table describes about the receipt details of each user, store name, transaction dates associated with purchase of item and mooney spent on each item (transaction amount).

**Receipt Items:** The receipt items table gives the details of each item mentioned in the receipt and its description, its barcode, brand name and final price of each item. Through analysis we can see that there are many items (reward receipt item ids) in each receipt. There are repetition of brands across different receipts.

**Brands:**  The brands table gives us the details of each brand, their category, its name and code and related brand id. The related brand id can be useful for business in many ways. If a business has multiple brands or products under a larger parent brand, the related brand ID can help to establish the brand hierarchy and identify the relationships between different brands. It can also be used to gain the insights of their competitors by analyzing their related brands.

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

After successful loading of data into master database, I have written the atached SQL queries (in MS SQL) for business questions given.

**Reference : SQL_Queries.pdf**

**Third: Choose something noteworthy about the data and share with a non-technical stakeholder**

I have developed a dashboard in Tableau with existing data to give the following insights to stakeholders:
- To forecast the Total items that will be purchased over the next quarter of 2023 so that the business can think about inventory management in the future
- Purchased items over each day of the week to let business know on which day is most of the business happening so that we can marketing strategies over the remaining days to improve the business.
- Quantity of items purchased across Bottom N States. Here I have given user the accessibility to filter on the number of states they chose to visualise for the least quantity purchased. By this metric, we can focus on the profitability of those particular least business states.

I have used "Use as filter " option to "Quantity Purchased over week sheet" to be applicable to the rest of the sheets.i.e., if we select any day on the first worksheet, the data gets filtered out to that particular day in the "Quantity Purchased Across State" worksheet.

**Exploratory Data Analysis:**

- When we look at Reward Points column from Receipt Items table, we see that data is populated to only 5.9% of the records. We are not sure if the data os not populated in the backend or reward points are not given to the users. This might be one of the important points to improve the business. So there is a need to eliminate the ambiguity.
- When we look at the Sign_up_platform column from Users table, we see that the there are only two known values like ios,android and rest of the columns are either unknown or nulls. The same ambiguity is repeated here as well. We need to work on importing and expanding the business to more platforms rather than limiting the options to two of them where there is a chance to loose our potential customers/users.
- 
**Recommendations:**
Based on the above analysis, Reward Points is one of the most important factor that can effect businesses marketing strategy and can lead to huge profits
To increase the customer loyalty, incentivize customers to make the purchase, and promote engagement with a brand by using the reward points as a tool for marketing. Below are few of the marketing strategies that businesses use for their growth:
- Businesses can encourage their customers to comeback and make additional purchases by offering the reward points for each purchase they made. 
- They can also help to increase the customer retention by providing an incentive for the customers to continue doing business with a brand.
- Reward points are used to engage the customers with a brand like signing up for a newsletter, following the brand on the social media, or providing the reviews on the product by offering the reward points.



**Reference : Tableau Visualization**

