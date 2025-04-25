# Ecommerce-assignment
ecommerce database assignment
The schema is collection of tables showing various relationship
Project Overview: A concise description of the e-commerce schema’s purpose (e.g., product catalog, inventory, pricing, attributes).

Prerequisites:

Supported MySQL version (e.g., MySQL 8.0+)

Required user privileges (CREATE, ALTER, DROP on schema)

Installation / Import Instructions:

mysql -u <username> -p < ecommerce.sql

Schema Structure:

Tables: List all 12 tables with a one-line description for each (e.g., brand: stores manufacturer info).

ER Diagram: Reference the file ecommerce_erd.png for a visual overview of entities and relationships.

Relationships Overview: Briefly describe key foreign-key relationships (e.g., products to categories, variations to products).

Sample Queries:

Retrieve all products with their category and brand:

SELECT p.name, c.name AS category, b.name AS brand
FROM product p
JOIN product_category c ON p.category_id = c.category_id
JOIN brand b ON p.brand_id = b.brand_id;

Show available stock for each variation SKU:

SELECT pi.sku, pi.stock_quantity
FROM product_item pi;

Authors / Contributors: List team members and their roles John Gadiru I did all the work alone.

