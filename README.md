# Library Operations & Analytics: Data Warehouse Design (OLAP)

## Project Overview
This project involves the end-to-end design and implementation of a Data Warehouse for a Library Management System. By transforming a highly normalized Transactional Database (OLTP) into an analytical Star Schema (OLAP), I enabled high-speed querying and trend analysis to solve real-world operational challenges.

## Tech Stack & Skills
- **Data Engineering:** Star Schema Modeling, ETL Process Design, Denormalization.
- **Database Logic:** Fact & Dimension Table Partitioning, Surrogate Key Implementation.
- **Tools:** SQL, Power BI (Visual Analysis), Logical & Physical Modeling.

## Data Architecture: From OLTP to Star Schema
The core of this project was migrating from a complex 3rd Normal Form (3NF) database to a streamlined **Star Schema** to optimize performance for high-volume analytical workloads.

### **1. Central Fact Table**
* **`fact_library_transactions`**: The central repository for all measurable events.
    * **Grain:** Individual transactions (Borrowing, Returning, and Facility Bookings).
    * **Measures:** Total transactions, fine amounts, overdue duration, and occupancy rates.
    * **Connectivity:** Integrated via surrogate keys to ensure join efficiency and historical tracking.

### **2. Dimensional Modeling**
Developed seven dimensions to provide deep business context for library operations:
1. **`dim_member`**: Tracks demographics, membership tiers, and validity status.
2. **`dim_book`**: Consolidates book titles and languages into a single flattened table.
3. **`dim_author`**: Profiles author popularity and catalog frequency.
4. **`dim_publisher`**: Monitors procurement trends and publisher-specific engagement.
5. **`dim_facility`**: Maps study rooms and labs for floor-wise spatial utilization analysis.
6. **`dim_staff`**: Captures staff-on-duty data to analyze workload distribution.
7. **`dim_date`**: Supports time-series hierarchies (Year > Month > Week > Day).

---

## 📈 Strategic Performance Analysis (2022–2024)
**Focus:** Festive Event & Operational Stress-Point Evaluation
Through the implementation of the analytical layer, Critical performance phases that define the library’s operational lifecycle:
### **1. The "March Stress Point" (Festive & Academic Peak)**
The data reveals a massive surge in March, with 2022 recording over **12,000 daily transactions**. 
* **Analysis:** This peak correlates with festive events and high academic demand. However, a comparative analysis shows 2024 struggled to reach these historical levels.
* **Strategic Insight:** This gap indicates "Operational Compression," where current staffing or system limitations may be preventing the library from hitting maximum capacity.

### **2. The "July-August Valley" (Maintenance Window)**
Across the three-year study, July and August consistently show the lowest performance metrics.
* **Strategic Insight:** This represents the **Optimal Maintenance Window**. Major system upgrades, data warehouse maintenance, and staff training should be strategically scheduled during this period to minimize user disruption.

### **3. Baseline Performance Erosion**
A year-on-year comparison shows a downward trend in baseline daily loads from 2022 to 2024.
* **Strategic Insight:** The library is experiencing a shift in user behavior. I recommend transitioning to a proactive "Digital Engagement" model during off-peak months to restore baseline activity levels.

---

## Strategic Recommendations for Management
| Event Period | Observation | Strategic Action |
| :--- | :--- | :--- |
| **Peak (Mar/Nov)** | 12k+ Transaction Stress | **Dynamic Staffing:** Implement temporary hiring cycles to handle volume surges. |
| **Off-Peak (Jul/Aug)** | Performance Valley | **System Resilience:** Schedule Data Warehouse upgrades and staff development. |
| **Full Year** | Downward Trend | **User Retention:** Launch targeted marketing to address reduced engagement in 2024. |

## Visual Graphs
<img width="788" height="449" alt="GROSS REVENUE BASED ON FESTIVE EVENT FROM 2022 - 2024" src="https://github.com/user-attachments/assets/8de84ae3-feaa-4fa4-ac34-052e92b56cf6" />

<img width="800" height="405" alt="Top 5 Genre Performance and Investment Priority Comparison Report (2022 - 2024)" src="https://github.com/user-attachments/assets/d283abbc-c6e4-46dd-a872-d1f7aadc83dd" />

<img width="624" height="473" alt="OPERATIONAL EFFICIENCY BY PEAK PERIOD VS OFF-PEAK" src="https://github.com/user-attachments/assets/088a3e1c-a1c1-48a1-8f13-590c124df5ff" />
