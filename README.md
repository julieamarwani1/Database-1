# Database-1
Project in Database Design I (1DL301) Fall 2020, Period 2

The project gives you the opportunity to practice a relational database design process from A to Z, from reading the customer specification, which might be redundant, vague or even inconsistent; to conceptual modeling using ER diagrams; to creating, populating and querying the database in an RDBMS; to writing applications accessing
and modifying the stored data.

Your group has been asked to help with a project for AltOnline AB, a new Swedish company which, inspired by the tremendous success of Amazon.com, Inc., wants to become a market leader in online sales in Sweden.The project is rather large and your part is to design and implement a database system for its online store. 

# Customer specification and requirements
   # Structure of the store departments
   
AltOnline is planning to sell a huge variety of products. To make the navigation as easy and user-friendly as possible, AltOnline wishes to have a hierarchical structure (i.e., a tree) of departments. The following is an example of such a structure:

Electronics
Electronics / Computers and tablets
Electronics / Computers and tablets / Desktops (leaf1)
Electronics / Computers and tablets / Laptops (leaf)
Electronics / Computers and tablets / Tablets (leaf)
Electronics / Computers and tablets / Accessories
Electronics / Computers and tablets / Accessories / For desktops (leaf)
Electronics / Computers and tablets / Accessories / For laptops (leaf)
Electronics / Computers and tablets / Accessories / For tablets (leaf)
Electronics / TV and video
Electronics / TV and video / TVs (leaf)
Electronics / TV and video / Projectors (leaf)
etc.
Each product in the store will belong to exactly one leaf department.The managers at AltOnline have specified how the pages are going to look like (rather than what they want to store in the database).

# Department page
A department page will show:
 Logo of the store
 Breadcrumbs (the path to the department, e.g., Home / Electronics / Computer and tablets)
 Title of the department
 Description of the department

If the department is not a leaf, we want to show a list of all child departments, including the following for each of them:

 Title of the child department
 Short description
 Link to the child department’s page

    If the department is a leaf, we want to show a list of its products, including the following for each product:
       Title of the product
       Short description
       Current retail price (with the value added tax)
       Add to basket button (disabled if the product is out of stock)
       Link to the product page
# Product page
A product page will show:
 Logo of the store
 Breadcrumbs
 Title of the product
 Description
 Retail price without and with the value added tax
 Value added tax in percents
 Stock quantity (how many items are in stock)
 Add to basket button (disabled if the product is out of stock)
 A list of all keyword-related products (products that share at least one of the keywords) showing the
following for each of them:
– Title
– Short description
– Current retail price
– Link to the product page
 User reviews (see below)
 Average rating of the product (see below)
The product might be on sale; in that case we want to show also the price before the discount and the discount
as a percentage. The discount is always registered in percents by store managers.
