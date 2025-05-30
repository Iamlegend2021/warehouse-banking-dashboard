# warehouse-banking-dashboard
Tableau dashboard showing sales, inventory risk, and product trends for a simulated warehouse + fintech business
https://public.tableau.com/views/Book1_17483034695830/TopProducts?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link

--Products sold in the last 60 days, ordered by quantity sold.
SELECT p.product_id,
    p.product_name,
        SUM(o.quantity) as total_quantity_sold,
MAX(o.order_date) as last_sold_date
    FROM products p  
LEFT JOIN orders o ON 
p.product_id  = o.product_id
GROUP BY o.product_id;  

# Warehouse + Banking Hybrid Dashboard (Tableau)

This Tableau project simulates a business like Amazon + Chime. It includes:

- Top-selling products in last 60 days
- Overstock risk analysis (low sales, high inventory)
- Sales trend over time
- Sales by category

Built with SQL + Tableau, using real-world business questions to showcase analytical and dashboard skills.
