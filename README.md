# AirBnb-MongoDB-project

## What is MongoDB and why is it important?

MongoDB is a **non relational database** designed to store and manage large volumes of unstructured or semi-structured data. MongoDB's utilization has been increasing worldwide, because it enables the following advantages:

* **Flexible schema** - Businesses constantly evolve, but relational databases often have rigid structures that make adapting difficult. In contrast, MongoDB offers a flexible schema, allowing it to easily adapt to changing businesses.
  
* **Horizontal Scaling** - MongoDB, like many other non-relational databases, is designed to support **horizontal scaling**. This means the database can be partitioned across multiple machines as data volume grows, enabling efficient distribution and management of large datasets. In contrast, relational databases are typically built for **vertical scaling**, which involves upgrading hardware, such as adding more CPU, RAM, or storage—to a single server. This approach has limitations and doesn't naturally support data partitioning across multiple nodes.


## Project Requirements

As part of the "Big Data Modelling and Management" course, my colleagues and I completed a notebook project using Airbnb data. The goal of this project is to answer the designated questions, which are divided into the following 3 sections: **Data Modelling**, **Uses for the database** and **Database updates**.

### Data Modelling 

The current database's performance is known to be low, given the lack of patterns and indexes. In addition, there is regular overwriting of data, which deletes valuable information for analysis, and additional issues, such as duplicated values and wrong timestamps. We must apply good practices to improve the database's performance, which means answering the following questions:

1) The most typical use case for the database is to show information relating to a property listing to a customer. This is done by a query to the database which returns one of the listing documents. Currently a lot of time is spent when a listing is retrieved from the database to show to a customer. Decide what information should be returned in a typical query and optimise the structure for this use case. For example, we typically only want a sample of reviews but not all reviews (although all reviews ), the customer does not need to know past transaction data, etc. Update the document schema for this typical use case. This may involve the creation of new collections and documents.  

2) Review the data for any errors (such as transactions that don’t fit the listing) or inappropriate duplication and clean up as appropriate. 

  
### Queries to database to answer the questions 

After addressing the Data Modelling, we needed to write queries to retrieve the necessary information for answering the following questions:

3)	Once per month we like to reward hosts with recognition. Pick three superhosts who have at least two property listings that can accommodate more than four people?

4)	One of employees is thinking of buying a property to rent out. Which bed type is most common in the listings that have waterfront and a dishwasher in New York?

5)	We are thinking of identifying someone to hire to write review for us professionally. What is the name of the reviewer who left the longest review in New York?

6)	We are thinking of trying to assess the security of different areas based on the security deposit required. What is the biggest and smallest difference between the price and deposit for security per number of visitors staying at the property?

7)	We want to identify areas by whether they are typically used for short breaks, like weekend mini breaks, or whether they are more suitable for long trips. We will use this information to target advertising of different customers. It is not expected this information will change much over time so we won’t look to update it we just would like a current view. What is the average duration of stay (in nights) per type of property per city (you can use the maximum_nights to measure length of stays)? For each property type return the city with the highest and lowest average value.

8)	We want to have a new webpage for hosts when setting up their account. It will list suggested typical amenities. This data will need to be available every time a host registers a property but is not expected to change very much. The starting point for the list will be all unique amenities currently listed in properties (across all documents). Optimise the database for this use case and show how the data should be queried.

9)	We want to start tracking our reviewers better. We want to create a webpage that shows the top 20 reviewers and the count of the number of reviews of each of these reviewers. This webpage should be kept up to date. It should also have a link to return the number of reviews for a given reviewer ID or Name (show how to query for number of reviews by ID or query quickly).

10)	For each property we store review scores across different metrics (accuracy, check-in, cleanliness etc). We are thinking we may soon add more metrics, although we don’t know what these will be. We want to be able to easily query the average score across all of these metrics, including any new metrics that might be added without changing the query. Adjust the data model so this can be done and show the query for an example property.

11)	We wish to be able to have better access to information about transaction, we wish to develop a search engine that can calculate the average value of transactions in a given period of time quickly for a given property.

12)	We wish to have a summary webpage that displays information about our top destinations. This webpage should display for each of the top 10 cities some basic information about our operations in the area (number of properties by type for example, average price by type) but you can choose the metrics. For each of the top 10 cities it should also provide some basic information about the top 3 properties in each city (price, number of review, whatever you think useful) to show an example of the properties available in the area. We would like to keep this webpage up to date as information changes.

### Database updates

After completing the initial tasks and optimising the database, we proceeded with the remaining assignments. For these, we had the flexibility to create and use fictional data as needed.

13)	Add a new property, this property should have a new host, and should be located in one of the top 10 cities. The host selects the top 10 most common amenities to be listed for the property.

14)	Add a new review to this property, the review should be from one of our top 20 reviewers.

15)	Add a new review metric called x_factor to the new document and give a score of 10. Show that the average across all metrics is correctly calculated for this listing, with the query you previously developed.


