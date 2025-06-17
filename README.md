# 🥤 Soda Sales Time Series Analysis (RainMan Case Study)

This project analyzes a time series dataset of a fictitious soft drink company to explore sales patterns and the impact of advertising and promotions using Excel-based statistical analysis.

---

##  Dataset Description

- **Time Period:** Jan 2012 to Sept 2015 (monthly granularity)
- **Columns Included:**
  - `Month` — Date of observation
  - `SalesVol` — Sales volume in litres
  - `TVGRP` — TV Gross Rating Points (advertising exposure)
  - `Instoreads` — In-store advertisement spend
  - `Outdoorads` — Outdoor advertisement spend
  - `Digitalads` — Digital advertisement spend
  - `Promotions` — Promotion spend (discounts, offers, gifts)
  - `Price` — Average price per 10 litres
  - `Comp1TV`, `Comp1NP` — Competitor 1 media spend (TV and Newspaper)
  - `Comp2OOH`, `Comp2NP` — Competitor 2 media spend (Outdoor and Newspaper)

---

##  Key Analysis Conducted

### 1️⃣ Seasonality Check  
- Observed clear seasonal patterns — sales tend to increase in summer months, indicating strong seasonality.

### 2️⃣ Trend Analysis  
- A moderate upward trend observed across the years, indicating stable market growth.

### 3️⃣ Correlation Analysis  
- ✅ **Media Impact:**
  - Positive correlation between Sales Volume and advertising spends across TVGRP, Instoreads, Outdoorads, Digitalads.
- ✅ **Price Sensitivity:**
  - Negative correlation between Price and Sales Volume, indicating price elasticity of demand.
- ✅ **Promotions Impact:**
  - Positive correlation between Promotions spend and Sales Volume.

### 4️⃣ Competitor Impact Analysis  
- **Competitor 1's TV Spend (Comp1TV)** showed a stronger inverse relation with our sales compared to other competitor spends.

---

##  Adstock Transformation (Carryover + Saturation Effect)

To better capture the long-term and saturation effects of advertising, Adstock transformation was applied on the **TVGRP** variable:

**Adstock Formula Used:**

A(t) = L × A(t−1) + g(t)^n / (g(t)^n + k^n)

Where:
- **L** = Carryover parameter (0 ≤ L ≤ 1)
- **k** = Saturation parameter (k > 0)
- **n** = Response curve shape parameter (n > 0)

### Parameter Testing Results:

| K Value | Correlation (Sales vs Adstock) |
|---------|----------------------------------|
| 100     | 0.4989 |
| 1000    | **0.5912 (Best Fit)** |
| 3000    | 0.5798 |

➡ Based on correlation strength, **K = 1000** was chosen as optimal.

---

## 🛠 Tools Used

- **Microsoft Excel** — Data cleaning, transformation, statistical calculations
- **Statistical Techniques** — Seasonality detection, correlation, partial correlation, Adstock modeling

---

##  Key Business Takeaways

- Summer seasonality plays a key role in driving sales.
- Promotions and media spending have positive sales impact.
- Competitor 1's TV advertisements significantly affect sales volume.
- Adstock modeling provides deeper insight into media saturation effects.

---

## 👩‍💻 About Me

I am an aspiring Data Analyst passionate about analyzing real-world business data using data science techniques.

📧 nirmalashanthi04@gmail.com  
🔗 [LinkedIn] (https://www.linkedin.com/in/shanthi-nirmala2001/)

