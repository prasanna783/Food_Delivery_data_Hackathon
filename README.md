# Food Delivery Data Integration Pipeline

Project Overview
This project demonstrates a complete data integration pipeline for a food delivery platform.  
Data is ingested from **multiple real-world formats (CSV, JSON, SQL/Python script)**, cleaned, and merged into a **single source of truth** dataset for downstream analytics.

This notebook was created as part of a hackathon challenge focused on data engineering and data preparation skills.

---

## Data Sources
The project uses three different datasets simulating real-world systems:

1. **orders.csv**  
   - Transactional data containing order-level details  
   - Includes `order_id`, `user_id`, `restaurant_id`, order amount, date, etc.

2. **users.json**  
   - User master data  
   - Contains user demographics, city, and membership type (Gold / Regular)

3. **restaurants.sql** 
   - Python-based database setup script  
   - Creates a SQLite database (`restaurants.db`)  
   - Contains restaurant master data such as cuisine and ratings

---

## Tools & Technologies
- **Python 3**
- **Pandas** – data loading, merging, and transformation
- **SQLite3** – handling relational restaurant data
- **VS Code**
- **GitHub** – version control and submission

---

## Data Processing Steps
1. Loaded transactional data from CSV using Pandas  
2. Loaded user master data from JSON  
3. Executed a Python-based SQL setup script to create and populate a SQLite database  
4. Loaded restaurant data from SQLite into Pandas  
5. Performed **LEFT JOINS**:
   - `orders.user_id → users.user_id`
   - `orders.restaurant_id → restaurants.restaurant_id`
6. Created a final consolidated dataset containing:
   - Order details  
   - User information  
   - Restaurant information  

---

## Final Output
- **final_food_delivery_dataset.csv**

This dataset serves as the **single source of truth** for:
- Order trend analysis
- User behavior analysis
- City-wise and cuisine-wise performance
- Membership impact (Gold vs Regular)
- Revenue distribution and seasonality

---

## How to Run the Project
1. Clone or download this repository
2. Open `Food_Delivery_Data_Integration.ipynb` in Jupyter Notebook or VS Code
3. Ensure all data files are in the same folder
4. Run **Kernel → Restart & Run All**
5. The final dataset will be generated automatically

---

## Conclusion
This project showcases a realistic data integration workflow involving multiple data formats and relational joins.  
It mirrors real-world data engineering tasks and prepares clean, analysis-ready data for business insights.

---

## Author
**K.Laxmi Prasanna**  
Hackathon Participant
