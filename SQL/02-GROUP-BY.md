# SQL GROUP BY

## What is GROUP BY

GROUP BY is used to group rows that have the same values.

---

# COUNT Example

```sql
SELECT parent_id, COUNT(*) AS child_count
FROM bom_items
GROUP BY parent_id;
```

---

# SUM Example

```sql
SELECT department_id, SUM(salary) AS total_salary
FROM employees
GROUP BY department_id;
```

---

# HAVING Example

```sql
SELECT parent_id, COUNT(*) AS child_count
FROM bom_items
GROUP BY parent_id
HAVING COUNT(*) > 2;
```

---

# GROUP BY Notes

- GROUP BY is usually used with aggregate functions
- Common aggregate functions:
  - COUNT()
  - SUM()
  - AVG()
  - MAX()
  - MIN()

---

# Interview Questions

## Difference between WHERE and HAVING

WHERE filters rows before grouping.

HAVING filters groups after GROUP BY.

---

# Practice

- Count BOM child materials
- Calculate total quantity
- Find materials with more than 3 child nodes
