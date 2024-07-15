## 1. What is the total amount each customer spent at the restaurant?

```
SELECT sales.customer_id, SUM(menu.price)
FROM dannys_diner.sales sales
  INNER JOIN dannys_diner.menu menu
  ON sales.product_id = menu.product_id
GROUP BY sales.customer_id
ORDER BY sales.customer_id;
```

## 2. How many days has each customer visited the restaurant?

```
SELECT customer_id, COUNT(DISTINCT order_date)
FROM dannys_diner.sales
GROUP BY customer_id
ORDER BY customer_id;
```