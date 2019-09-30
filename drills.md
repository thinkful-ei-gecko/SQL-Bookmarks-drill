How many canned goods products are there in the cat food care aisle

Slightly unclear wording. Checking ‘canned goods’ department returns 0 results. 

SELECT count(*)
FROM products
WHERE aisle = ‘cat food care’
AND department =  ‘canned goods’;

Checking for the term ‘Can’ in products within the cat food care aisle: 


inventory=# select product_name
inventory-# from products
inventory-# where aisle= 'cat food care'
inventory-# and product_name LIKE '%Can%';	

Returns 17 results

List all chicken products that cost less than $5

inventory=# select product_name
inventory-# from products
inventory-# where product_name LIKE '%Chicken%'
inventory-# and price < 5;

Returns 128 results. 

How many products per department in the beauty aisle? 

SELECT department, count(*)
FROM products
WHERE aisle = ‘beauty’
GROUP BY department;

Returns personal care, count of 178