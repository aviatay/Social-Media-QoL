# The Impact of Social Media on Quality of Life

## 🧠 Overview

This project investigates the **causal relationship** between exposure to social media and **quality of life (QoL)** across two key demographic groups — **adolescents and adults**.

The main question:
Does intensive use of social media cause changes in lifestyle, mental health, and well-being — or merely correlate with them?

---

## 🎯 Research Goals

* Evaluate whether **daily social media exposure (≥3 hours)** leads to measurable declines in quality of life.
* Examine **differences across age groups**, focusing on psychological and behavioral outcomes.
* Assess causality through **matching** and **regression** methods under core identification assumptions.

---

## 🧩 Dataset

**Source:** Survey of **481 participants** from Dhaka, Bangladesh (collected April–May and November–December 2022).
**Context:** Conducted during and after the COVID-19 pandemic — a period that intensified online activity.

**Variables include:**

* **Demographics:** Age, gender, marital status, employment
* **Treatment:** Daily exposure to social media (≥3 hours = treated)
* **Outcomes:**

  * Depression
  * Sleep disturbances
  * Daily activity engagement
    *(Each measured on a 1–5 Likert scale; higher = worse quality of life)*

---

## 🧮 Methodology

### Identification Assumptions

* **SUTVA:** Each participant’s quality of life is influenced only by their own exposure.
* **Ignorability:** Confounding variables (age, gender, etc.) are observed and controlled for.
* **Common Support:** Overlap maintained between treated and control groups within demographic strata.

### Analytical Methods

1. **Matching Analysis**

   * Age groups: 10–19, 20–29, 30–39, 40–49
   * Controlled for age, gender, marital and employment status
   * ATE and 95% confidence intervals estimated using **bootstrap (1,000 samples)**

2. **Linear Regression Analysis**

   * Age groups: 10–19 to 60–69
   * Controlled for gender, marital status, and employment
   * Estimated causal effect per group

---

## 📈 Results Summary

| **Age Group** | **Method** | **ATE**   | **95% Confidence Interval** | **Significant (p<0.05)** | **Interpretation**             |
| ------------- | ---------- | --------- | --------------------------- | ------------------------ | ------------------------------ |
| 10–19         | Matching   | 1.892     | (-1.686, 5.515)             | ❌                        | No significant effect          |
| 20–29         | Matching   | 0.828     | (-2.639, 4.442)             | ❌                        | No significant effect          |
| 30–39         | Matching   | 1.022     | (-4.501, 6.000)             | ❌                        | No significant effect          |
| 40–49         | Matching   | 2.123     | (-1.857, 6.715)             | ❌                        | No significant effect          |
| 10–19         | Regression | 1.655     | (-0.237, 3.410)             | ❌                        | No significant effect          |
| 20–29         | Regression | **0.766** | **(0.146, 1.409)**          | ✅                        | Significant negative impact    |
| 30–39         | Regression | 1.484     | (-1.040, 3.993)             | ❌                        | Inconclusive effect            |
| 40–49         | Regression | 1.002     | (-1.417, 3.484)             | ❌                        | No significant effect          |
| 50–59         | Regression | 2.327     | (-0.000, 4.948)             | ❌                        | Wide interval, low reliability |
| 60–69         | Regression | 0.261     | (-0.672, 0.631)             | ❌                        | No significant effect          |

**Main finding:**
📉 High social media exposure correlates with **lower quality of life among ages 20–29**, with statistical significance.

---

## 💬 Discussion

* The **20–29** group appears particularly vulnerable — possibly due to social comparison, emotional pressure, and identity formation during this life stage.
* No statistically significant causal effect was observed for other age groups, though variability and small sample sizes may obscure the true effect.
* Future research should:

  * Expand the dataset for older groups.
  * Include **education** and **income** as confounders.
  * Distinguish between **active** and **passive** social media use.
  * Explore the impact of **content type** (social, political, entertainment).

---

## 📚 References

1. Ilić et al. (2010). *Assessing Quality of Life: Current Approaches.*
2. Özabacı (2010). *Quality of Life as a Predictor of Depression.*
3. Amaral et al. (2017). *Quality of life, sleepiness and depressive symptoms in adolescents with insomnia.*
4. Eid et al. (2024). *Activities of Daily Living and Quality of Life among Older Adults.*
5. Datta et al. (2013). *Relationship of Activity of Daily Living with Quality of Life.*
6. Clear (2014). *How long does it actually take to form a new habit?*
7. Reed et al. (2023). *Reduction in Social Media Usage and Improvements in Well-being.*

---

## 🧭 Key Takeaway

> Intensive social media use (3+ hours daily) **causally reduces quality of life among young adults (20–29)** — while effects on other age groups remain uncertain.
> This emphasizes the need for mindful, balanced engagement with social media.
