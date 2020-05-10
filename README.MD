# T2A1 - Workbook - RfQ Response

## Name: Georgia Leng



> *ACME* Corporation is looking for *devs* with an understanding of *Rails*. The following set of questions relate to this RfQ-requirement. ( Word Count: 200-300 )

### Q1

------

**Question:** Describe the architecture of a typical *Rails* application ( 200-300 words )

**![q1](docs/q1.png)**

 



### Q2

------

**Question:** **Identify** a database management system (DBMS) commonly used in web applications (including *Rails*) and discuss the pros and cons of this database. ( Word Count: 150-250 )

![q2](docs/q2.png)

------

**PostgreSQL**

- PostgreSQL is one of the oldest yet the most advanced open source database management system.
- https://www.aalpha.net/blog/pros-and-cons-of-using-postgresql-for-application-development/









> ACME* Corporation is very big on project management, documentation and process. This will be a key metric in their decision to award the project. The following set of questions relate to this RfQ-requirement.

### Q3

------

**Discuss** the implementation of *Agile* project management methodology. ( Word Count: 200-300 )

![q3](docs/q3.png)

------









### Q4

------

Provide an **overview** and **description** of a standard source control workflow. ( Word Count: 100-200 )

![q4](docs/q4.png)

------





​																												

### Q5

------

Provide an **overview** and **description** of a standard software testing process (e.g. manual testing). ( Word Count: 100-200 )

![q5](docs/q5.png)

------







> Having suffered several cyber attacks in the past and resultant remedial audits *ACME* Corporation takes compliance, security and privacy very seriously. The following set of questions relate to this RfQ-requirement.

### Q6

------

**Discuss** and **analyse** requirements related to information system security and how they relate to the **project**. ( Word Count: 100-200 )

![q6](docs/q6.png)

------









### Q7

------

**Discuss** common methods of protecting information and data and how you would apply them to the **project**. ( Word Count: 100-200 )

![q7](docs/q7.png)

------











### Q8

------

**Research** what your legal obligations are in relation to handling user data and how they can be met for the **project** ( Word Count: 100-200 )

![q8](docs/q8.png)

------













> *ACME* Corporation has specifically requested the *app* to be based on a *relational* database. The next set of questions relate to this RfQ-requirement.

### Q9

------

**Question**: **Describe the structural aspects of the relational database model. Your description should include information about the structure in which data is stored and how relations are represented in that structure. ( Word Count: 100-200 )**

![q9](docs/q9.png)

------



In relational databases data is structured in a **tabular** format.  All tables (or relation) names are **unique** and within any given table the ***column*** and ***row*** fields represent ***attributes*** and the ***records*** or entries ***respectively*** - it is in this way that relations are represented. 

*All* entries in an attribute column have the same *datatype*. This is specified when the table is generated. 

Image 1.0 below shows a section of the schema file from a recipe web app that details the "recipes" table/relations attribute columns and their respective datatypes. 

For every row there will be a *single entry* for each of these attribute column fields. For example, a single string entry for attribute column "title", a single string entry for "summary", a single text entry for "method" etc, and these entries make up that unique row/tuple, which will be identifyable by its unique *primary key*.

1.0

![Screen Shot 2020-05-09 at 3.52.24 pm](docs/Screen Shot 2020-05-09 at 3.52.24 pm.png)



**Because each relation has a column attribute containing a unique primary key field other tables/relations can include this ID as well enabling the construction of a complex and accurate way to associate data.**

This unique primary key also prevents problems associated with duplicated entries, so although there may be many entries with the same title for a recipe (if we continue with the example at hand), the unique primary key establishes an identifier allowing interaction and identification with that correct and unique row. This also means that this primary key must have a *known* value, this means it can't be a "NULL" value.(1) 



1.2

![user_and_recipe_table](docs/user_and_recipe_table.png)

### **References:**

1. Mike Chappelle 'Definition of Database Relation', in 'Lifewire', (last updated: 10/01/2020), acessed 1/5/20 at: https://www.lifewire.com/relation-definition-1019260

2. Georgia Leng, Nic Megoran and Joshua Gillmore, *Recipe App* 'Eats Good', (2020), schema.rb, lines 39-49, available at:  https://github.com/NicMeg/recipe-app 
3. https://database.guide/codds-12-rules/

### Q10

------

**Question**:  ( Word Count: 100-200 )

**Rubric**: **Describe** the integrity aspects of the relational database model. Your description should include information about the types of data integrity and how they can be enforced in a relational database.



![q10](docs/q10.png)

Data integrity encompasses a set of practical principles that ensure that all data within a database is able to be connected or traced in relation to other data. Planning and implementing well engineered data integrity principles are essential to establish a database that is able to perform well in the long run, in terms of maintenance, use and interaction and expansion. 

Three core constraints make-up data integrity management:

**Domain Integrity** Domain integrity simply refers to implementing constraints that enforce all 

**Entity Integrity** - Can be established with Primary Key values in relations. As discussed in the previous section, this can not be a null value, as this would render some rows in the relation unidentifiable. The primary key attribute must be something every row or instance in the relation will have and every relation must have a primary key column if complying with primary key entity integrity principles. A common and clear example may be enrollment numbers, or a user ID - something that will be assigned on every instance and be a unique single entry in this primary key field; *this* way the presence of other null values for other attributes are less problematic and the row as a whole remains uniquely identifiable and tracable through its primary key. 

**Referential Integrity**  Referential Integrity requires any foreign keys in a relation have a valid corresponding unique primary key *or* a null value. When the database creator generates the relations the referential integrity constraints are specified by the creator. An example may be that a recipe table may have a foreign key of user ID from the user relation, this user ID must be the user relations valid primary key and must of course share the same datatype as the foreign key. This relationship would be described as parental, user relation is parent of recipe relation.  Adherance to referential integrity principles enforces the rule of relational databases whereby all data is traceable through relation. Referential integrity also relates to entity integrity in that it requires adherence to that prinicple in order to work as part of an integrated system.

A well structured approach to data-integrity that comprehensively encorporates all of these constraints sets a database in good stead moving forward.



References:

1) Adrienne Watt & Nelson Eng, *Database Design - 2nd Edition*, (2014), Victoria, B.C.:BCcampus, retrieved from https://opentextbc.ca/dbdesign01/ , Chapter 9 - Integrity Rules and Constraints.

1) https://www.guru99.com/relational-data-model-dbms.html

https://database.guide/codds-12-rules/

### Q11

------

**Question**: **Describe** the manipulative aspects of the relational database model. Your description should include information about the ways in which data is manipulated (added, removed, changed, and retrieved) in a relational database. ( Word Count: 100-200 )

![q11](docs/q11.png)



![Screen Shot 2020-05-09 at 3.55.03 pm](docs/Screen Shot 2020-05-09 at 3.55.03 pm.png)

> The efficiency of an *app* (i.e. site) and the algorithms used are of the utmost importance. The next set of questions relate to this RfQ-requirement.

### ![q12_q13](docs/q12_q13.png)Q12

------

**Question**: **Identify** and **explain** the workings of TWO **sorting** algorithms and **discuss** and **compare** their performance/efficiency (i.e. Big O) ( Word Count: 300-500 )



# Q13

**Question**: **Identify** and **explain** the workings of TWO **search** algorithms and **discuss** and **compare** their performance/efficiency (i.e. Big O) ( Word Count: 300-500 )











> Companies (including *ACME* Corporation) value previous project experience and case studies. The following set of questions relate to this RfQ-requirement.

## Q14

**Question**: ( 50-100 per part )

Conduct **research** into a marketplace website (*app*) and answer the following parts: 



### a. List and describe the software used by the \*app\*.

![q14_a](docs/q14_a.png)

------



![Airbnb_April_2020](docs/Airbnb_April_2020.jpg)Airbnb co-founder and CTO Nathan Blecharczyk started Airbnb as a Ruby on Rails application in July 2009

![first-commit-airbnb](docs/first-commit-airbnb.png)

Reference Video: [From Monorail to Monorepo: Airbnb's journey into microservices - GitHub Universe 2018](https://youtu.be/47VOcGGm6aU?t=143)

Since then Airbnb's marketplace application has increased in complexity and its monolithic Rails application (known internally as "Monorail") has been gradually migrated to a distributed microservice architecture.

The transition to a service-oriented architecture (SOA) was meant to solved the deployment, scalability and performance issues that came with the Rails monolith. [Reference](https://rubygarage.org/blog/advantages-of-microservices).



##### Core Platform Features & Associated Software: 

- Ruby on Rails

- Frontend - built with [React](https://reactjs.org/) 

- Listing Search Engine - [Machine Learning System](https://arxiv.org/pdf/1810.09591.pdf)

- Global payments - [Braintree](https://www.braintreepayments.com/au)

- Price Optimisation System 

- Communication & Messaging [via Twillio API](https://www.twilio.com/)

- Image Classifier - [Tensorflow](https://medium.com/airbnb-engineering/categorizing-listing-photos-at-airbnb-f9483f3ab7e3)

  

- Search Function 

- ID and verification

- Review System 

- Payment System

- Availability 

- Messaging System - Notifications, reminders, sms

- Communication System - for host & guests

- Support System

  

- User

  - Host
  - Guest

- Destinations

- Listing

- Bookings

- Favourites

- Reservation 

  

  

### Airbnb Tech Stack 

#### Applications and Data

- Nginx ( HTTP server and mail proxy server )
- JavaScript
- Java
- React
- MySQL
- Amazon EC2
- Amazon S3
- Node.js - [Reference](https://medium.com/airbnb-engineering/operationalizing-node-js-for-server-side-rendering-c5ba718acfc9)
  - Hypernova - deprecated
  - Hyperloop - Server side rendering
- Redis
- Ruby
- Sass
- Rails
- [Kotlin](https://medium.com/airbnb-engineering/better-android-testing-at-airbnb-eacec3a8a72f) 
- Amazon RDS
- Hadoop
- Amazon Elasticache
- Amazon EBS
- Airflow
- Presto
- Druid
- Native Navigation
- [Airpal](http://airbnb.io/airpal/) - web-based query execution tool
- [Envoy](https://www.envoyproxy.io/) - Edge and service proxy

#### Utilities

- Amazon CloudFront
- Twilio SendGrid
- Amazon Route 53
- Twilio
- Visual Website Optimizer
- Braintree (Used for global payments)
- Lottie
- Nexmo
- Urban Airship
- Aerosolve
- DeepLinkDispatch
- Akamai (CDN)

#### DevOps

- GitHub
- New Relic
- Webpack
- Sentry
- Vagrant
- Kibana
- Amazon CloudWatch
- Logstash
- Datadog
- Jest
- Chef
- Enzyme
- Apache Mesos
- SmartStack
- [Buildkite](https://buildkite.com/) - continuous integration testing pipelines

#### Business Tools

- Slack
- G Suite
- InVision
- Asana
- Superset
- React 
- Sketch.app
- Assemblage

#### Analytics

- Google Analytics
- Campaign Monitor



> **References :**
>
> - https://mixpanel.com/topics/tech-stack-examples/
> - https://stackshare.io/airbnb/airbnb
> - https://airbnb.io/
> - https://builtwith.com/?https%3a%2f%2fwww.airbnb.com.au%2f
> - https://stackshare.io/airbnb/airbnb
> - https://yalantis.com/blog/the_technology_stack_behind_airbnb/
> - https://medium.com/airbnb-engineering
> - [Airbnb: Utilizing Machine Learning to Optimize Travel](https://digital.hbs.edu/platform-rctom/submission/airbnb-utilizing-machine-learning-to-optimize-travel/)
> - https://mixpanel.com/topics/tech-stack-examples/





## b. Describe the hardware used to host the \*app\*. 

![q14_b](docs/q14_b.png)



Airbnb platform architecture relies heavily on Amazon Web Services (AWS) for nearly all of its cloud computing functions. Airbnb's rapid growth meant it had to focus on reliability and scalability. AWS infrastructure allowed Airbnb to automatically scale up to meet their growing user base and focus on product development instead of physical infrasture and hosting administration. I have outlined below the key services utilised by Airbnb and provided brief explanations of each services function.



- Application cloud hosting, memcache and search servers
  - Amazon Elastic Compute Cloud (EC2) - direct increases and manage spikes
    - manage core Airbnb application
  - [Amazon ElastiCache for Redis](https://aws.amazon.com/elasticache/redis/) - for cache infrastructure and for the main database
  - [Elastic Load Balancing](https://aws.amazon.com/elasticloadbalancing/)
  - [Amazon Elastic MapReduce](https://aws.amazon.com/emr/) -  tool for big data processing and analysis
- Cloud storage for user data, backups and static files
  - Amazon Simple Storage Service (S3)
  - [Amazon Elastic Block Store (EBS)](https://aws.amazon.com/ebs/)
- Cloud-based MySQL relational database to store data
  - Amazon Relational Database Service (RDS)
- Application and Infrastructure Monitoring
  - Amazon CloudWatch 
- Content Delivery Network (CDN) for rapid delivery
  - [Amazon CloudFront](https://aws.amazon.com/cloudfront/)
- Big data tools by Airpal, Presto, and Druid — to store, process, analyze, and manage huge amounts of data.



> **References :** 
>
> - https://www.contino.io/insights/whos-using-aws
> - https://aws.amazon.com/solutions/case-studies/airbnb-case-study/
> - https://aws.amazon.com/solutions/case-studies/airbnb/
> - https://enqueuezero.com/airbnb-architecture.html
> - https://www.softwareadvisoryservice.com/en/blog/case-study-airbnb-and-the-power-of-amazon-web-services/
> - https://yalantis.com/blog/the_technology_stack_behind_airbnb/
> - https://airbnb.io/
> - https://stackshare.io/airbnb/airbnb





#### c. Describe the interaction of technologies within the \*app\*

![q14_c](docs/q14_c.png)



Frontend:

- ReactJs

Backend:

- Ruby on Rails - Core 



For the back-end Airbnb relies on Rails, making developing new features and scaling a breeze. To complement the framework they use Apache Thrift to bind C code with Ruby. Airbnb has plenty of dynamic data so it relies on ReactJS to control It's front-end and give it flexibility and efficiency. It also uses HTML5, CSS, jQuery, and elements of Node JS.

Airbnb uses an Nginx webserver to handle traffic demands with a proxy server to lighten the load. It also offers security and scalability. It uses Redis for caching to increase response times.

For storage, AirBNB originally used MySQL but changed to cloud storage once demands increased. They use Amazon RDS as a cloud database, EC2 for hosting and S3 and EBS for cloud storage.  

For the large amounts of user data, Airbnb uses Presto, Druid, and Airpal to handle the analytics and processing. 







#### d. Describe the way data is structured within the \*app\*

![q14_d](docs/q14_d.png)







#### e. Identify entities which must be tracked by the \*app\*

![q14_e](docs/q14_e.png)

Use





#### f. Identify the relationships and associations between the entities you have identified in part (e)

![q14_f](docs/q14_f.png)

Users:

- has many Bookings 
- has many Wishlists 
- has many Accommodations 

Accommodations:

- has many Bookings
- has many Users through Bookings
- has one Country
- has one Currency 
- has one City
- has one Property type
- has one Room Type 
- has one State 

 Bookings:

- has one User 
- has one Wishlist 
- has one Transaction

 Wishlist: 

 - has one User 
 - has many Accommodations 

 Transactions:

 - has one Currency 
 - has one Booking 
 - has one Accommodation 

 Reviews 

- has one User
- has many Accommodations  
- has many Bookings 

 Countries: 

 - has many Accommodations  

 Cities: 

 - has many Accommodations  

 States: 

 - has many Accommodations  

 Currencies: 

 - has many Transactions 

 Property types: 

 - has many Accommodations  

 Room types: 

 - has many Accommodations 





#### g. Design a schema using an Entity Relationship Diagram (ERD) appropriate for the database of this website (assuming a relational database model)

![q14_g](docs/q14_g.png)
