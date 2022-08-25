# **T2A1-A - Workbook**  
**Name:** Wade Doolan  
**Student number:** 12678  

<hr>   

## **Question 1:**  

*Describe the architecture of a typical Flask application.*  




<hr>  

## **Question 2:**  

*Identify a database management system (DBMS) commonly used in web applications (including Flask) and discuss the pros and cons of this database.*  

PostgreSQL is an open source, object-relational database system the utilises the Structured Query Language (SQL)(Postgresql.org, 2022). PostreSQL works well for many programming languages including Pythin, .Net, C, C++, Java Node.js(JavaScript) and PHP to name a few (ScaleGrid, 2021). Like all technologies, there are pros and cons associated with using PostgreSQL.

### Pros of PostgreSQL   

- **Scalability:** the PostgreSQL DBMS is capable of scaling vertically, allowing a web application's storage to easily scale as the customer base increases.   
- **Custom data type support:** PostgreSQL supports a significant number of data types by default, including document types like XML, JSON. PostgreSQL is a relational database that comes with NoSQL features. Moreover, it's possible for a user to define their own custom data types, giving a web application greater flexibility around the type of information that can be stored in the database.
- **Third-party integration:** many external tools can be integrated into PostgreSQL. For example, ClusterControl can be integrated to help manage scaling for both SQL and NoSQL databases.    
- **Open-source and community support:** being open source database makes PostgreSQL a cost-effective DBMS. It also a large community support network that provides free, fast help when required.   
(AltexSoft, 2019)  

### Cons of PostgreSQL

- **Documentation consistency:** the documentation for PostgreSQL is sometimes inconsistent or incomplete when it comes to some of its features. This makes finding a solution to some problems challenging at times.
- **Limited auditing and reporting tools:** PostgreSQL does not have an easy way to audit a database to determine its current condition. Database administrators are required to continuously check the state of the database and could possibly miss an important issue that leads to failure.     
(AltexSoft, 2019)


<hr>  

## **Question 3:**  

*Discuss the implementation of Agile project management methodology.*  

In general, the agile project management approach outlines a set of values and principles upon which specific agile project management methodologies are based. These values include placing more importance on:
- People and communication rather than processes;
- Properly functioning software over documentation;
- Customer focused behaviour rather than contractual requirements; and
- adapting to change over a strict plan. 

(Aipm.com.au, 2022)  

More specifically, the agile approach to project management is iterative and involves regular releases of the software product being developed, with customer feedback integrated into each release. The agile approach can be grouped into two broad project management methodologies, scrum and kanban (Atlassian, 2022). The most notable difference between the two approaches is that scrum uses fixed length iterations of work called sprints to address each item in a prioritised list of tasks, while kanban is focused more on getting things done as quickly as possible and bases the work iterations on team capacity (Atlassian, 2022a). Regardless of which agile method is used, implementation will follow the same general process 

**1. Project planning:** this is where the following is determined:
- The end goal,   
- The value of the product to the organisation or client
- How the product will be developed. 
- A general project scope can be developed here, but it needs to remain flexible.

**2. Product creation roadmap:** At this stage a list of features that will make up the end product is developed. This list of features will be added to a backlog or to-do list. At a later stage each feature in the backlog will be built by the team as part of each sprint.

**3. Release planning:** In contrast to the waterfall project management approach, where there is one final release date, the agile method involves product features being released at the end of shorter development cycles (aka sprints). At the release planning stage a high level feature release plan is developed; however, since agile is flexible, this plan is subject to change and the release dates are reassessed at the beginning of each sprint.  

**4. Sprint planning:** This takes place before each sprint and involves meeting to determine resource allocation, how tasks will be achieved and task load distribution. A visual outline of workflow during the sprint is required to ensure the team is able to identify and remove any potential roadblocks.  

**5. Daily stand-ups:** short (max. 15 minute) meeting are held daily throughout each sprint. They involve each team member briefly discussing what they achieved the day prior and what they intend to achieve that day. 

**6. Sprint review and retrospective:** This stage involves holding two meetings:  
-  *Sprint review* - This involves meeting with the product stakeholders to show them the finished feature. This meeting is designed to ensure constant communication with the stakeholders, to build the relationship and ensure any product issues are dealt with early.  
- *Sprint retrospective* - This involves meeting with team members to discuss what went well and what could have been done better during the sprint. It is also important to discuss if the task load was too heavy or light and to highlight what was accomplished.

(Workfront.com, 2020)

<hr>  

## **Question 4:**  

*Provide an overview and description of a standard source control workflow.*  

While there are a number of version control systems available, this question will be answered in the context of the Git and GitHub source control system. A source control workflow is an agreed process upon which the flow of code changes are applied during development. Notably, there are several common approaches to source control workflow, including centralised workflow, feature branch workflow and forking workflow (Atlassian, 2022c). The following is based on the feature branch workflow.

### Overview  
**The feature branch workflow** involves developing each feature on a dedicated branch, separate to the main branch holding the main codebase. This approach allows developers to work on a product feature, collaborate and review the new feature code before it is ultimately merged onto the main codebase. This approach can protect the main code from potential faults and facilitates continues development (Atlassian, 2022b). 

 ### Description   
 The general process below can be followed for feature development workflow.  

 Note: It's assumed a remote GitHub repository has been created and has a main branch that holds the latest code. It's also assumed that all developers in the team have full access to the remote GitHub repo.  

 A developer has been assigned a task to develop a new feature for a product under development. 
 
 1. On their local machine they ensure their copy of the main code base is up-to-date. Whilst on the main branch, they can do this using a ```git pull``` or other commands like ```git fetch origin``` and ```get reset --hard origin/main```.  
 2. Still local, create a new branch and give it the name of the feature to be developed. For example, ```git checkout -b new-menu-feature```.  
 3. Develop the feature code on the feature branch, making regular commits with the usual commands: ```git add .```, ```git commit -m "message"```. It's also important to push the feature branch to the remote repository. This allows other team members to view/review the progress of the feature branch. For example, ```git push -u origin new-menu-feature```.
 4. Other team members might review the commits. Changes are made locally in response to any feedback and then pushed back up to the remote feature branch. 
 5. When the developer has finished developing the feature they commit their recent changes locally and push back up to the remote feature branch. They then file a pull request to merge the new branch onto the main codebase. This triggers a review by other developers, including one or more senior developers to review the code before it is merged into the main branch.
 6. Once all feedback regarding the new feature has been addressed and the pull request has been accepted, the developer (on their local machine) can merge the feature branch into the main codebase. This can be done by moving to the main branch, updating the local main inline with the remote (central) version and merging the feature branch onto the main branch. For example the following commands can be used to achieve this.   
    - Move to the main branch:```git checkout main```    
    - update the local version of main inline with the central version: ``` git pull```
    - merge the local feature branch onto local main: ```git pull origin new-menu-feature```
    - pushing all updates back to the central repository: ```git push```  
(Atlassian, 2022b)

<hr>  

## **Question 5:**   

*Provide an overview and description of a standard software testing process (e.g. manual testing).*  

Manual testing involves manually checking new software against a written test plan, with the aim of determining whether the software functions as it should. Any instance of the software not performing as expected is identified as a bug and appropriate measures are taken to correct the issue. Essentially, manual testing is used to analyse software performance from the perspective of the end user (Jash Unadkat, 2021). 

### Manual testing stages  
Manual testing is typically performed in stages. The testing stages are listed below.  
1. **Unit testing:** 
Unit testing is done early during the development process and involves testing the individual components of the application as they are developed. For example, this could involve testing a new api 'get' route using postman. Unit testing is performed by someone with knowledge of the underlying code, with this type of testing known as transparent testing.

2. **Integration testing:**  
Integration testing is done after unit testing and involves testing how multiple units/components perform together as a whole. For example, a 'post' route that redirects to a 'get' route when completed could be tested to ensure both routing components perform as expected.     

3. **System testing:**  
System testing is done after integration testing and involves testing all the integrated software components as a whole. For example, an end user can be asked to input specific data like updating their name and address. They are then asked to confirm the update was successful. Notably, automated regression testing can be used at this stage to the system functions as intended. 

4. **User interface testing:**  
At this stage, the graphic user interface (GUI) is tested to ensure the visual components function as intended. The visual components that are tested can include text boxes, menu bars colours and fonts etc. Browser compatibility is also tested at this stage.     

5. **Acceptance testing:**  
Acceptance testing is done to ensure the application as a whole is fit for purpose in the real world. This type of testing involves internal testing (conducted by staff inside the development organisation) and external testing (conducted by select people outside the organisation). These types of acceptance testing are known as alpha and beta testing, respectively. Ultimately, acceptance testing is used to evaluate how well the application meets the user's requirements.  

(Jash Unadkat 2021; Shaumik Daityari 2022)


<hr>  

## **Question 6**  
*Discuss and analyse requirements related to information system security and how they relate to the project.*  

Information system security is an ever-changing and expanding field that covers network/infrastructure security and includes auditing and testing. The purpose of information system security is to protect sensitive information from illegal access, alteration or destruction. Notably, information security is a broad umbrella term, with cybersecurity considered a subset of information security. A robust information security program is built on three main concepts or principles, which include confidentiality, integrity and availability. It is considered a requirement that more than one of these principles be implemented in an information security program (Tutorialspoint.com, 2020).   

- **Confidentiality:** This feature is implemented to ensure only authorised people can access the data within a system. Basically, this involves checking each individual who tries to access the application's database is authorised to do so and is allowed to access the specific data they are attempting to view (GeeksforGeeks, 2020). 

- **Integrity:** Integrity of the data is ensured when no unauthorised individual or program alters the data. Also unauthorised alteration of data can occur intentionally or unintentionally, with unintentional alteration occurring when an authorised user accidentally removes or changes data (GeeksforGeeks, 2020).

- **Availability:** This feature relates to the timeframe in which an authorised user can access or modify data, with the timeframe set to suit the security requirements of a given organisation (GeeksforGeeks, 2020).   

In relation to this project, it is essential that user authentication is implemented as part of the development process in order to meet the confidentiality and integrity requirements. Furthermore, encrypting sensitive data held in the database is also essential. However, it is also considered best practice to implement role management and access control, with the aim of giving as little privilege as possible to limit the chances of a data breach. Multifactor authentication and timed access is also important to consider for this project, with timed access helping to meet the availability requirement mentioned above (Jones, 2018). 

It is important to consider the end user's experience and the sensitivity of the data when developing an information security program. A user needs to be able to access the relevant data without being too impeded; however, if the project data in extremely sensitive then additional measures like password expiration, account lock-outs and SSL certification should be implemented (Jones, 2018).      

<hr>  

## **Question 7**  
*Discuss common methods of protecting information and data and how you would apply them to the project.*  

Several common methods of protecting information and data for web applications are listed below.

1. **Authentication, role management and access control:** This involves giving authenticated user as little access to data as possible, provided they still get what they need from the system. This can be achieved using strong password requirements, multifactor authentication, role based authorisation, password expiration and SSL certificates to prevent sensitive account information being displayed in transit (Jones, 2018).  
In relation to the flask application for this project, authentication and access control can be implemented using the latest flask security package, which can be installed from the python package index (pip) with ```pip install Flask-Security-Too``` (PyPI, 2022). Specifically, session based authentication and role/identity based access can be implemented for the project using various package integrated within the flask security package, including flask-login and flask-principal (Readthedocs.io, 2022).     

2. **Data encryption:** Essentially, encryption is used to mask sensitive data like passwords whilst stored at rest in a database or while in transit. Encryption is the most common method of protecting sensitive data (Jones, 2018).
Sensitive data to be stored for this flask project can be encryption using another package included with the flask security package called 'passlib', which is used to hash passwords. By default, passwords are hashed using bcrypt but can be configured with more advanced hashing algorithms (Readthedocs.io, 2022).  

3. **Security configurations:** It's important to ensure sensitive information contained in the API development code is not pushed to an external server and made visible for others to see. For example, security keys and passwords need to be prevented from being pushed to an external server (Jones, 2018).  
In relation to this project, all sensitive information should be included in '.gitignore' file (assuming git/GitHub is used) to ensure API keys, secrets and passwords are not pushed to GitHub during development and the hosting provider later during production (Heddings, 2021)     

4. **Exception management:** It's important to develop generic error/exception messages when developing a web API. This is done for a number of reasons. Firstly, to ensure that the end user is told in plain English that an exception has occurred. Secondly, to not provide valuable error information for potential hackers (Jones, 2018).
In relation to the flask project, it's possible to add custom error/exception messages when developing the application. For example the ```APIException``` class from the flask_restful package can be used to raise a custom error if no data is included in a post request, thus hiding the raw error: ```TypeError: NoneType error...```(Vaati, 2020).

5. **Auditing and logging:** logs can provide a record of suspicious activity and help identify bad actor's identity (Jones, 2018).
In relation to the project, flask security makes it possible to implement login tracking, which can track the following events:
    - Last login date
    - Current login date
    - Last login IP address
    - Current login IP address
    - Total login count  
    (Readthedocs.io, 2022).


<hr>  

## **Question 8**  
*Research what your legal obligations are in relation to handling user data and how they can be met for the project.*  

Any online business in Australia that stores and collects data from customers must comply with the Australian *Privacy Act 1988*. In short, an online business must make their customers aware of what data will be stored; for example, name, address, phone number and credit card. Moreover, online businesses are legal obligated under the *Privacy Act 1988*, to inform customers of the measures that will be taken to protect their personal information. This might include using data encryption, SSL (secure socket layer) and DCI-PSS (payment card industry data security standard) (Qld.gov.au, 2022). 

Importantly, an online business may also need to comply with international privacy laws depending on the jurisdiction they intend to operate in. For example, if an online business offers goods and services in the European Union (EU), they will need to comply with EU privacy laws such as the General Data Protection Regulation (GDPR) (The Office of the Australian Information Commissioner, 2018). 

The Australian Privacy Principles (APPs) are a principles-based law that can be used to help an organisation meet its legal obligations under the *Privacy Act 1988* (The Office of the Australian Information Commissioner, 2022). Specifically, there are 13 APPs. These include: 
- APP 1: Open and transparent management of personal information.
- APP 2: Anonymity and pseudonymity.
- APP 3: Collection of solicited personal information.
- APP 4: Dealing with unsolicited personal information.
- APP 5: Notification of the collection of personal information.  
- APP 6: Use or disclosure of personal information.
- APP 7: Direct marketing.
- APP 8: Cross-border disclosure of personal information.
- APP 9: Adoption, use or disclosure of government related identifiers.  
- APP 10: Quality of personal information.  
- APP 11: Security of personal information.
- APP 12: Access to personal information.
- APP 13: Correction of personal information. 

In order to meet the relevant legal obligations listed above, the flask project could: 
- Ensure the level of protection applied to customer data whilst at rest and in transit is robust. This will help meet APP 11. Notably, this can be done using and correctly configuring the flask security package (Readthedocs.io, 2022). 
- Developing a privacy policy that informs customers about what personal information will be collected, what will be done with the information and how their information will be protected (Qld.gov.au, 2022). This could a help meet the obligations under APPs 1, 3, 5, 6, 8, 11.
- Ensuring the application allows the customer to easily access, update and de-identify their personal information if required. This will help to meet APPs 2, 10, 12. 
- Publishing the privacy policy on the application's publicly facing website (Qld.gov.au, 2022). 
- Seeking further legal advice to ensure all privacy requirements have been meet (Qld.gov.au, 2022). 







<hr>  

## **Question 9**  
*Describe the structural aspects of the relational database model. Your description should include information about the structure in which data is stored and how relations are represented in that structure.*   

In the relational database model developed by E.F. Codd in the 1970s, data is stored in the form of tables (relations). Each table represents an entity, for example, a **CUSTOMER** table. Within each table, information is represented in columns and rows, where each column (or attribute) represents a variable with a set data type and a row (or record/tuple) contains the value associated with a specific column variable. Notably, each row represents a unique record in the entity (table). In the image shown below, the CUSTOMER table has 4 columns (Customer ID, Customer name, Billing address, Shipping address). Each row in the CUSTOMER table would hold the information for individual customers (Google Cloud, 2022).  

Importantly, each table in a database has one or more columns that will hold a unique identifier called a **primary key**. Again, using the CUSTOMER table below as an example, the Customer ID column/attribute holds the primary key and is used to uniquely identify each customer. The primary key cannot be duplicated within a table. Any unique information can be used as a primary key, such as a phone number or email address; however, a database can also be configured to assign the primary key automatically. Relationships within the relational database model are represented using a foreign key, which is a column in one table referencing the primary key of another table. The image below shows the relationship between the CUSTOMER table and the ORDER table, with the ORDER table column Customer ID (foreign key) containing the related Customer ID value from the CUSTOMER table. This allows the database to establish a relationship to link each order with the relevant customer (Google Cloud, 2022).     

![Relational database](https://lh3.googleusercontent.com/_j-DAQG6tx5MwOwhdNFkHMou4fWHRuEbzYr3wEaRClkCnC3W2TR8CnMsAvmVX-rgOICpWX-wrBPc=e14-rj-sc0xffffff-h1000-w1000)
(Google Cloud, 2022)  

<hr>  

## **Question 10**  
*Describe the integrity aspects of the relational database model. Your description should include information about the types of data integrity and how they can be enforced in a relational database.*  

Data integrity refers to the accuracy, consistency and completeness of data in a relational database. Data integrity in a relational database is enforced during the design phase via the relational database management system's (DBMS's) built-in process and rules. Integrity is further enforced during database operations through error-checking and validation procedures. These procedures and rules are known as constraints (Techopedia, 2022). The specific types of data integrity and associated constraints are listed below.

### Entity integrity  
This type of data integrity pertains to the tables within the database and ensures that each row for a table is uniquely identifiable. Entity integrity is enforced through the use of primary keys. The primary key constraint indicates that the value of a primary key must be unique and cannot be null. With this constraint in place it is possible to always uniquely identify each record (Afteracademy.com, 2019).

### Domain integrity  
Domain relates to the type and range of values that can be stored in a specific table column within the database. The data types can include text, integer, date and so on. The data entered into a particular column must be in the domain of this data type. For example, if a CUSTOMER table has a column called 'date of birth' and the domain constraint for this column is set to 'date' then only valid dates can be entered into this field. If, however, a text value is entered into this field, the DBMS will return an error (Afteracademy.com, 2019).

### Referential integrity  
This type of data integrity is used to ensure data remains consistent between two tables. Referential integrity constraints relate to how foreign keys are used to ensure updates, deletions and additions in the database do not affect the data integrity. This constraint stipulates that the foreign key value in a table that refers to the primary key in another table must be present in the other table or null. The example below highlights this constraint visually (Afteracademy.com, 2019).    

![Referential integrity example](https://s3.ap-south-1.amazonaws.com/afteracademy-server-uploads/what-is-data-integrity-referential-integrity-155347826035d439.jpg)

(Afteracademy.com, 2019)

### User defined integrity  
In addition to the three types of data integrity listed above, a database developer/administrator can also implement additional data integrity constraints, if required. This is done using triggers or stored procedures. For example, a STUDENT table contains grades for different subjects as well as an overall average column. A stored procedure can be developed to automatically re-calculate the average for a given student when new grades are added to the STUDENT table (Afteracademy.com, 2019).

<hr>  

## **Question 11**  
*Describe the manipulative aspects of the relational database model. Your description should include information about the ways in which data is manipulated (added, removed, changed, and retrieved) in a relational database.*  

Interaction with data in the relational database model is performed using Structured Query Language (SQL). SQL statements can be divided into two broad categories: data definition language (DDL) and data manipulation language (DML), with the latter used to manipulate the data within the database tables (Csulb.edu, 2022). Using DML, data within a relational database is added, removed, changed and retrieved in the following ways.

### Adding data  

Adding data to a table in a relational database is done using the INSERT statement. This is used to add new rows to a table in the database. Importantly a new INSERT statement is required for every new row of data. And the comma delimited values to be added to the table must match the table structure and have the required data type for each attribute (Csulb.edu, 2022). The pattern for the INSERT statement is shown below:

```sql 
INSERT INTO <table name> VALUES (<value 1>, ... <value n>);
```
(Csulb.edu, 2022)

An example of inserting data into a fictional PRODUCTS table is shown below:

```sql
INSERT INTO products (product_no, name, price) VALUES (1, 'Cheese', 9.99);
INSERT INTO products (name, price, product_no) VALUES ('Cheese', 9.99, 1);
```
(PostgreSQL Documentation, 2022a)

### Removing data  

Data is removed from a relational database table using the DELETE statement. And a WHERE clause is used to indicate which particular row/s should be deleted. If the WHERE clause is omitted, every row of the table will be deleted (Csulb.edu, 2022). The pattern for the DELETE statement is shown below:

```sql
DELETE FROM <table name>
WHERE <condition>;
```
Using the fictional PRODUCTS table mentioned above, all rows where the price = 10 will be deleted:

```sql
DELETE FROM products WHERE price = 10;
```
(PostgreSQL Documentation, 2022c)

### Changing data  

Data in a database table can be changed using the UPDATE statement along with a SET and WHERE clause. The SET clause indicates the attribute and the new value to be updated. Similar to the DELETE statement, the WHERE clause is used to indicate the row or rows to be updated (Csulb.edu, 2022). The pattern for the UPDATE statement is shown below:  

```sql
UPDATE <table name>
SET <attribute> = <expression>
WHERE <condition>;
```
Again using the PRODUCTS table example, the UPDATE statement below is used to change all values in the price column to 10 where they are currently equal to 5:

```sql
UPDATE products SET price = 10 WHERE price = 5;
```
(PostgreSQL Documentation, 2022b)

### Retrieving data  

Data can be retrieved from a database using the SELECT statement. Generally, a SELECT statement typically uses a FROM clause, which indicates the table or tables to be used in the query. The SELECT statement can be used to view all columns of data from one or more tables, specific columns of data from one or more tables as well as specific columns and rows of data from one or more tables. A where clause can be used to filter the required rows of data based on a stated condition (PostgreSQL Documentation, 2022d). The general pattern for a SELECT statement is:

```sql
SELECT * FROM table1;
```
(PostgreSQL Documentation, 2022d).





<hr>  

## **Question 12**  

<hr>  


## References  

