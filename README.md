# BankingDashboard
Dashboard for analyzing banking datasets, including customer trends, transactions, and financial performance.
# 💼 Banking Dashboard

An interactive Power BI dashboard that empowers banks and financial institutions to make data-driven lending decisions by analyzing customer profiles, financial history, and key risk indicators.

---

## 📌 Problem Statement

Develop a basic understanding of risk analytics in banking and financial services and leverage data to minimize the risk of financial losses while lending to customers.

---

## ✅ Solution

This dashboard provides key insights into customer profiles using interactive visualizations. It allows banks to:

- Identify high-risk and low-risk customers.
- Analyze loan repayment potential based on customer data.
- Track deposits, credit card balances, and overall financial engagement.
- Make informed loan approval decisions.

---

## 🧰 Tools & Technologies

- Power BI (for data visualization)
- MySQL (for database management)
- Excel (for data preprocessing and exploration)
- Python (for data cleaning and transformation)

---

## 📊 Dataset Overview

**Table: Customer Financial Profile**

Each row represents a customer's financial snapshot including:
- Estimated Income
- Superannuation Savings
- Credit Card Balances
- Loans & Deposits
- Loyalty Classification (Jade, Gold, etc.)

**Key Columns:**
| Column Name | Description |
|-------------|-------------|
| `Estimated Income` | Annual income of the customer |
| `Amount of Credit Cards` | Number of credit cards held |
| `Credit Card Balance` | Total credit card debt |
| `Bank Loans` | Total loan value taken by the customer |
| `Bank Deposits` | Total deposits across all accounts |
| `Loyalty Classification` | Tier level (e.g. Jade, Gold) |

**Relationships (ERD):**
- `IAId` → Investment Advisor Table
- `BRId` → Bank Branch Table
- `GenderId` → Gender Lookup Table

---

## 🧹 Data Cleaning Steps

- Created `Engagement Days` column to calculate the number of days since the client joined.
- Created `Engagement Timeframe` to categorize client engagement periods.
- Binned income data into `Income Band` (Low, Mid, High).
- Calculated `Processing Fees` based on fee structure rules.

---

## 📐 DAX Measures in Power BI

- **Total Clients**: `DISTINCTCOUNT([Client ID])`
- **Bank Loan**: `SUM([Bank Loans])`
- **Business Lending**: `SUM([Business Lending])`
- **Total Deposit**: `[Bank Deposit] + [Savings Account] + [Foreign Currency Account] + [Checking Accounts]`
- **Total Fees**: `SUMX(Table, [Total Loan] * [Processing Fees])`
- **Engagement Days**: `DATEDIFF([Joined Bank], TODAY(), DAY)`

---

## 📈 KPIs Tracked

- **Total Clients**
- **Total Loans**
- **Business Lending**
- **Total Deposits**
- **Processing Fees**
- **Savings & Checking Account Balances**
- **Foreign Currency Holdings**
- **Credit Card Usage**

---

## 📍 Dashboard Pages

- **🏠 Home** – High-level summary and navigation
- **📉 Loan Analysis** – Loan data by gender, investor, and loyalty tier
- **💰 Deposit Analysis** – Insights into deposits and savings patterns
- **📊 Summary Dashboard** – Aggregated KPIs for quick decision-making

---

## 📚 Conclusion

Empowered by the latest data visualization techniques, this Power BI banking dashboard demonstrates how financial institutions can leverage data to:

- Minimize credit risk
- Optimize product offerings
- Enhance customer segmentation
- Streamline loan approval processes

---

## 🚀 Future Work

- **Investor Loan Overview**: Deep dive into individual investor loan amounts.
- **Client Distribution by Bank Type**: Compare client base across retail, private, and international banks.
- **Nationality-Based Loan Analysis**: Analyze loans segmented by nationality for demographic insights.
- **Account Type & Investment Patterns**: Explore investor behavior across different account types.

---


## 👤 Author

**Jyoti**  
*Data Analyst | Power BI Enthusiast*
