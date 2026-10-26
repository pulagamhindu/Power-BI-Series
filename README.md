# Olist Operations Performance Dashboard

## Project objective

Imagine you are a Power BI analyst supporting the operations manager of an online marketplace. The management team is concerned that some orders arrive late and receive poor reviews. They also want to know which product categories and sellers contribute most to sales, and where delivery improvements would have the greatest impact.

The goal of this project is to build a business-facing report that helps answer operational and commercial questions with clear decision value.

## Business questions to answer

This analysis is designed to answer five key questions:

1. How are sales and order volumes changing over time?
2. What percentage of orders are delivered late?
3. Which product categories, sellers, or locations have the highest late-delivery rates?
4. Are late deliveries associated with lower customer review scores?
5. Which operational improvements should management investigate first?

These questions are stronger than simply asking for total sales and top-selling products because they lead to actionable operational decisions.

## Why this matters

Late deliveries create business risk in multiple ways:

- lower customer satisfaction
- poorer review scores and reputational damage
- higher refund or support costs
- reduced repeat purchase behavior
- possible loss of sales in high-volume categories or regions

The analysis therefore connects order performance, delivery reliability, product mix, and customer experience so management can prioritize actions with the largest impact.

## Data sources

The project uses the Brazilian public e-commerce dataset by Olist, stored in the `Datasets/` folder. The main files include:

- `olist_orders_dataset.csv` – order dates, status, and delivery timestamps
- `olist_order_items_dataset.csv` – item prices, quantities, shipping costs, and seller/product mapping
- `olist_products_dataset.csv` – product category and product characteristics
- `olist_sellers_dataset.csv` – seller identifiers and seller locations
- `olist_customers_dataset.csv` – customer city and state data
- `olist_order_reviews_dataset.csv` – customer review scores
- `olist_order_payments_dataset.csv` – payment information and order value
- `olist_geolocation_dataset.csv` – geographic data for location analysis
- `product_category_name_translation.csv` – translated product categories for reporting

## Key analysis areas

### 1. Sales and order volume trends

Track changes in:

- monthly sales revenue
- number of orders by month
- growth or decline in order volume over time
- seasonality or spikes tied to promotional periods

### 2. Late-delivery rate

Build a metric for:

- percentage of orders delivered late
- late delivery rate by month, region, category, and seller
- comparison between on-time and late orders in terms of revenue contribution

### 3. Operational risk by category, seller, and location

Identify the segments with the highest late-delivery rates, including:

- product categories with poor fulfillment performance
- sellers with repeated shipping delays
- cities or states with unusually high late-order rates
- combinations of region and category that require attention

### 4. Customer review impact

Analyze whether:

- late deliveries correlate with lower review scores
- certain categories or sellers experience both late deliveries and poor reviews
- customer satisfaction declines meaningfully when order delays exceed expected delivery windows

### 5. Prioritized operational improvements

Use the findings to suggest the most important actions, such as:

- improving delivery performance for the highest-volume underperforming sellers
- targeting categories with the highest late-delivery penalty
- focusing logistics investments in the worst-performing regions
- monitoring seller-level service quality before it affects review scores

## Recommended Power BI report structure

A strong report should include the following pages or sections:

1. Executive summary
   - overall sales trend
   - late-delivery share
   - review-score impact
   - top priority problem areas

2. Sales and demand trends
   - monthly revenue and order count
   - category revenue mix
   - seller contribution analysis

3. Delivery performance
   - on-time vs late rate
   - late-delivery rate by category, seller, and state
   - geographic map of delivery issues

4. Customer experience
   - review score distribution
   - late-delivery vs review-score comparison
   - category and seller review analysis

5. Actionable recommendations
   - management priorities
   - highest-impact operational fixes
   - focus areas for investigation

## Key metrics to build

Possible performance metrics include:

- Total sales
- Total orders
- Average order value
- On-time delivery rate
- Late delivery rate
- Average days to delivery
- Average review score
- Late delivery rate by category, seller, and state
- Revenue lost or affected by late delivery

## Suggested workflow

1. Import the relevant CSV files into Power BI.
2. Clean and model the data relationships.
3. Create a date table for monthly and trend analysis.
4. Build a delivery performance measure to classify orders as on time or late.
5. Merge customer, product, order, seller, and review data into a unified model.
6. Analyze late-delivery trends by category, seller, and location.
7. Correlate delivery performance with review scores.
8. Summarize the top operational improvement opportunities.

## Tools

This project is well-suited to:

- Power BI
- Excel for data validation and quick analysis
- Python or pandas for preprocessing and exploratory analysis
- Jupyter Notebook for testing logic before modeling in Power BI

## Folder structure

```text
Brazilian ecommerce public dataset by Olist/
├── Datasets/
│   ├── olist_customers_dataset.csv
│   ├── olist_geolocation_dataset.csv
│   ├── olist_order_items_dataset.csv
│   ├── olist_order_payments_dataset.csv
│   ├── olist_order_reviews_dataset.csv
│   ├── olist_orders_dataset.csv
│   ├── olist_products_dataset.csv
│   ├── olist_sellers_dataset.csv
│   └── product_category_name_translation.csv
├── README.md
└── (analysis files, Power BI outputs, notebooks, or dashboards)
```

## Expected outcome

The final deliverable should be a report that helps management understand not only how sales are performing, but also which operational issues are driving late deliveries and lower customer satisfaction. The report should allow leaders to prioritize corrective actions based on revenue impact, service risk, and customer experience.

## License

This dataset is publicly available through Olist and is intended for educational, analytical, and business reporting use. Please review the original source for any usage or attribution requirements before publishing or commercializing results.
