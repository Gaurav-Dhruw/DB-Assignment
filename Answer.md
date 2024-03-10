1) The given "product" to "product_category" relation is many-to-one. It means that a "product" item can have only a single "product_category" item associated with it while a "product_category" item can have zero or multiple "product" items associated with it.

2) By adding a foreign key constraint on the "category_id" field of the "product" table. This constraint will ensure only a valid "product_category" item will be assigned to the "product" items. SQL snippet for the same is provided below:

    ```
   category_id INT,
   CONSTRAINT FOREIGN_KEY(category_id) REFERENCES product_category(id)
   ```
   
4) I have used Prisma (ORM) for creating the given schema, it is present in the "schema.prisma" file in the root directory.
