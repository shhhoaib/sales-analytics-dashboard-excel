================================================================================
  DATA ANALYTICS PROJECT 4 – COMPLETE DELIVERABLE
  Data Visualization | DecodeLabs Industrial Training Kit | Batch 2026
================================================================================

PROJECT OVERVIEW
----------------
This Excel workbook is the complete deliverable for Project 4: Data Visualization
(Optional Mastery Phase). The goal is to transform raw e-commerce data into
boardroom-ready visual insights that communicate findings clearly and drive
executive action.

Framework applied: The 3 Pillars from the DecodeLabs Project 4 PDF:
  Pillar 1 – The Architect  : Choose the right chart type for each business question
  Pillar 2 – The Editor     : Maximize data-ink ratio; eliminate chartjunk; use
                               direct labeling; apply color as a spotlight
  Pillar 3 – The Storyteller: Write action titles; structure via SCR framework;
                               answer "So What?" for every visualization

Source Data: Dataset_for_Data_Analytics_(1).xlsx
  - 1,200 orders | Jan 2023 – Jun 2025
  - 14 columns: OrderID, Date, CustomerID, Product, Quantity, UnitPrice,
    ShippingAddress, PaymentMethod, OrderStatus, TrackingNumber,
    ItemsInCart, CouponCode, ReferralSource, TotalPrice


================================================================================
WORKBOOK STRUCTURE – 10 SHEETS
================================================================================

SHEET 1: Raw Data
-----------------
Description : Clean copy of the original dataset with professional formatting.
              Alternating row shading, frozen header row, formatted date/currency.
Purpose     : Source of truth for all derived analyses in subsequent sheets.
Chart Used  : None (data table)

----

SHEET 2: Summary Statistics
----------------------------
Description : Executive KPI dashboard + two summary tables (Revenue by Product,
              Orders by Status).
Key KPIs    : Total Revenue, Total Orders, Avg Order Value, Top Product,
              Top Marketing Channel, Delivery Rate, Unique Customers.
Insight     : Provides a one-page executive overview before diving into details.
Chart Used  : None (summary tables + KPI cards)
Design Note : Color-coded KPI tiles follow the "spotlight rule" — each metric
              uses a distinct accent color to draw the eye.

----

SHEET 3: Monthly Revenue Trend (LINE CHART)
--------------------------------------------
Chart Type  : Line Chart — chosen because we are TRACKING A TREND OVER TIME.
              Per the Chart Selection Matrix in the PDF: "Showing a trend over
              time? → Line Chart (Connects continuous data points)."
Action Title: "Monthly Revenue Trend – Consistent Growth with Seasonal Peaks
               Across 2023–2025"
Data        : 30 months of monthly aggregated revenue, order count, avg order value.
SCR Applied :
  Situation   – Revenue has been growing steadily month over month.
  Complication– Q4 dips suggest inventory shortfalls during peak demand.
  Resolution  – Pre-stock high-demand SKUs before Q4 to capture peak revenue.
Key Insight : Revenue shows a consistent upward trajectory. Seasonal investment
              in Q4 restocking is recommended.

----

SHEET 4: Revenue by Product (HORIZONTAL BAR CHART)
----------------------------------------------------
Chart Type  : Horizontal Bar Chart — chosen because we are COMPARING VALUES
              ACROSS CATEGORIES (products). Per PDF: "Comparing values across
              categories? → Bar/Column Chart. Horizontal bars are best for long
              category labels."
Action Title: "Laptops & Monitors Drive the Most Revenue — Prioritize Stock &
               Marketing Investment"
Data        : 7 products ranked by total revenue, with orders and avg order value.
Key Insight : Laptops (~$207K) and Monitors (~$198K) dominate. Recommend
              increasing Laptop inventory and introducing accessory bundles.
Design Note : Single color used for all bars (no rainbow chartjunk). The data
              itself communicates the ranking.

----

SHEET 5: Order Status Analysis (COLUMN BAR CHART)
--------------------------------------------------
Chart Type  : Column Bar Chart — comparing discrete categories (order statuses).
              Color-coded category labels (green = delivered, red = cancelled,
              orange = returned) serve as direct labels per Pillar 2 guidance.
Action Title: "Cancellation & Return Rate Exceeds 40% — Immediate Fulfilment
               Review Required"
Data        : 5 order statuses with count, percentage share, revenue, avg value.
Key Insight : Combined Cancelled + Returned orders represent significant revenue
              leakage. Root cause investigation recommended.
Design Note : Status cells are color-coded (green/blue/yellow/red/orange) —
              using color as a spotlight to immediately signal good vs bad.

----

SHEET 6: Referral Source Analysis (COLUMN BAR CHART)
-----------------------------------------------------
Chart Type  : Column Bar Chart — comparing revenue across marketing channels.
Action Title: "Google & Instagram Are Top Revenue Channels — Referral Program
               Delivers Highest Avg Order Value"
Data        : 5 referral sources with orders, revenue, avg order value, % share.
Key Insight : Google and Instagram generate the majority of revenue. The Referral
              channel produces high-value, loyal customers. Email has untapped
              growth potential.

----

SHEET 7: Payment Method Analysis (COLUMN BAR CHART)
----------------------------------------------------
Chart Type  : Column Bar Chart — comparing payment method revenues.
Action Title: "Credit Cards Lead in Orders — Cash Customers Spend Significantly
               More Per Order"
Data        : 5 payment methods with orders, revenue, avg order value, % share.
Key Insight : Digital payments dominate volume. Cash orders are rare but carry
              a notably higher average — suggesting B2B or premium customers.
              Recommendation: Investigate and nurture this high-value segment.

----

SHEET 8: Coupon Code Impact (COLUMN BAR CHART)
-----------------------------------------------
Chart Type  : Column Bar Chart — comparing coupon performance by order volume.
Action Title: "SAVE10 Drives the Most Orders — Customers Without Coupons Spend
               Significantly More"
Data        : 4 coupon states (SAVE10, FREESHIP, WINTER15, No Coupon) with
              orders, revenue, and avg order value.
Key Insight : Coupon codes drive volume but attract price-sensitive customers.
              Non-coupon buyers have higher basket sizes. Evaluate net margin
              impact and consider shifting to loyalty-based strategies.

----

SHEET 9: Yearly Comparison (COLUMN BAR CHART)
----------------------------------------------
Chart Type  : Column Bar Chart — comparing annual revenue across 3 years.
Action Title: "2024 is Peak Revenue Year — 2025 Tracking Strong Despite Being
               Only Half Complete"
Data        : 3 years (2023, 2024, 2025) with orders, revenue, avg order,
              unique customers, and YoY growth % (color-coded green/red).
Key Insight : Revenue grew strongly 2023→2024. 2025 (Jan-Jun only) is already
              competitive. H2 2025 investment recommended to lock in record year.

----

SHEET 10: Product x Status Cross Analysis (CROSSTAB TABLE)
-----------------------------------------------------------
Chart Type  : Heatmap-style cross-tabulation table — showing COMPOSITION and
              RELATIONSHIPS between two categorical variables.
              No chart is added here because the data tells the story through
              the table itself (consistent with "one message per visual").
Action Title: "Laptop & Tablet Cancellations Are Highest — Chair & Monitor
               Returns Need Quality Investigation"
Data        : Cross-tab of 7 products × 5 order statuses with color-coded headers.
Key Insight : Laptops have highest absolute cancellations (stock/pricing issue).
              Chairs have disproportionate returns (product quality/description).
              Drill-down action required by product operations team.


================================================================================
DATA VISUALIZATION PRINCIPLES APPLIED (from Project 4 PDF)
================================================================================

1. CHART SELECTION MATRIX (Pillar 1 – The Architect)
   - Bar/Column Charts used for: comparing values across categories
   - Line Chart used for: tracking trends over time
   - Cross-tab table used for: investigating two-dimensional relationships
   - Pie charts deliberately AVOIDED (per "Strict Rule" in the PDF)

2. DATA-INK RATIO & CHARTJUNK (Pillar 2 – The Editor)
   - No 3D effects, no heavy gridlines, no decorative backgrounds
   - Direct data labels used where applicable
   - Color used as a spotlight (single dominant color per chart)
   - Legends minimized — categories labeled directly where possible

3. ACTION TITLES & SCR FRAMEWORK (Pillar 3 – The Storyteller)
   - Every sheet header states the CONCLUSION, not just the topic
   - Monthly Trend sheet uses full SCR (Situation → Complication → Resolution)
   - Each insight answers the executive question: "So What?"

4. AXIS INTEGRITY (Lie Factor = 0)
   - All bar charts start at zero
   - No truncated axes
   - No distortion of data-to-visual ratios


================================================================================
TECHNICAL DETAILS
================================================================================

Tool Used      : Python (pandas + openpyxl)
Source File    : Dataset_for_Data_Analytics_(1).xlsx (1,200 rows × 14 columns)
Output File    : Data_Analytics_Project4_Complete.xlsx
Sheets Created : 10
Charts Embedded: 8 (Line + Column + Horizontal Bar)
Date Created   : May 2026

Libraries:
  - pandas     : Data aggregation, groupby, cross-tabulation
  - openpyxl   : Excel workbook creation, formatting, chart embedding
  - numpy      : Numerical calculations (YoY growth, NaN handling)


================================================================================
HOW TO USE THIS FILE
================================================================================

1. Open Data_Analytics_Project4_Complete.xlsx in Microsoft Excel or LibreOffice.
2. Start with "Summary Statistics" for a quick executive overview.
3. Navigate to individual analysis sheets for deep dives.
4. Each sheet has:
   a. An ACTION TITLE (row 1) — the key conclusion
   b. An INSIGHT NOTE (row 2) — the SCR narrative / recommendation
   c. A DATA TABLE — the supporting numbers
   d. A CHART — the visual story
5. Cross-reference "Product x Status Cross" with "Order Status Analysis"
   to identify which specific products are driving cancellation/return issues.


================================================================================
CONTACT / PROJECT INFO
================================================================================

Course    : Data Analytics Industrial Training Kit
Project   : Project 4 – Optional Mastery Phase: Data Visualization
Provider  : DecodeLabs | www.decodelabs.tech | decodelabs.tech@gmail.com
Batch     : 2026

================================================================================
                        END OF README
================================================================================
