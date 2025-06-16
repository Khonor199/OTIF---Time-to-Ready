# OTIF---Time-to-Ready

## 📊 Research on the time of order co-ordination (`time_to_ready`)

## 🎯 Purpose of the study

To investigate the metric `time_to_ready` (time to order reconciliation between customer and supplier), identify its patterns, dependencies and impact on key metrics: OTIF, share of overdue orders (`late_%`) and delivery times.

---

## 📏 Metric Description

`time_to_ready` is the time (in days) from order creation to supplier approval.  
This is a critical step in the supply chain, affecting further operations: shipment planning, delivery dates, order fulfilment on time.

---

## 🧭 Approach

- Analysis of `time_to_ready` distribution
- Clustering of orders by processing time
- Hypothesis testing of relationships with other metrics
- Automatic search for anomalous objects:
  - Distribution Centres
  - Customers
  - Customer Catalogues
  - Legal Entities
- Dependency visualisation
- Predictive model building using **CatBoost**, interpretation via **SHAP**

---

## 🧪 Hypotheses

1. ** As `time_to_ready` increases, `late_%` within a cluster grows.** 
 ✅ Tested using χ² test for trends.

2. **Median `time_to_ready` varies for at least one day of the week.** 
 ✅ Checked using the Kraskell-Wallis test.

---

## 🔍 Results

- A **statistically significant relationship** was found between approval times and the proportion of delinquencies (`late_%`).
- Identified **days of the week** where approval times are systematically higher/lower.
- Created automated scripts to find ‘bad’ groups (RAs, customers, etc.) with high `time_to_ready`.
- Built **CatBoostRegressor** model to predict `time_to_ready`, finding key influencers via **SHAP values**.
- Found the `time_to_ready` significance threshold at which the risk of order delay increases significantly.

---
