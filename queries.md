![Ironhack Logo](https://i.imgur.com/1QgrNNw.png)

# Answers

### 1. All the companies whose name match 'Babelgum'. Retrieve only their `name` field.

<!-- Your Code Goes Here -->

_filter_: {name: "Babelgum"}{name:1,\_id:0},
_projection_: {name:1,\_id:0},
_sort_: `Your sort here`,
_skip_: `Your skip here`,
_limit_: `Your limit here`,

### 2. All the companies that have more than 5000 employees. Limit the search to 20 companies and sort them by **number of employees**.

<!-- Your Code Goes Here -->

_filter_: {number*of_employees : {$gt:5000}},
\_projection*: {name:1,\_id:0},
_sort_: `Your sort here`,
_skip_: `Your skip here`,
_limit_: 20,

### 3. All the companies founded between 2000 and 2005, both years included. Retrieve only the `name` and `founded_year` fields.

<!-- Your Code Goes Here -->

_filter_: {$and: [ {founded_year:{$gte:2000}}, {founded*year:{$lte:2005}} ] },
\_projection*: {name:1, founded*year:1, \_id:0},
\_sort*: `Your sort here`,
_skip_: `Your skip here`,
_limit_: `Your limit here`,

### 4. All the companies that had a Valuation Amount of more than 100.000.000 and have been founded before 2010. Retrieve only the `name` and `ipo` fields.

<!-- Your Code Goes Here -->

_filter_: {$and: [ {"ipo.valuation_amount": {$exists:true}}, {"ipo.valuation*amount":{$gt:100000000}}, {founded_year:{$lt:2010}} ]},
\_projection*: {name:1,ipo:1},
_sort_: `Your sort here`,
_skip_: `Your skip here`,
_limit_: `Your limit here`,

### 5. All the companies that have less than 1000 employees and have been founded before 2005. Order them by the number of employees and limit the search to 10 companies.

<!-- Your Code Goes Here -->

_filter_: {$and:[  {number_of_employees:{$lt:1000}}, {founded*year:{$lt:2005}} ]},
\_projection*: `Your projection here`,
_sort_: {number*of_employees:1},
\_skip*: `Your skip here`,
_limit_: 10,

### 6. All the companies that don't include the `partners` field.

<!-- Your Code Goes Here -->

_filter_: {partners:{$exists:false}},
_projection_: `Your projection here`,
_sort_: `Your sort here`,
_skip_: `Your skip here`,
_limit_: `Your limit here`,

### 7. All the companies that have a null type of value on the `category_code` field.

<!-- Your Code Goes Here -->

_filter_: {category*code:{$eq:null}},
\_projection*: `Your projection here`,
_sort_: `Your sort here`,
_skip_: `Your skip here`,
_limit_: `Your limit here`,

### 8. All the companies that have at least 100 employees but less than 1000. Retrieve only the `name` and `number of employees` fields.

<!-- Your Code Goes Here -->

_filter_: {$and: [ {number_of_employees:{$gte:100}}, {number*of_employees:{$lt:1000}}]},
\_projection*: {name:1, number*of_employees:1, \_id:0},
\_sort*: `Your sort here`,
_skip_: `Your skip here`,
_limit_: `Your limit here`,

### 9. Order all the companies by their IPO price in a descending order.

<!-- Your Code Goes Here -->

_filter_: `Your filter here`,
_projection_: `Your projection here`,
_sort_: {ipo:-1},
_skip_: `Your skip here`,
_limit_: `Your limit here`,

### 10. Retrieve the 10 companies with most employees, order by the `number of employees`

<!-- Your Code Goes Here -->

_filter_: `Your filter here`,
_projection_: {number*of_employees:1,name:1},
\_sort*: {number*of_employees:-1},
\_skip\*: `Your skip here`,
\_limit*: 10,

### 11. All the companies founded on the second semester of the year. Limit your search to 1000 companies.

<!-- Your Code Goes Here -->

_filter_: {$and: [ {founded_month:{$gte:4}},{founded*month:{$lte:7}} ] },
\_projection*: `Your projection here`,
_sort_: `Your sort here`,
_skip_: `Your skip here`,
_limit_: 1000,

### 12. All the companies founded before 2000 that have an acquisition amount of more than 10.000.000

<!-- Your Code Goes Here -->

_filter_: {$and: [ {founded_year:{$lt:2000}}, {"acquisition.price*amount":{$gt:10000000}} ] },
\_projection*: `Your projection here`,
_sort_: `Your sort here`,
_skip_: `Your skip here`,
_limit_: `Your limit here`,

### 13. All the companies that have been acquired after 2010, order by the acquisition amount, and retrieve only their `name` and `acquisition` field.

<!-- Your Code Goes Here -->

_filter_: {$and: [{"acquisition.price_amount":{$gte:10000000}}, {"acquisition.acquired*year":{$gt:2000}} ]},
\_projection\*: {name:1, acquisition:1, \_id:0},
\_sort*: `Your sort here`,
_skip_: `Your skip here`,
_limit_: `Your limit here`,

### 14. Order the companies by their `founded year`, retrieving only their `name` and `founded year`.

<!-- Your Code Goes Here -->

_filter_: `Your filter here`,
_projection_: `Your projection here`,
_sort_: `Your sort here`,
_skip_: `Your skip here`,
_limit_: `Your limit here`,

### 15. All the companies that have been founded on the first seven days of the month, including the seventh. Sort them by their `acquisition price` in a descending order. Limit the search to 10 documents.

<!-- Your Code Goes Here -->

_filter_: `Your filter here`,
_projection_: `Your projection here`,
_sort_: `Your sort here`,
_skip_: `Your skip here`,
_limit_: `Your limit here`,

### 16. All the companies on the 'web' `category` that have more than 4000 employees. Sort them by the amount of employees in ascending order.

<!-- Your Code Goes Here -->

_filter_: `Your filter here`,
_projection_: `Your projection here`,
_sort_: `Your sort here`,
_skip_: `Your skip here`,
_limit_: `Your limit here`,

### 17. All the companies whose acquisition amount is more than 10.000.000, and currency is 'EUR'.

<!-- Your Code Goes Here -->

_filter_: `Your filter here`,
_projection_: `Your projection here`,
_sort_: `Your sort here`,
_skip_: `Your skip here`,
_limit_: `Your limit here`,

### 18. All the companies that have been acquired on the first trimester of the year. Limit the search to 10 companies, and retrieve only their `name` and `acquisition` fields.

<!-- Your Code Goes Here -->

_filter_: `Your filter here`,
_projection_: `Your projection here`,
_sort_: `Your sort here`,
_skip_: `Your skip here`,
_limit_: `Your limit here`,

### 19. All the companies that have been founded between 2000 and 2010, but have not been acquired before 2011.

<!-- Your Code Goes Here -->

_filter_: `Your filter here`,
_projection_: `Your projection here`,
_sort_: `Your sort here`,
_skip_: `Your skip here`,
_limit_: `Your limit here`,
