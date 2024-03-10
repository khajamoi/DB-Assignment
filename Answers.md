1. Relationship between "Product" and "Product_Category" entities:
The relationship between the "Product" and "Product_Category" entities is a foreign key relationship. Specifically, the "Product" table has a column named "category_id," which is a foreign key referencing the "id" column in the "Product_Category" table. This means that each product in the "Product" table is associated with a category from the "Product_Category" table.

1.1   Each product in the "Product" table belongs to exactly one category.
1.2  Each category in the "Product_Category" table may have multiple products associated with it.

2. To ensure that each product in the "Product" table has a valid category assigned to it, you can set up a foreign key constraint on the "category_id" column in the "Product" table. This constraint will enforce referential integrity, ensuring that every value in the "category_id" column of the "Product" table corresponds to a valid "id" in the "Product_Category" table.
    an example of how you could set up the foreign key constraint in SQL
                ALTER TABLE product
                ADD CONSTRAINT fk_product_category
                FOREIGN KEY (category_id)
                REFERENCES product_category(id);
This constraint ensures that each value in the "category_id" column of the "Product" table must exist in the "id" column of the "Product_Category" table.               


