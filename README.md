[Availability Report.pdf](https://github.com/user-attachments/files/33228772/Availability.Report.pdf)
# 🛒 Product Availability Report | Power BI

### Bazooka Sales Drive 2023, Phase 3 | Field Sales Solutions Assessment

> A Power BI report that analyses store calls, product availability and sales outcomes from a field sales drive, built with data modelling and report design best practices.

![Report Preview]

<img width="1225" height="756" alt="Availability Report" src="https://github.com/user-attachments/assets/6120167f-d8ce-441d-93fc-ee4fc029dfba" />

<!-- Save a screenshot of the Visuals page at images/report_visuals_page.png -->

---

## 📌 Table of Contents

1. [Project Overview](#-project-overview)
2. [Business Problem](#-business-problem)
3. [Objectives](#-objectives)
4. [Dataset](#-dataset)
5. [Tools & Skills Used](#-tools--skills-used)
6. [Data Modelling Best Practices](#-data-modelling-best-practices)
7. [Report Building Best Practices](#-report-building-best-practices)
8. [Report Walkthrough](#-report-walkthrough)
9. [Key Insights](#-key-insights)
10. [Recommendations](#-recommendations)
11. [Blockers & How I Handled Them](#-blockers--how-i-handled-them)
12. [Lessons Learned](#-lessons-learned)
13. [Repository Structure](#-repository-structure)
14. [How to Use This Project](#-how-to-use-this-project)
15. [About Me](#-about-me)

---

## 🧭 Project Overview

This project was completed as an assessment for **Field Sales Solutions**. The data covers **calls made to stores** during the **Bazooka Sales Drive 2023 (Phase 3)**, including:

- The reasons calls were made
- The availability of products within each call
- Sales details at product level (products: Juicy Drop Blasts, Juicy Drop Gummies and Mix-Up's)

The report turns this field data into an interactive, two-view Power BI report: a **Visuals** page for quick insight and a **Tables** page for detailed record-level review.

---

## 💡 Business Problem

Field sales teams visit stores to get products ranged, stocked and sold. When products are not available on the shelf, or a sale is not made, revenue is lost and it is often unclear why.

The business needed to understand:

- How often are products **available** in stores?
- How many **cases were sold** compared to the number of calls made?
- **Why** are sales not being made?
- **Why** are products not available when the sales rep leaves the store (on exit)?
- **Where** are the stores located, and which retail groups do they belong to?

---

## 🎯 Objectives

- Measure **product availability** (Yes / No) by product
- Compare **cases sold against total calls** for each product
- Identify the main **reasons for no sale** and **reasons for unavailability on exit**
- Show the **geographic spread** of stores visited
- Build a clean, accessible and high-performing report following **Power BI best practices**

---

## 🗂 Dataset

| Detail | Description |
|---|---|
| **Source** | Field Sales Solutions assessment data (`[add link or note if shareable]`) |
| **Campaign** | Bazooka Sales Drive 2023, Phase 3 |
| **Data refresh date** | 25/01/2024 00:05:13 |
| **Key fields** | Product Name, Town, Postcode, Store Name, Retail Group, Availability Status, Availability Count, Total Calls, Total Cases Sold, Reason No Sale Made, Reason Not Available On Exit |

> **Note:** All dates in the supplied data were the same (**29 November 2023**), so no time series analysis was possible (see [Blockers](#-blockers--how-i-handled-them)).

---

## 🛠 Tools & Skills Used

- **Power BI Desktop** for modelling and report design
- **Power Query** for data cleaning and transformation
- **DAX** for measures and a custom date table
- **Star schema** data modelling
- **Bookmarks and buttons** for navigation and toggling views
- **Accessibility-minded design** (colour-blind friendly palette)

---

## 🏗 Data Modelling Best Practices

- ⭐ **Star schema** model used, the best-performing structure for Power BI.
- 🧮 **DAX formulae formatted** for easy readability and debugging.
- 🚫 **Auto date/time disabled** to reduce model size and allow more flexible date measures.
- 📅 **Custom date table created with DAX**, with more columns than the built-in date table.
- 📂 **Power Query queries organised into folders** for proper grouping.
- 💤 **Unused tables disabled from load** to prevent unnecessary loading and power usage.

---

## 🎨 Report Building Best Practices

- 🔖 **Bookmarks** toggle between visuals and tables for better accessibility and to suit personal preferences, including users with disabilities.
- 🎨 **Simple, consistent colours** keep the report readable and cater for users with colour blindness.
- 🔗 **Clickable company logo** that doubles as a button linking to the company website.
- 🕒 **Data refresh date** displayed at the top right so users can judge how current the data is.
- ⚡ **Limited number of visuals per page** to avoid performance issues.

---

## 🖥 Report Walkthrough

### Global controls
- **Slicers:** Product Name and Town
- **Date Last Refreshed** card
- **Navigation buttons:** *Visuals* and *Tables*

### Visuals page

| Visual | What it shows |
|---|---|
| **Product Availability Status** | Availability count by status (Yes / No) split by product, with total calls overlaid |
| **How Many Product Case Was Sold?** | Total cases sold versus total calls by product |
| **Why Was No Sale Made?** | Treemap of reasons a sale did not happen |
| **Why Are Products Not Available On Exit?** | Bar chart of reasons products were unavailable when leaving the store |
| **Number Of Store Per Town** | Map showing the geographic spread of stores visited |

### Tables page
- Availability status and count by product
- Total cases sold and total calls by product
- Reason no sale made, by total calls
- Product with reason not available on exit
- Store list with postcode, store name and retail group

---

## 🔍 Key Insights

### Availability
- Of the **50 availability records**, **33 were "No"** (about 66%) and **17 were "Yes"** (about 34%). Products were unavailable in roughly two out of three cases.
- The unavailable count was equal across all three products (**11 each**), so the problem is not limited to one product.
- Availability ("Yes") by product: **Juicy Drop Blasts 6, Mix-Up's 6, Juicy Drop Gummies 5**.

### Sales
- **50 cases sold** across **50 calls** in total.
- Sales were evenly spread by product: **Juicy Drop Blasts 17, Mix-Up's 17, Juicy Drop Gummies 16**.
- Calls logged against **Unavailable Products (33)** resulted in **zero cases sold**.

### Reasons no sale was made
| Reason | Calls |
|---|---|
| *(no reason recorded, "-")* | 25 |
| **No space available** | **14** |
| Tried before and did not sell | 6 |
| Already stocking | 2 |
| Stocks too many competitor brands | 2 |
| Other | 1 |

- Among calls with a recorded reason, **lack of shelf space is the leading barrier** (14 of 25).
- Six stores had tried the product before and it did not sell, a signal worth investigating around product appeal or placement.

### Reasons products are not available on exit
- The most common recorded reasons were **No Stock Available**, **Not Ranged In Store** and **Manager Refused**.
- A large share of records have no reason captured ("-"), which points to a data capture gap.

### Store footprint
- Stores visited are spread across the UK, with clusters in **London and the South East, the Midlands, the North West and Scotland (Glasgow and Edinburgh)**.
- The store list is dominated by **Independent – Convenience Stores**, with some **Symbol** group stores.

---

## ✅ Recommendations

1. **Address shelf space.** "No space available" is the top stated reason for no sale. Agree space or planogram placement before or during calls, and consider compact display units.
2. **Fix stock availability.** "No Stock Available" is a major reason for unavailability. Review distribution and replenishment so reps do not lose sales to supply issues.
3. **Improve ranging conversations.** Where products are "Not Ranged In Store" or the manager refused, equip reps with stronger pitch materials, promotions and sell-in incentives.
4. **Investigate the "tried before and did not sell" stores.** Understand whether the issue was pricing, location in store or product awareness.
5. **Improve data capture.** Make "reason" fields mandatory so blank values ("-") do not hide insight.
6. **Collect real dates on future phases** so trend and time series analysis becomes possible.
7. **Target high-opportunity areas** using the store map and retail group breakdown to focus on regions and groups with better ranging potential.

---

## 🚧 Blockers & How I Handled Them

| Blocker | How I handled it |
|---|---|
| **No time series analysis possible.** Every date supplied was 29 November 2023. | Focused the analysis on product, location and reason breakdowns instead of trends. |
| **Missing product (primary) keys.** | Brought them in as *unavailable products* under product name, using a dash ("-") to represent incomplete data. |
| **No specific deliverables were provided.** The BI developer had to define the scope. | Defined my own questions and visuals. In a real-life scenario I would run a proper **user requirements gathering** session first. |

---

## 🌱 Lessons Learned

- A well-structured **star schema** and tidy Power Query make everything downstream simpler.
- **Accessibility** (bookmarks, colour-blind friendly palette, minimal visuals) should be designed in from the start.
- Missing or blank data needs to be handled **transparently** rather than hidden.
- Without clear requirements, always **confirm the business questions** before building.
- **Replace the legacy map visual** with the newer Azure Maps visual, as Power BI is retiring the old one.

---

## 📁 Repository Structure

```
├── README.md
├── data/
│   └── availability_data.xlsx      # Dataset (or link to source)
├── report/
│   └── Availability_Report.pbix    # Power BI file
├── images/
│   ├── report_visuals_page.png
│   └── report_tables_page.png
└── Availability_Report.pdf         # PDF export of the report
```

> Update this structure to match your actual repository.

---

## ▶️ How to Use This Project

1. **Clone the repository**
   ```bash
   git clone https://github.com/<your-username>/<your-repo-name>.git
   ```
2. **Install Power BI Desktop** (free) from the [Microsoft website](https://powerbi.microsoft.com/desktop/).
3. **Open** `report/Availability_Report.pbix`.
4. If prompted, **update the data source path** under *Transform data → Data source settings*.
5. Use the **Product Name** and **Town** slicers to filter, and the **Visuals / Tables** buttons to switch views.

---

## 👤 About Me

**[Your Name]**
Data Analyst | Power BI | [Add other skills, e.g. SQL, Excel, Python]

- 💼 LinkedIn: [your-linkedin-url]
- 📧 Email: [your-email]
- 🌐 Portfolio: [your-portfolio-url]

---

⭐ If you found this project useful, consider giving the repo a star!
