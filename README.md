# Boston Housing Data Analysis: Executive Insights for Urban Development

## 📌 Project Overview
As a Data Scientist for the Boston Housing Agency, this project analyzes structural, environmental, and demographic factors collected by the U.S. Census Service in Boston, MA. The objective is to provide upper management with actionable, statistically backed insights to optimize housing policy and market predictions.

This analysis evaluates key executive questions regarding property valuations (`MEDV`), environmental impacts (`NOX`), industrial zoning (`INDUS`), proximity to the Charles River (`CHAS`), and structural age dependencies (`AGE`).

---

## 🛠️ Methodology & Project Workflow

The project follows a rigorous exploratory and inferential data science workflow divided into three strategic phases:

### Phase 1: Data Audit & Integrity Check
* Initialized data profiling by auditing structural shapes (506 observations), inspecting data types, and verifying data completeness (missing values and duplicates check).
* Constructed a global **Correlation Matrix** to identify preliminary linear dependencies across all features.

### Phase 2: Descriptive Statistics & Visual Analytics
Generated targeted visual representations to uncover underlying patterns:
* **Overall Market Distribution:** Boxplots evaluating outliers and density profiles for the median value of homes (`MEDV`).
* **Zoning & Location Profiles:** Bar charts assessing the representation of properties tracking the Charles River (`CHAS`).
* **Demographic Cohort Analysis:** Discretized historical building data (`AGE`) into three custom generations (*35 years or younger*, *between 36 and 70 years*, and *71 years and older*) to evaluate its relationship with asset valuation.
* **Environmental & Resource Mapping:** Scatter plots mapping chemical concentrations (`NOX`) against commercial density (`INDUS`), and detailed histograms capturing the distribution of the Pupil-Teacher Ratio (`PTRATIO`), showing a clear concentration above 20.

### Phase 3: Inferential Statistical Testing & Predictive Modeling
Validated corporate hypotheses using strict statistical thresholds ($\alpha = 0.05$):
1. **Variance Homogeneity:** Applied **Levene’s Test** to check if the variances of `MEDV` for homes bounded by the Charles River (`CHAS = 1`) and those not bounded (`CHAS = 0`) are equal.
2. **Mean Difference Testing:** Conducted an independent **T-test** to determine if there is a significant difference in `MEDV` between homes based on river proximity.
3. **Multi-Group Comparisons:** Executed a One-way **ANOVA** to compare average `MEDV` among the three custom `AGE` cohorts.
4. **Feature Interdependence:** Performed a **Pearson Correlation Test** to measure the exact linear relationship between Nitric Oxide concentrations (`NOX`) and the proportion of non-retail business acres (`INDUS`).
5. **Predictive Analytics:** Fitted an **Ordinary Least Squares (OLS) Linear Regression** model to quantify the impact of an additional weighted distance to the five Boston employment centers (`DIS`) on `MEDV`.

---

## 📊 Core Business Insights & Analytical Findings

Based on the statistical tests executed in the notebook, here are the key takeaways delivering immediate value to the agency:

* **The Charles River Premium:** The **T-test** (preceded by Levene's test for variance checking) confirmed that properties adjacent to the Charles River (`CHAS = 1`) command a statistically significant difference in their average market value compared to those that are not.
* **The Structural Age Factor:** The **ANOVA** test proved that the average value of homes (`MEDV`) differs significantly across the three age categories, showing that newer developments retain higher market values.
* **Industrial-Environmental Nexus:** A strong positive **Pearson correlation** demonstrated a clear linear relationship between `NOX` and `INDUS`, meaning that areas with higher industrial density suffer from significantly higher air pollution.
* **Employment Proximity Impact:** The **OLS Regression** model established that distance to employment centers (`DIS`) significantly impacts property pricing. The model yielded an **R-squared of 0.062**, which translates to a **correlation coefficient of 0.25**, indicating a statistically significant but **very weak** positive relationship between distance and house values.

---

## 💻 Tech Stack & Libraries Used
* **Language:** Python
* **Data Manipulation:** `pandas`, `numpy`
* **Statistical Inference & Modeling:** `scipy.stats`, `statsmodels`
* **Data Visualization:** `matplotlib`, `seaborn`

---
*Analysis developed by Javier Rodríguez (SyntaxPure)*
