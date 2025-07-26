# Lab 6: Association Rule Mining with Apriori and FP-Growth

**Author:** Rutu Ketankumar Shah  
**Course:** Advanced Big Data and Data Mining  
**Lab Title:** Association Rule Mining with Apriori and FP-Growth  
**Dataset:** Online Retail Dataset (UCI Machine Learning Repository)

---

##  Purpose

The goal of this lab was to explore frequent itemset mining and association rule generation using two fundamental algorithms in data mining:

- **Apriori Algorithm**
- **FP-Growth Algorithm**

By applying these methods to a real-world transactional dataset, we aimed to uncover hidden patterns, frequent product combinations, and strong association rules that can inform cross-selling or marketing strategies.

---

##  Key Insights

- Both **Apriori** and **FP-Growth** identified similar frequent itemsets when using the same support threshold (1%).
- Association rules with **high confidence (> 0.7)** and **lift (> 1.0)** revealed strong product correlations (e.g., customers who purchase item A are very likely to purchase item B).
- The **top 10 frequent itemsets** included commonly purchased decorative items, suggesting opportunities for product bundling.

Visualizations such as barplots of frequent itemsets and scatter plots of **confidence vs. lift** helped in identifying the most valuable patterns.

---

## Tools & Libraries

- Python (Pandas, Seaborn, Matplotlib)
- `mlxtend` for Apriori and FP-Growth algorithms
- Jupyter Notebook for analysis
- Dataset: Online Retail Dataset (`Online Retail.xlsx`)

---

##  Challenges & Decisions

- **Large Data Load Time:**  
  The original dataset (~500K records) was slow to load and process. This was resolved by cleaning the data upfront and using country-level filters (e.g., UK-only transactions).

- **Deprecation Warning:**  
  A warning from `applymap()` was resolved by switching to a more efficient and recommended method using boolean masking.

- **Sparse Rule Generation:**  
  When initial rules were too few due to high confidence thresholds, the `min_threshold` was adjusted to a more lenient value (e.g., 0.4) to generate richer results.

---

##  Conclusion

This lab demonstrated how both Apriori and FP-Growth can effectively uncover hidden associations in market basket data. While Apriori is conceptually simple, FP-Growth offers better scalability. Visual and rule-based insights extracted from this analysis can be applied in various domains, including recommendation systems and targeted marketing.
