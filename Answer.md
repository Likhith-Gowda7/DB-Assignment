1) Explain the relationship between the "Product" and "Product_Category" entities from the above diagram.

Product Entity: This entity represents individual products with fields id, name, desc, SKU, category_id, inventory_id ,price, discount_id, created_at, modified_at, deleted_at
Product_Category Entity: This entity represents categories of products with fields id, name, desc, created_at, modified_at, deleted_at
The relationship between these entities is established through the category_id field in the Product table. Specifically, each product is associated with one category by referencing the id field of the corresponding category in the Product_Category table.
This means that for each product, there is a single category it belongs to, but a category may have multiple products associated with it. 

2) How could you ensure that each product in the "Product" table has a valid category assigned to it?

To ensure that each product in the "Product" table has a valid category assigned to it, you can utilize a foreign key constraint. The foreign key constraint is a key used to link two tables together. A foreign key is a field in one table that refers to the PRIMARY KEY in another table.
The Product_Category table is created with the specified fields.
The Product table is created with a category_id column that serves as a foreign key referencing the id column of the Product_Category table.
The FOREIGN KEY constraint ensures that every value in the category_id column of the "Product" table must exist in the id column of the Product_Category table.
