# Maven Toys Sales Dashboard (Power BI)

A Power BI report built on the **Maven Toys** dataset to analyze sales performance and track key KPIs (Orders, Revenue, Profit) across time, product categories, and store locations.

---

## 📦 Dataset
The report is built from four CSV tables:
- **sales** (fact table)
- **products** (dimension)
- **stores** (dimension)
- **calendar** (dimension)

### Data validation & exploration
Before modeling, I:
- Reviewed columns and checked for **blank/null values**
- Confirmed **data types** were correctly defined
- Identified **primary/foreign keys**
- Performed quick exploratory checks:
  - Number of **transactions**
  - Number of **stores**
  - **Lowest and highest** product prices

---

## 🧱 Data Modeling (Star Schema)
Tables were loaded into the model and connected in a **star schema**:
- **1:Many** relationships from **sales → products / stores / calendar**
- Followed data modeling best practices (fact at the center, dimensions around it)
- **Hidden foreign keys** in the `sales` table from the report view for a cleaner field list

---

## 🗓️ Calendar Enhancements
Added calculated columns in the **calendar** table:
- **Start of Month**
- **Start of Week**

Created a **date hierarchy** using:
- `Start of Month` → `Start of Week` → `Date`

---

## 💰 Calculations
### Calculated columns (sales)
- Pulled **Cost** and **Price** from `products` into `sales`
- Calculated:
  - **Revenue** per transaction
  - **Profit** per transaction

### Measures
Created measures for:
- **Total Orders** (count of orders)
- **Total Revenue** (sum of revenue)
- **Total Profit** (sum of profit)

✅ **Bonus:** Built Revenue/Profit measures without referencing calculated columns (measure-driven approach).

---

## 📊 Report Visuals & Features
The final report includes:
- **KPI cards** for the **current month**:
  - Total Orders, Total Revenue, Total Profit  
  - with **monthly trends** for each KPI
- **Slicer** to filter by **store location**
- **Bar chart:** Total Orders by **product category**
- **Line chart:** Total Revenue over time using the **date hierarchy**
- Polished layout with improved formatting, alignment, and readability





## 👩‍💻 Author
**Sophie Ranj**  
📫 Email: ranj.sophie@outlook.com  
🔗 LinkedIn: <a href="https://linkedin.com/in/sophie-ranj" target="_blank" rel="noopener noreferrer">linkedin.com/in/sophie-ranj</a>  
🌐 Portfolio: <a href="https://sophie-ranj.github.io/" target="_blank" rel="noopener noreferrer">https://sophie-ranj.github.io/</a>
