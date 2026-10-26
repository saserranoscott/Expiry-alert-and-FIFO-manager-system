# Expiry Alert & FIFO Manager System

> A batch-level inventory management engine designed to prevent product expiration losses through automated FIFO (First-In, First-Out) stock rotation and proactive expiry alerts.

## 📌 Problem Overview
In many small-to-medium retail businesses and independent pharmacies, standard POS systems fail to track inventory at the batch level. Most barcode scanners only identify the product, not its specific expiration date or batch number. Furthermore, flawed database constraints in legacy software often restrict entering multiple batches with identical expiry dates, leading to inventory miscalculations, misplaced stock, and financial losses from expired goods.

## 💡 Solution
This system addresses these real-world operational gaps by providing:
* **Batch-Level Granularity:** Tracks distinct batches per product using a synthetic primary key model, allowing multiple batches to share identical expiration dates without database conflicts.
* **Automated FIFO Deduction:** Automatically deducts inventory starting from the batch closest to expiration whenever a sale or dispatch is processed.
* **Proactive Expiry Alerts:** Categorizes stock into status tiers (*Normal*, *Near Expiry*, and *Expired*) to prompt timely stock rotation and vendor returns.

## 🛠 Tech Stack
* **Language:** Java
* **Database:** Microsoft SQL Server (JDBC)
* **Design Pattern:** Data Access Object (DAO) / Separation of Concerns
