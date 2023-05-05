# Project Step 1 (Proposal, Outline, ERD)
## Objective
You will work in a Project Group to create a proposal for the [CS 340 Project](https://canvas.oregonstate.edu/courses/1914742/pages/cs340-project-guide). The proposal will be, at most, 5 pages in length. This assignment forms the basis of what your Project will be and what your database will look like. After viewing the lectures this week and last, you should have an idea of what kinds of things databases are used for as well as the basic definitions of entities, relationships, attributes and various kinds of constraints.

As described in the [CS 340 Project](https://canvas.oregonstate.edu/courses/1914742/pages/cs340-project-guide) page, you should have at least 4 entity tables (4 different 'things' in your database) and at least 4 different relationships. At least one of these relationships must be a many-to-many relationship. Your proposal should explain the project and outline the 4 entities and 4 relationships in detail as described below.

This assignment also gets you started on your project right away by having you a create an ER diagram. You can use this diagram to forward engineer a database as depicted in Exploration - Creating ER Diagram MySQL Workbench. Later project steps will have you building a website in NodeJS or Flask to interact with this database.

Database design is an iterative process, and we don't expect you to get the design nailed with the first attempt. But this project assignment will give you a chance to develop your ideas and get some useful feedback from others. As you complete these project steps, expect that you will further refine your design, making it progressively better as the term goes on.

## Deliverable(s)

You should submit a **single PDF** containing (in the same order as they are presented):

### Team member names and project title
### Overview
A database is always (or at least should be!) designed to meet the requirements of the business or organization it is being built for. Imagine you are designing this system (a website with a relational database back end) for some client--briefly describe the client and what they need from the system. One well-written paragraph may be enough. Be specific (and include numbers) so the reader can understand the motivation for your design. A company that makes 200 sales per year will have a very different system from one that makes 20,000 sales per year. For example:
```text
Adventure Bikes sells $20 million in bicycles annually. A database driven website will record SalesOrders of Products to Customers.
```

### Database Outline, in Words
Using a bulleted list (see format below) describe each entity in detail, including its attributes and its relationship(s) with other entities. Explain the purpose of each entity. Provide details about each entity's attributes, including attribute data type and any constraints. For example:
- Customers: records the details of Customers we do business with
  - customerID: int, auto_increment, unique, not NULL, PK
  - email: varchar, not NULL
  - ...
  - Relationship: a 1:M relationship between Customers and Orders is implemented with customerid as a FK inside of Orders

**NOTE:** for every future project step, you will be graded based on consistency in your design. Similar to real-world database design, a documented plan for your database implementation should be . If you don't go into detail, the grader will use their best judgment, which will be final. For example, if we think a customer should be able to purchase multiple products on a sales order, and you don't clearly state this assumption in this assignment, you will likely lose points in the further steps of the project if your website does not allow multiple products on an order.

Be consistent in your naming of entities and attributes throughout your document, this helps later when you write your code. For example, if the overview describes Customers, then we expect an entity named Customers. If you use initial capitalization for entity names (or not), then we expect all entities to follow this convention. Its a good idea to make entities plural (e.g. Customers) and attributes singular (e.g. customerID). Its a good idea to distinguish when two words are combined (e.g. customerID or customer_id) but avoid using spaces in names (e.g. NOT customer id).

### Entity-Relationship Diagram:
**An ER diagram that matches your database outline.** Anything that does not match the Database outline or uses incorrect notation will cause a reduction in your points in the Final Version of this assignment.

**Note -- ER diagrams** are a **conceptual** model of databases, and often omit some details. For example, entities maybe modeled without any attributes. M:N relationships can be shown without using any intersection tables. ER diagrams may omit these details for brevity and simplicity. If you choose to make your ER diagram more detailed by adding most attributes and also showing the intersection tables in your ERD, you will not lose any points. However, we prefer that you save some of the implementation details for the schema you will create in a later Project Step.

We recommend that you use [Draw.io](https://app.diagrams.net/), or MySQL Workbench to create the ERD as shown in Exploration - Creating ER Diagram MySQL Workbench. You may draw your diagram by hand and upload a scanned copy. Regardless of how it is created, you must stick to the notation covered in the learning material.

Note that you don't need to include your schema, DDL or sample data just yet. Creating these will be part of future project steps.

## Frequently Asked Questions
### Can my Project be based on this obscure novel? Can I have some items in the store in my Project given away for free? Can vampires in my Project world be traders of garlic? Can students in this University (in my Project) be given free points without having to complete their assignments?
Yes. Anything can happen in your Project world and you are the master of that universe. The only thing we require is that you describe in detail any such quirks and deviations from general expectations. To be on the safe side, describe your world like you would to a layman.

### Can I change various things in my Database Outline in later Steps of the Project?
Yes. But, you would be required to supply the changed version of Project Outline + Database Outline.

### Can I change my Project idea completely, later?
Yes. But again, the changed version of this Step should be supplied in later steps.

### Do I also need to include a schema diagram from PhPMyAdmin designer, the Create table script out of MySQL Workbench or the MySQL backup from PhPMyAdmin export?
No. You do not need to include those in your report now. You will need them for later steps.
