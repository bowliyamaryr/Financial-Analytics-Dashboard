# 📊 DAX Measures

This document contains the DAX measures used in the **Financial Analytics Dashboard** developed in Microsoft Power BI.

---

## 📈 Total Sales

```DAX
Total Sales =
ROUND(SUM('dataset'[Sales]), 2)
```

**Purpose:** Calculates the total sales amount rounded to 2 decimal places.

---

## 💰 Total Profit

```DAX
Total Profit =
SUM('dataset'[Profit])
```

**Purpose:** Calculates the total profit generated.

---

## 💵 Total Cost

```DAX
Total Cost =
SUM('dataset'[Cost])
```

**Purpose:** Calculates the total cost incurred.

---

## 📦 Total Orders

```DAX
Total Orders =
COUNTROWS('dataset')
```

**Purpose:** Counts the total number of orders in the dataset.

---

## 📊 Average Sales

```DAX
Average Sales =
AVERAGE('dataset'[Sales])
```

**Purpose:** Calculates the average sales value.

---

## 📊 Average Profit

```DAX
Average Profit =
AVERAGE('dataset'[Profit])
```

**Purpose:** Calculates the average profit value.

---

## 📊 Average Cost

```DAX
Average Cost =
AVERAGE('dataset'[Cost])
```

**Purpose:** Calculates the average cost value.

---

## 🚀 Profit Condition

```DAX
Profit Condition =
VAR Profit = [Total Profit]

RETURN
SWITCH(
    TRUE(),
    Profit >= 15000000, "Excellent",
    Profit >= 8000000, "Good",
    "Bad"
)
```

**Purpose:** Classifies overall profit performance into **Excellent**, **Good**, or **Bad** based on predefined thresholds.

---

## 📈 Sales Condition

```DAX
Sales_Condition =
VAR Sales = [Total Sales]

RETURN
SWITCH(
    TRUE(),
    Sales >= 40000000, "High",
    Sales >= 20000000, "Medium",
    "Low"
)
```

**Purpose:** Categorizes sales performance into **High**, **Medium**, or **Low**.

---

## 🛠 Skills Demonstrated

- DAX Measure Creation
- Aggregate Functions
- Variables (`VAR`)
- Conditional Logic using `SWITCH`
- KPI Development
- Business Performance Analysis

---

## 📌 Notes

These DAX measures were created as part of the **Financial Analytics Dashboard** project to support KPI reporting and interactive business analysis in Microsoft Power BI.

**Author:** Bowliya Mary
