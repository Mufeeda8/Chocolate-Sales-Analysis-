# 🍫 Chocolate Sales Analysis

This Tableau project presents a detailed analysis of chocolate sales performance.  
It includes *Three dashboards* that explore sales overview, monthly sales trends, and profit insights across regions and product categories.

---

## 📊 Dashboards Included

### 1 Sales Overview Dashboard
- Displays total sales, Unit price, and number of boxes shipped  
- Highlights sales distribution across countries and categories  
- Identifies top-performing regions  

---

### 2 Profit Analysis Dashboard
- Shows profit margins across product categories and countries  
- Compares sales vs. profit performance  
- Highlights top and least profitable areas  

---

### 3 Monthly Sales Dashboard
- Shows monthly sales and quantity trends   
- Highlights seasonal sales patterns  

---

## 💲 Data Preparation Notes
- The dataset originally included a field named *“Amount.”*  
- This field was *converted from a Dimension (categorical field) to a Measure (numerical field)* in Tableau.  
- It was then *formatted as Currency (Dollar $)* and renamed to *“Sales”* for better readability and accurate aggregation in dashboards.  

---

## 🧮 Calculated Fields Used

Several calculated fields were created to support analysis and visualization:

| *Calculated Field* | *Purpose / Formula (Simplified)* |
|-----------------------|------------------------------------|
| *Profit(USD)* | [Sales (USD)]-[Cost_per_Box]*[Boxes Shipped]
| *Profit_Margin(USD)* | SUM([Profit(USD)]) / SUM([Sales (USD)]) * 100 → to find % profit margin |
| *Unit_Price(USD)* | SUM([Sales (USD)]) / SUM([Boxes Shipped]) → to calculate price per box |
| *Profit marginlevel* | IF [Profit_Margin(USD)] <=0 THEN "Loss",ELSEIF  [Profit_Margin(USD)]<=10 THEN "Low",ELSEIF  [Profit_Margin(USD)]<=20 THEN "Moderate",ELSE"Profitable",END |

These fields helped in identifying key trends and profitability patterns.

---

## 📊 Profit Margin & Pricing Analysis

###  Key Insights
- The number of boxes shipped varies across different product categories.  
- Profitability differs by category due to variations in unit prices.  
- Maintaining an average unit price that is neither too high nor too low supports balanced profit margins and stable sales performance.  
- When unit prices are low, reducing the number of boxes shipped helps minimize losses.  
- When unit prices are high, the number of boxes shipped decreases due to lower customer demand, which negatively impacts sales performance.  
- *Profit Margin Classification:*  
  - Below 0% → Loss  
  - 0–10% → Low profit  
  - 10–20% → Moderate profit  
  - Above 20% → High profit  
- A balanced pricing and shipment strategy ensures consistent profitability across all categories and regions.

---
