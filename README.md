# 🏨 Hotel Booking Data Analysis — End-to-End Exploratory Project

> **Executive Summary:**  
> This project analyzes **119,390 hotel booking records** from a City and Resort hotel to uncover **cancellation trends, revenue drivers, and customer behavior patterns**.  
> Through exploratory data analysis (EDA), the study reveals key insights on **seasonality, pricing strategy, and booking behavior**, helping hotels make **data-driven business decisions** to improve profitability and reduce cancellations.

---

## 🎯 Objective

The goal of this project is to perform a **comprehensive analysis of hotel booking data** to extract actionable insights that can help hospitality businesses:

- 📈 **Improve booking efficiency** by understanding customer booking patterns.  
- 🚫 **Reduce cancellations** through behavioral insights and policy optimization.  
- 👥 **Understand customer demographics & preferences** to enhance marketing strategies.  
- 💶 **Optimize pricing and revenue** by identifying high-value segments and seasonal trends.  
- ⚙️ **Support data-driven decision-making** for operations, resource allocation, and forecasting.

---

## 🗂️ Dataset Overview

The dataset contains detailed information about hotel bookings from two types of hotels — **City Hotel** and **Resort Hotel** — collected between **2015 and 2017**.

| Metric | Description |
|--------|-------------|
| **Records** | 119,390 |
| **Features** | 31 |
| **Hotel Types** | City Hotel (≈61%), Resort Hotel (≈39%) |
| **Average Daily Rate (ADR)** | €106 (mean), with significant variability |
| **Average Lead Time** | 80 days |
| **Cancellation Rate** | ~27% of all bookings |
| **Common Stay Duration** | 1 weekend night and 2 weeknights |
| **Peak Month for Bookings** | August |
| **Dominant Customer Type** | Transient (individual travelers) |
| **Deposit Type** | Mostly “No Deposit” |
| **Special Requests** | Typically ≤ 1 per booking |

---

## 🧹 Data Preprocessing

To ensure analytical accuracy, several preprocessing steps were applied:

1. **Missing Value Handling**
   - Replaced `'NULL'` with `NaN`.
   - Imputed missing categorical and numerical values using mode and median respectively.

2. **Data Type Conversion**
   - Converted date columns to `datetime`.
   - Encoded categorical data for correlation and visualization.

3. **Outlier Treatment**
   - Detected outliers in `adr` and `lead_time` using IQR method.
   - Removed unrealistic pricing and booking intervals.

4. **Feature Engineering**
   - Created new features:
     - `total_nights` = `stays_in_week_nights` + `stays_in_weekend_nights`
     - `total_revenue` = `adr * total_nights`
   - Extracted **month**, **year**, and **season** from arrival dates.

5. **Data Integrity**
   - Removed duplicates and validated column consistency.

---

## 📊 Exploratory Data Analysis (EDA)

### 1. 🕒 Lead Time Distribution
- Majority of bookings occur within **0–100 days** of arrival; median ≈ **45 days**.  
- The distribution is **right-skewed**, with a few extreme advance bookings.  

**💡 Insight:**  
Encourage **early reservations** through advance-booking discounts to smooth out demand volatility.

---

### 2. 🛏️ Stay Duration Analysis
- Most guests stay **0–3 days on weekends** and **0–8 days on weekdays**.  
- Indicates dominance of **short business or city stays**.

**💡 Suggestion:**  
Promote **short-stay packages** and **corporate plans** to align with demand.

---

### 3. 🚫 Cancellation Analysis

| Variable | Observation |
|-----------|--------------|
| **Hotel Type** | City Hotels show ~40% cancellations vs 20% in Resort Hotels. |
| **Customer Type** | Transient customers have the highest cancellation rate (~40%). |
| **Deposit Type** | “No Deposit” bookings (majority) have ~25% cancellations; “Non-Refund” shows 90% but small volume. |
| **Meal Type** | “Bed & Breakfast (BB)” is most common with ~30% cancellations. |

**💡 Insights:**
- High cancellations linked to **flexible booking types**.  
- City Hotels’ short-stay nature leads to more cancellations.

**💡 Recommendation:**  
Introduce **tiered refund policies** or **discounted prepayments** to balance flexibility and commitment.

---

### 4. 🔗 Correlation Insights

| Relationship | Observation |
|--------------|--------------|
| `total_of_special_requests` ↔ `is_canceled` | Negative — guests with more requests cancel less. |
| `adr` ↔ `adults` / `children` | Positive — higher group size correlates with higher ADR. |
| `is_repeated_guest` ↔ `previous_bookings_not_canceled` | Strong positive — repeat guests are loyal. |
| `previous_cancellations` ↔ `previous_bookings_not_canceled` | Positive — frequent customers both book and cancel more often. |

**💡 Business Takeaway:**  
Repeat customers show strong engagement — a **loyalty rewards system** can strengthen retention and reduce cancellations.

---

### 5. 💶 ADR (Average Daily Rate) Analysis
- Most ADRs range between **€50–€100**.  
- A few **premium bookings** significantly raise the average.  
- Slightly **higher ADRs** in canceled bookings indicate **price sensitivity**.

**💡 Recommendation:**  
Use **dynamic pricing models** to balance room demand and cancellation risk.

---

### 6. 🌍 Country-wise Booking Trends
- **Portugal** accounts for the highest number of bookings.  
- **Great Britain** and **France** follow, with about **⅓ of Portugal’s volume**.  

**💡 Recommendation:**  
Enhance **domestic loyalty programs** and **regional promotions** in Portugal, while **expanding targeted campaigns** in the UK and France.

---

### 7. 💹 Monthly and Revenue Insights
- **March** generates the **highest revenue**, despite moderate booking volume.  
- **August** records the **most bookings** but with lower ADR, reducing profit margins.

**💡 Insights:**
- March’s high revenue is driven by **higher ADR and longer stays**.  
- August’s strong volume can be leveraged with **seasonal price adjustments**.

**💡 Strategy:**  
Implement **dynamic seasonal pricing** to boost profit during high-demand months like August.

---

### 8. 👥 Revenue by Customer Type
- **Transient customers** dominate total revenue.  
- **Group and Contract** customers contribute least.

**💡 Recommendation:**  
- Design **loyalty programs** and **referral offers** for transient guests.  
- Partner with **corporate clients** to grow the underperforming contract segment.

---

## 🧭 Insights by Objective

| Objective | Findings | Actionable Recommendation |
|------------|-----------|----------------------------|
| **Booking Efficiency** | Short booking windows; 45-day median lead time | Offer **early-bird incentives** to encourage advance booking |
| **Cancellation Reduction** | City Hotels & Transient customers cancel most | Enforce **tiered refund policies** and **flexible deposits** |
| **Customer Understanding** | Portugal leads bookings; short stays dominate | Tailor **local campaigns** and **short-stay offers** |
| **Revenue Optimization** | March highest revenue, August highest volume | Use **seasonal dynamic pricing** to align volume and profit |

---

## 🧰 Tools & Technologies

- **Language:** Python  
- **Libraries:** pandas, numpy, matplotlib, seaborn  
- **Environment:** Jupyter Notebook  
- **Techniques:** Descriptive Statistics, Correlation Heatmap, Boxplots, Histograms, Count Plots, Revenue Estimation  

---

## 🗂️ Project Structure

