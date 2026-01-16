# Hospitality Revenue Intelligence: Predictive Lead & Cancellation Analysis

## 📌 Executive Summary
This project is a large-scale strategic analysis of **119,390 hotel booking records** aimed at optimizing Yield Management and Revenue Operations. By performing an end-to-end audit of City and Resort hotel data, I identified critical drivers of **Revenue Leakage** (Cancellations) and developed a data-driven framework for **Dynamic Pricing** and **Demand Forecasting.**

## 🎯 Strategic Business Objectives
* **Revenue Protection:** Analyze the 27% cancellation rate to identify high-risk segments and mitigate loss.
* **Yield Optimization:** Correlate ADR (Average Daily Rate) with seasonality to maximize RevPAR (Revenue Per Available Room).
* **Customer Lifecycle Value:** Segment transient vs. contract guests to tailor loyalty and retention strategies.

## 🛠 Advanced Technical Implementation
* **Data Sanitization & Engineering:** Processed 119k+ rows, engineered `Total_Revenue` and `Stay_Duration` metrics, and performed IQR-based outlier treatment for skewed ADR data.
* **Behavioral Correlation Mapping:** Discovered a negative correlation between "Special Requests" and "Cancellations," identifying customer engagement as a proxy for booking commitment.
* **Lead-Time Modeling:** Analyzed the 80-day average lead time to determine optimal windows for "Early Bird" pricing interventions.

## 💡 High-Impact Business Insights
* **The Cancellation-ADR Link:** Higher ADRs correlate with higher cancellation rates, suggesting a **Price Sensitivity Threshold** where guests are more likely to churn for better deals.
* **Strategic Seasonality:** While August peaks in volume, **March represents the highest Revenue Efficiency** due to optimized ADR-to-stay-duration ratios.
* **The "Commitment" Indicator:** Guests with at least one special request are significantly more likely to complete their stay, providing a key feature for predictive cancellation models.
* **City vs. Resort Dynamics:** City Hotels face double the cancellation risk (40%) compared to Resort Hotels (20%), requiring more aggressive non-refundable deposit policies for urban properties.

## 🚀 Revenue-Focused Recommendations
1. **Dynamic Deposit Tiering:** Implement non-refundable "Flash Rates" for City Hotels during high-lead-time windows to lock in revenue.
2. **March-Standardization:** Replicate the high-margin booking conditions of March across Q2/Q3 through targeted corporate and luxury-segment campaigns.
3. **Engagement-Driven Retention:** Use automated guest-engagement prompts (special request queries) as a tool to increase "mental commitment" and reduce churn in transient segments.

---

