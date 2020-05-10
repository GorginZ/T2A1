README document

Project documentation is to be compiled as a single markdown file named README.md. This file should contain,
No. 	Requirement
R1 	Answers to all the Questions below.
R2 	Your README.md should have headings for each question and answers organised under the appropriate headings.
R3 	Provide full attribution to referenced sources (where applicable).
Questions

    ACME Corporation is looking for devs with an understanding of Rails. The following set of questions relate to this RfQ-requirement.

# No. 	Question 	Word Count

Q1 	Describe the architecture of a typical Rails application 	200-300

ORM. Object-relational- mapping active record takes data which is tored in a database. useing rows and columns. thse need to be modified or retrieved by SQL queery, we are able to interact as if it were a normal ruby object. so long as there's config in database.yml it doesn't matter what kind of database is being used, active record means you can still access this information in this way.

Models. In relation to the database.
The model inherets from active record and inherets the methods from active record - eg all , find and create. one table corresponds with one model which ineherets from active record. (from odin)



active record is a way to access information in the database without having to write a queery in SQL. can say User.all instead of qruiting a query. 

https://www.theodinproject.com/courses/ruby-on-rails/lessons/active-record-queries


Q2 	Identify a database management system (DBMS) commonly used in web applications (including Rails) and discuss the pros and cons of this database 	150-250





    ACME Corporation is very big on project management, documentation and process. This will be a key metric in their decision to award the project. The following set of questions relate to this RfQ-requirement.

No. 	Question 	Word Count
Q3 	Discuss the implementation of Agile project management methodology 	200-300
Q4 	Provide an overview and description of a standard source control workflow 	100-200
Q5 	Provide an overview and description of a standard software testing process (e.g. manual testing) 	100-200

    Having suffered several cyber attacks in the past and resultant remedial audits ACME Corporation takes compliance, security and privacy very seriously. The following set of questions relate to this RfQ-requirement.

No. 	Question 	Word Count
Q6 	Discuss and analyse requirements related to information system security and how they relate to the project 	100-200
Q7 	Discuss common methods of protecting information and data and how you would apply them to the project 	100-200
Q8 	Research what your legal obligations are in relation to handling user data and how they can be met for the project 	100-200

    ACME Corporation has specifically requested the app to be based on a relational database. The next set of questions relate to this RfQ-requirement.

No. 	Question 	Word Count
Q9 	Describe the structural aspects of the relational database model. Your description should include information about the structure in which data is stored and how relations are represented in that structure. 	100-200

DESCRIBE STRCTURE

RELATIONS REPRESENTED IN T STRCUTRUE
foriegn keys and associations - 

relational databases are structured with rows and columns. this is a tabular way to represent relational data. 

relational databases are more dynamic than two dimensional databases, they can allow for more complex interaction and reflect  and create more complex relationships.

They prevent duplicate and formatting issues by pre-defining valid inputs. how does this work? associations and foreign keys. for instance specifying datatypes.


rows and columns, tabular way to represent relational data. duplicate/ format issues (?) if these are issues good to move toa relational model. defines a set of relations that are analogous to tables, they relfect the relationships between the data stored and how they inetract. relation databases are more dynamic - in contrast to a two dimensional tabel, a relationdatabase can handle more complex relationships. example. some examples of relational databases are - Sqlite, MS SQL, postgreSql and Mysql are relational datbases. some are more lightweight some more heavyweight. all relational databses use SQL as the language to interact with and manipulate the data on the datbase. 



https://launchschool.com/books/sql/read/introduction


Q10 	Describe the integrity aspects of the relational database model. Your description should include information about the types of data integrity and how they can be enforced in a relational database. 	100-200


Q11 	Describe the manipulative aspects of the relational database model. Your description should include information about the ways in which data is manipulated (added, removed, changed, and retrieved) in a relational database. 	100-200

SQL! simple english commands allow us to Select(find) Insert (add) update (change) and delete (remove) data in databases in very simple oftenone line of code. 
sql is a declaritive language - tells what to do not how to do it, so how the query is executed is not specified in our sql command.



    The efficiency of an app (i.e. site) and the algorithms used are of the utmost importance. The next set of questions relate to this RfQ-requirement.

No. 	Question 	Word Count
Q12 	Identify and explain the workings of TWO sorting algorithms and discuss and compare their performance/efficiency (i.e. Big O) 	300-500
Q13 	Identify and explain the workings of TWO search algorithms and discuss and compare their performance/efficiency (i.e. Big O) 	300-500

    Companies (including ACME Corporation) value previous project experience and case studies. The following set of questions relate to this RfQ-requirement.

No. 	Question 	Word Count
Q14 	Conduct research into a marketplace website (app) and answer the following parts:  a. List and describe the software used by the app.
  b. Describe the hardware used to host the app.
  c. Describe the interaction of technologies within the app
  d. Describe the way data is structured within the app
  e. Identify entities which must be tracked by the app
  f. Identify the relationships and associations between the entities you have identified in part (e)
  g. Design a schema using an Entity Relationship Diagram (ERD) appropriate for the database of this website (assuming a relational database model) 	50-100 per part