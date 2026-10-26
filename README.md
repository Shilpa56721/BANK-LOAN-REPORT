# 🏦 Bank Loan Report – Power BI Dashboard

An interactive **Power BI** dashboard that analyzes a bank's loan portfolio. It tracks lending volume, repayment performance and borrower risk, so stakeholders can quickly see how the loan book is performing and where the risk sits.

---

## 📌 Table of Contents
- [Project Overview](#-project-overview)
- [Objectives](#-objectives)
- [Repository Structure](#-repository-structure)
- [Dataset](#-dataset)
- [Key Metrics (KPIs)](#-key-metrics-kpis)
- [Dashboard Views](#-dashboard-views)
- [Tools & Technologies](#-tools--technologies)
- [How to Use](#-how-to-use)
- [Key Insights](#-key-insights)
- [Future Improvements](#-future-improvements)
- [Author](#-author)

---

## 📖 Project Overview

Banks need to monitor how much they lend, how much they collect back, and how many loans go bad. This project turns raw loan data (`financial_loan.csv`) into a Power BI report that answers questions such as:

- How many loan applications are we receiving, and how much are we funding?
- How much money has been collected from borrowers?
- What share of loans are **good** (Fully Paid / Current) versus **bad** (Charged Off)?
- Which states, purposes, loan terms and borrower groups drive the most volume and the most risk?

---

## 🎯 Objectives

- Build a clear summary of the overall loan portfolio.
- Separate **Good Loans** from **Bad Loans** and compare their key numbers.
- Analyze trends over time (monthly / quarterly).
- Break down lending by geography, loan purpose, term, employment length and home ownership.
- Give decision-makers a quick, filterable view of lending performance.

---

## 📂 Repository Structure

```
BANK-LOAN-REPORT/
├── BANK LOAN REPORT.pbix    # Power BI dashboard file
├── financial_loan.csv       # Source dataset (~7.4 MB)
└── README.md                # Project documentation
```

---

## 🗃️ Dataset

**File:** `financial_loan.csv` (~7.44 MB)

The dataset contains loan-level records covering borrower details, loan terms, and repayment status. Typical fields include:

| Category | Fields |
|---|---|
| **Identifiers** | `id`, `member_id` |
| **Borrower profile** | `emp_title`, `emp_length`, `home_ownership`, `annual_income`, `address_state` |
| **Loan details** | `loan_amount`, `term`, `int_rate`, `installment`, `grade`, `sub_grade`, `purpose`, `application_type` |
| **Risk indicators** | `dti` (debt-to-income ratio), `verification_status`, `total_acc` |
| **Dates** | `issue_date`, `last_payment_date`, `next_payment_date`, `last_credit_pull_date` |
| **Outcome** | `loan_status`, `total_payment` |

> 📝 *Update this table if your column names differ from the above.*

---

## 📊 Key Metrics (KPIs)

| KPI | Description |
|---|---|
| **Total Loan Applications** | Count of all loan applications received |
| **Total Funded Amount** | Total money lent out to borrowers |
| **Total Amount Received** | Total payments collected from borrowers |
| **Average Interest Rate** | Mean interest rate across loans |
| **Average DTI** | Mean debt-to-income ratio of borrowers |
| **MTD / MoM Trends** | Month-to-date values and month-over-month change for the KPIs above |

### Good Loan vs. Bad Loan

| | Good Loan | Bad Loan |
|---|---|---|
| **Loan status** | Fully Paid, Current | Charged Off |
| **Tracked** | Application %, applications, funded amount, amount received | Application %, applications, funded amount, amount received |

---

## 🖥️ Dashboard Views

The Power BI report is organized into three pages:

1. **Summary** – Headline KPIs, good vs. bad loan comparison, monthly trend, and a loan status grid.
2. **Overview** – Breakdown by month, state, term, employment length, loan purpose and home ownership.
3. **Details** – A drill-down table of loan-level records for deeper investigation.

> 📸 *Add dashboard screenshots here, for example:*
> ```md
> ![Summary Dashboard](images/summary.png)
> ![Overview Dashboard](images/overview.png)
> ```

---

## 🛠️ Tools & Technologies

- **Power BI Desktop** – data modeling, visuals and interactivity
- **DAX** – measures and KPI calculations
- **Power Query** – data cleaning and transformation
- **CSV** – source data format

---

## 🚀 How to Use

### Prerequisites
- [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (Windows)

### Steps
1. **Clone the repository**
   ```bash
   git clone https://github.com/Shilpa56721/BANK-LOAN-REPORT.git
   cd BANK-LOAN-REPORT
   ```
2. **Open** `BANK LOAN REPORT.pbix` in Power BI Desktop.
3. If prompted that the data source can't be found, go to **Home → Transform data → Data source settings**, and point the source to your local copy of `financial_loan.csv`.
4. Click **Refresh** to reload the data.
5. Use the slicers and filters to explore the dashboard.

---

## 💡 Key Insights

> 📝 *Replace these placeholders with the actual findings from your dashboard.*

- Total applications received: **XX,XXX**, with **$XX M** funded and **$XX M** collected.
- Good loans make up about **XX%** of applications; bad loans about **XX%**.
- The highest lending volume comes from **[state]** and the most common loan purpose is **[purpose]**.
- Longer loan terms and higher grades (e.g., **[grade]**) show a **[higher/lower]** charge-off rate.
- Lending peaked in **[month/period]**.

---

## 🔮 Future Improvements

- Add predictive modeling for default risk.
- Add drill-through pages by borrower segment.
- Automate data refresh from a live database.
- Publish the report to Power BI Service for sharing.

---

## 👩‍💻 Author

**Shilpa**
GitHub: [@Shilpa56721](https://github.com/Shilpa56721)

---

⭐ If you found this project useful, consider giving it a star!
