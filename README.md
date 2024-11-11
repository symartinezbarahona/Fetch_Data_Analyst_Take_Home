# Fetch Data Analyst Take Home
## Overview
In this take home, I will demonstrate my ability to reason about data as well as showcase how I communicate findings and insights with stakeholders and business executives.

----
## Requirements
### 1. Explore the data
- Are there any data quality issues present?
- Are there any fields that are challenging to understand?

### 2. Provide SQL queries

Answer three of the following questions with at least one question coming from the closed-ended and one from the open-ended question set. Each question should be answered using one query.

Closed-ended questions:
- What are the top 5 brands by receipts scanned among users 21 and over?
- What are the top 5 brands by sales among users that have had their account for at least six months?
- What is the percentage of sales in the Health & Wellness category by generation?

Open-ended questions: for these, make assumptions and clearly state them when answering the question.
- Who are Fetch’s power users?
 - Which is the leading brand in the Dips & Salsa category?
 - At what percent has Fetch grown year over year?

### 3. Communicate with stakeholders
    
Construct an email or slack message that is understandable to a product or business leader who is not familiar with your day-to-day work. Summarize the results of your investigation. Include:
- Key data quality issues and outstanding questions about the data
- One interesting trend in the data
    - Use a finding from part 2 or come up with a new insight
- Request for action: explain what additional help, info, etc. you need to make sense of the data and resolve any outstanding issues

----

### Setup

1. Fork or clone this repo to your own computer and `cd` into the directory

2. Make sure you have the proper dependencies installed.
    - You can do this by typing `pip install -r requirements.txt` in the command line
---
## The Data

### Users Data Schema

Column | Definition
--- | -----------
id | unique identifier for each user 
created_date | date when the account was created
birth_date | the date of birth of each user
state | state abbreviation for where user resides
language | the language preference of the user
gender | gender of the user

----
----

### Transactions Data Schema

Column | Definition
--- | -----------
receipt_id | a unique identifier for each receipt submitted by a user
purchase_date | The date when the purchase was made
scan_date | the date when the user scanned and submitted the receipt
store_name | the name of the store where the purchase took place
user_id | a unique identifier for the user who submitted the receipt
barcode | a unique identifier for each product
final_quantity | the quantity of product purchased
final_sale | the final sale amount for the transaction or item. 

----
----

### Products Data Schema

Column | Definition
--- | -----------
category_1 | the department taxonomy for each product
category_2 | the super category taxonomy for each product
category_3 | the category taxonomy for each product
category_4 | the sub category taxonomy for each product
manufacturer | the company that produces the product
brand |  the specific brand name under which the product is marketed
barcode | a unique identifier for each product

-----
-----
### Entity Relationship Model

<img src="entity_relationship_model.png" alt="Alt text" width="750"/>