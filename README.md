# Fitness Tracker Data Analysis with PySpark

**Dataset:** FitBit Fitness Tracker Data (dailyActivity_merged.csv, sleepDay_merged.csv, hourlySteps_merged.csv).

**Questions:** How do steps/calories affect sleep duration? How do steps relate to heart rate (stress proxy)? Optional: Does morning vs. evening exercise matter?

**Tools:** PySpark, Tableau.

**Timeline (~5 hours):**
- **0:00-0:45:** Set up Databricks, upload CSVs, create notebook.
- **0:45-1:45:** Load activity and sleep CSVs, explore schemas, check stats.
- **1:45-2:45:** Clean data (remove nulls, filter), join tables, add StepCategory.
- **2:45-4:15:** Aggregate (avg sleep by steps, steps by heart rate), plot 2-3 visuals (scatter: steps vs. sleep; bar: sleep by step category).
- **4:15-5:00:** Document notebook, save results to CSV, export as HTML/PDF.

**Output:** Notebook with code, comments, 2-3 plots, and a CSV of results.

**Learning:** Load DataFrames, filter/join/groupBy, save data, lazy evaluation.