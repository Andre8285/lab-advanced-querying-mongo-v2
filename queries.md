![Ironhack Logo](https://i.imgur.com/1QgrNNw.png)

# Answers

### 1. All the companies whose name match 'Babelgum'. Retrieve only their `name` field.

<!-- Your Code Goes Here -->

{name:"Babelgum"}
{name:1,_id:0}

### 2. All the companies that have more than 5000 employees. Limit the search to 20 companies and sort them by **number of employees**.

<!-- Your Code Goes Here -->

Query: {number_of_employees:{$gte:5000}}
sort: {number_of_employees:1}
Limit:20 


### 3. All the companies founded between 2000 and 2005, both years included. Retrieve only the `name` and `founded_year` fields.

Query: { "founded_year": { "$gte": 2000, "$lte": 2005 } }
projection: { founded_year:1,name:1,_id:0}

<!-- Your Code Goes Here -->

### 4. All the companies that had a Valuation Amount of more than 100.000.000 and have been founded before 2010. Retrieve only the `name` and `ipo` fields.


<!-- Your Code Goes Here -->

### 5 All the companies that don't include the partners field.
Query: {partners: {$exists: false}}

### 6 All the companies that have a null type of value on the category_code field.
Query:  {category_code: {$type: 'null'}}

### 7 Order all the companies by their IPO price in descending order.
Sort :{IPO:-1}?

### 8 Retrieve the 10 companies with most employees, order by the number of employees.

Sort :{number_of_employees:-1}
limit:10


### 9 All the companies founded in the second semester of the year (July to December). Limit your search to 1000 companies.

Query: { "founded_month": { "$gte": 7, "$lte": 12 } }
limit: 1000

### 10 All the companies that have been founded on the first seven days of the month, including the seventh. Sort them by their acquisition price in descending order. Limit the search to 10 documents.

Query: { "founded_month": { "$lte": 7 } }
Sort :{acquisitions.price:-1}
limit: 10
