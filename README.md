# 🧠 Momentum Metrics: Understanding Real User Engagement

**Status:** Complete  
**Type:** Exploratory Data Analysis (EDA) + Feature Engineering  
**Tools Used:** Python (Pandas, Matplotlib, Seaborn), Jupyter Notebook

---

## 📌 Project Goal

To explore and quantify **user engagement patterns** beyond surface-level metrics like total check-ins. 
This project focuses on creating **normalized features** that better reflect *momentum* and *depth* of user interaction.

---

## 🧩 Key Questions

- How can we tell if a user is *truly engaged*—not just logging activity?
- What patterns indicate **loss of momentum** before dropoff?
- Can we create better features from existing columns to support modeling?

---

## 🔨 Core Techniques

- **Feature Engineering:**
  - `checkins_per_day` = total check-ins normalized by task duration
  - Imputed missing/zero durations to avoid division errors
  - Created binary flags for edge cases (e.g. `is_one_day_task`, `zero_checkins`)
  
- **Exploratory Analysis:**
  - Visualized distribution of engagement features
  - Compared high vs. low engagement cohorts
  - Surfaced edge cases with boxplots and histograms

- **Outlier Handling & Missing Data:**
  - Used custom thresholds for realistic edge filtering
  - Filled nulls strategically to preserve analytic integrity

---

## 📊 Visualization

- Boxplot of `checkins_per_day` grouped by task category  
- Histogram showing where engagement drops sharply  


---

## 💡 Key Insights

- Many users “appear” active but show low normalized check-in density → false positives.
- Tasks under 1-day duration often skew engagement metrics—needed flagging.
- Visual analysis showed engagement decay near deadlines—worth modeling further.

---

## 🔍 Next Steps

- Build engagement prediction model using engineered features  
- Create dashboard version for non-technical stakeholders  
- Apply similar approach to long-term product usage datasets

---

## 🧰 Lessons Learned

> “Feature engineering isn’t just math—it’s **asking smarter questions** about behavior.”

This project deepened my understanding of how raw activity can **mislead**, and why good analysts don’t stop at totals.

---

## 📁 File Structure
📦 momentum-metrics/
┣ 📜 momentum_metrics.py
┣ 📜 README.md
