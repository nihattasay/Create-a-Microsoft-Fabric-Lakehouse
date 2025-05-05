# Create-a-Microsoft-Fabric-Lakehouse
# 🧱 Microsoft Fabric Lakehouse - End-to-End Data Analytics Lab

This project demonstrates how to build a complete data analytics solution using **Microsoft Fabric Lakehouse**, including file ingestion, transformation, SQL querying, and visualization.

> 💡 This lab is based on the **Microsoft Learn Fabric Lab** and requires an active [Microsoft Fabric trial](https://app.fabric.microsoft.com/home?experience=fabric).

---

## 📌 Lab Objectives

1. **Create a Workspace** – Set up a Microsoft Fabric workspace with Fabric capacity enabled.
2. **Create a Lakehouse** – Provision a Lakehouse with support for file and table storage (Delta format).
3. **Upload Data** – Download and upload `sales.csv` to a subfolder inside the Lakehouse.
4. **Explore Shortcuts** – View options to reference external data via shortcuts.
5. **Load File into Table** – Convert `sales.csv` into a managed Delta table named `sales`.
6. **Query with SQL** – Use the SQL endpoint to perform aggregations on the `sales` table.
7. **Visual Query** – Use Power Query to group and transform sales data visually.
8. **Create a Report** – Build a Power BI report from Lakehouse data using visual tools.
9. **Clean Up** – Optionally delete the workspace after completing the lab.

---

## 🧪 Sample SQL Query

```sql
SELECT Item, SUM(Quantity * UnitPrice) AS Revenue
FROM sales
GROUP BY Item
ORDER BY Revenue DESC;
```

---

## 📊 Output

- **Lakehouse** with structured and unstructured data
- **Managed Delta Table** for SQL querying
- **SQL Analytics Endpoint** for queries
- **Visual Query** using Power Query interface
- **Power BI Report**: Clustered bar chart of item sales

---

## 📁 Files Used

- [sales.csv](https://raw.githubusercontent.com/MicrosoftLearning/dp-data/main/sales.csv)

---

## 📎 References

- [Microsoft Fabric](https://app.fabric.microsoft.com/)
- [Microsoft Learn GitHub](https://github.com/MicrosoftLearning/mslearn-fabric)

---

## 🧹 Cleanup Instructions

To delete the environment:
1. Open workspace settings.
2. Click **Remove this workspace** under the General tab.

---

## 📌 Notes

- Delta tables created are stored in **OneLake** with Parquet format and `_delta_log`.
- A default **semantic model** is automatically generated for Power BI reporting.
- The lab showcases both **code-first** (SQL/Spark) and **low-code** (visual) approaches.
