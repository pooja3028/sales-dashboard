# 📊 Sales Performance Dashboard (.pbix)

This Power BI dashboard gives a full view of sales, returns, and revenue trends across different zones, time periods, and customer profiles. It was created to help decision-makers explore the data and gain useful business insights.

---

## Key Features

- **Matrix View**: Sales, returns, and return rates by product sub-category
- **Map Visualization**: Regional sales activity across zones
- **Donut Charts**: Revenue breakdown by customer education, gender, and zone
- **Slicers**: Filters to view data by year, month, and zone
- **Dynamic Dashboard**: Easy to explore key metrics and patterns

---

## Data Model

The dashboard is built on a clean **star schema** structure:

- **Fact Tables**:
  - `D-Sales`: Sales data
  - `D-Returns`: Return data

- **Dimension Tables**:
  - `Product`, `Customer`, `Territory`, `Calendar`

This setup ensures correct filtering, better performance, and accurate DAX calculations.

---

## Business Logic (Key Measures)

Some of the key DAX measures used:

- **Revenue**  
  `SUMX('D-Sales', 'D-Sales'[Units] * RELATED('Product'[ProductPrice]))`

- **Return Rate**  
  `SUM('D-Returns'[ReturnQuantity]) / SUM('D-Sales'[Units])`

- **Discounted Price (10%)**  
  `ROUND('Product'[ProductPrice] * 0.9, 0)`

These help estimate actual earnings, return losses, and future pricing strategies.

---

## Dashboard Use Cases

- Identify products with high return rates
- Find top-performing sales zones
- Understand customer behavior by education level and gender
- Explore how discounts might impact revenue
- View trends over time with simple filters

---

## How to Use

- Download and open the `.pbix` file in **Power BI Desktop**
- No external data source is required — data is already embedded
- Use filters and visuals to explore insights

---

## Notes

- Company name and confidential details have been removed for privacy.
- This dashboard was created as part of a professional project. It is now shared here as a portfolio example, with permission and sensitive data hidden.

---

