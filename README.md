# SQL-project (In progress)
In this SQL project we have created a <b>MS SQL Server database</b> with using dummy real world dataset generated from [generatedata.com](https://generatedata.com/) <span>&#8594;</span> Defined database structure and modified data using T-SQL queries to maintain data uniformity in database <span>&#8594;</span> Used medium-complex DQL queries to answer & visualize data-driven insights from data available in this normalized database using different types of JOINs, Aggregations, CTEs, Sub-Queries as per requirement.

<I> Below we have given a brief description of the database architecture and also screenshots are given for for queries and results of various insights retrieved from the database in different complex requirement scenarios </I>

**ER Diagram**
 
**Entities**

* User (__userId__, name, phoneNum)
* Buyer (__userId__)
* Seller (__userId__)
* Bank Card (__cardNumber__, userId, bank, expiryDate)
* Credit Card (__cardNumber__, organization)
* Debit Card (__cardNumber__)
* Store (__sid__, name, startTime, customerGrade, streetAddr, city, province)
* Product (__pid__, sid, name, brand, type, amount, price, colour, customerReview, modelNumber)
* Order Item (__itemid__, pid, price, creationTime)
* Order (__orderNumber__, creationTime, paymentStatus, totalAmount)
* Address (__addrid__, userid, name, city, postalCode, streetAddr, province, contactPhoneNumber)

**Relationships**

* Manage (__userid__, __sid__, SetupTime) (userid ref Seller, sid ref Store)
* Save to Shopping Cart (__userid__, __pid__, quantity, addtime) (userid ref Buyer, pid ref Product)
* Contain (__orderNumber__, __itemid__, quantity) (orderNumber ref Order, itemid ref Order Item)
* Deliver To (__addrid__, __orderNumber__, TimeDelivered) (addrid ref Address, orderNumber ref Order)
* Payment (__C.cardNumber__, __orderNumber__, payTime) (C.cardNumber ref Credit Card, orderNumber ref Order)


**Create Database**
* [Table creation.sql](https://github.com/Nilashis-Halder/Online-Retail-App-SQL-project/blob/main/Table%20creation.sql): Create tables for entities and relationships above.
* [Insert data.sql](https://github.com/Nilashis-Halder/Online-Retail-App-SQL-project/blob/main/Insert%20data.sql): Insert datas into tables.
* [Modification.sql](): Modify the data.

