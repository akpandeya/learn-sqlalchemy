# learn-sqlalchemy

<center>

![SQLAlchemy Overview Diagram](./images/sqlachemy_overview.png)  

 **Figure 1**: SQLAlchemy Overview Diagram 

 </center>

**Core** contains the breadth of SQLAlchemy’s SQL and database integration and description services, the most prominent part of this being the SQL Expression Language.

The SQL Expression Language is a toolkit all its own, independent of the ORM package, which provides a system of constructing SQL expressions represented by composable objects, which can then be “executed” against a target database within the scope of a specific transaction, returning a result set.

The ORM builds upon Core to provide a means of working with a domain object model mapped to a database schema. The persistence of business objects in a database, is automated using a pattern called unit of work.

What does this mean?

Whereas working with Core and the SQL Expression language presents a schema-centric view of the database, along with a programming paradigm that is oriented around immutability, the ORM builds on top of this a domain-centric view of the database with a programming paradigm that is more explcitly object-oriented and reliant upon mutability. Since a relational database is itself a mutable service, the difference is that Core/SQL Expression language is command oriented whereas the ORM is state oriented.