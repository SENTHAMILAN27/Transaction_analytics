# Payment Channel Performance and Failure Analytics

## 📊 Project Overview
A 7-page interactive Power BI dashboard analyzing 
598,496 payment transactions for a banking client 
across ATM, Online, and POS channels over 2 years 
(January 2023 – December 2024).

## Dashboard Preview
![Dashboard Preview](preview.png)

## 🔍 Key Findings

| Finding | Detail |
|---|---|
| ATM Failure Rate | 21.12% — highest channel |
| Peak Hour Spike | 24-25% during 10AM-1PM and 5PM-9PM |
| Anomaly Threshold | 104.93 seconds (Mean + 2SD) |
| ATM Anomalous Duration | 117 seconds avg — exceeds threshold |
| Geographic Risk | Lucknow 20.09% vs Mumbai 12.37% |
| Network Gap | RuPay 19.73% vs Amex 8.88% |
| Trend | Flat 15-16% failure rate for 24 months |

## 📈 Dashboard Pages

1. **Home** — Navigation hub with project overview 
   and key metrics
2. **Executive Summary** — Overall health KPIs, 
   channel comparison, day-of-week patterns
3. **Failure Analysis** — Hour vs channel heatmap, 
   failure type breakdown, duration analysis, 
   bookmark toggle between channel and network views
4. **Location Analysis** — City-wise risk ranking, 
   top 5 and bottom 5 city tables, payment network 
   comparison
5. **Transaction Profile** — Debit vs Credit split, 
   payment network volume, channel amount distribution
6. **Anomaly Detection** — Statistical outlier 
   detection using Mean + 2SD, peak hour deviation 
   analysis, anomalous hour summary table
7. **Recommendations** — 6 prioritized 
   recommendations with data evidence

## 🛠 Technical Details

**Tools:** Microsoft Power BI Desktop, DAX, 
Power Query, Microsoft Excel

**Dataset:** 598,496 synthetic banking transactions
- 3 channels: ATM, Online, POS
- 4 payment networks: RuPay, Visa, MasterCard, Amex
- 15 cities across India
- 10 customer occupation segments
- January 2023 to December 2024

**DAX Techniques Used:**
- Time intelligence: PREVIOUSMONTH, TOTALYTD, 
  SAMEPERIODLASTYEAR
- Statistical: STDEV.P, MAXX, MINX for anomaly 
  detection and dynamic KPI cards
- Pattern: CALCULATE with multiple filter contexts
- Text measures: SWITCH, FORMAT, VAR patterns 
  for dynamic card values

**Power Query Steps:**
- Extracted TransactionHour, TransactionDate, 
  DayOfWeek, MonthYear from datetime column
- Created TimeOfDay, DurationCategory, 
  LoginRiskFlag calculated columns
- Built separate DateTable with Mark as Date Table

## Anomaly Detection Methodology

Applied two-layer anomaly detection:

1. **Statistical Duration Outlier:** Calculated 
   Mean + 2 Standard Deviations of transaction 
   duration across full dataset = 104.93 seconds. 
   ATM failed transactions average 117 seconds — 
   exceeding this threshold, flagging them as 
   statistically anomalous.

2. **Time-Series Spike Detection:** Calculated 
   overall baseline failure rate (16.06%) and 
   measured hourly deviation. Hours 10-13 showed 
   +3.6 percentage point deviation — identified 
   as anomalous peak windows.

## 📌 Business Recommendations Summary

| Priority | Finding | Recommendation |
|---|---|---|
| High | ATM 21.12% failure | Increase monitoring, audit hardware |
| High | Peak hour spikes | Deploy auto-scaling alerts |
| High | 24-month flat trend | Structural root cause investigation |
| Medium | ATM 117s timeout | Reduce threshold to 45 seconds |
| Medium | RuPay 19.73% failure | Escalate SLA review with provider |
| Low | Student segment 20.59% | Implement low-balance SMS alerts |


## 🖼️ Dashboard Preview

| Page         | Preview |
|--------------|---------|
| 🏠 Home       | [Home](Images/Home.jpeg) |
| 📊 Executive      | [Executive](Images/Executive.jpeg) |
| 💰 Failure    | [Failure](Images/Failure.jpeg) |
| 📦 Location  | [Location](Images/Location.jpeg) |
| 📣 Transaction Profile  | [Transaction Profile](https://github.com/SENTHAMILAN27/Transaction_analytics/blob/01f567bd5b949b9abb6be5cc1efa84dfa0e51a1e/Images/Transaction%20Profile.jpeg)
| 🧠 Anomly | [Anomaly](Images/Anomaly.jpeg  )|
| Recommendation|[Recommendation](Images/Recommendations.jpeg)

## 👤 Author
**Senthamilan A** — Data Analyst  
LinkedIn Profile URL :  https://www.linkedin.com/in/senthamilan27/
