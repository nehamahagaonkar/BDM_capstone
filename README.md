# Enhancing Operational Efficiency and Workload Management in Sakhi Boutique

## 📌 Project Overview

This project was completed as part of the **Business Data Management** course under the **IIT Madras BS Degree Program**.

The objective of this project was to analyze and improve the operational efficiency of **Sakhi Boutique**, a home-based tailoring business run entirely by women who manage both entrepreneurship and household responsibilities.

The project uses **primary business data** collected from physical order registers to identify inefficiencies in workload management, delivery delays, backlog accumulation, and revenue variability, and proposes data-driven recommendations.

---

## 🏢 About the Business

**Sakhi Boutique** is a tailoring business located in **Chhatrapati Sambhaji Nagar, Maharashtra**.

### Business Characteristics:

* Home-based tailoring business
* Custom women’s garments
* Established in 2006
* Manual record-keeping system
* Operated entirely by women

---

## 🎯 Problem Statement

The boutique faced several operational challenges:

### 1. Limited Visibility into Order Backlog

* No real-time tracking of pending orders
* No clear measure of daily revenue vs costs
* Leads to over-commitment during high-demand periods

### 2. Inability to Anticipate Festive Demand

* Reactive planning instead of proactive planning
* No historical demand analysis
* Capacity overload during festivals

### 3. Unstructured Workload Allocation

* No workload caps per tailor
* Informal task assignment
* Causes tailor overload and delivery delays

---

## 📂 Dataset Description

The dataset was manually digitized from physical order registers.

### Time Period:

**May 2025 – October 2025**

### Total Orders:

**152 orders**

### Features in Raw Dataset:

* Order ID
* Order Date
* Expected Delivery Date
* Delivery Date
* Customer ID
* Item ID
* Quantity
* Material Cost
* Labour Cost
* Total Cost
* Net Earning
* Tailor Name
* Order Status

---

## 🧹 Data Preprocessing

Data preprocessing was performed to transform raw records into analyzable features.

### Cleaning Steps:

* Handled missing values
* Checked duplicate orders
* Ensured logical consistency in dates
* Cross-verified total cost calculations

### Outlier Detection:

Used **Interquartile Range (IQR)** method for:

* Material Cost
* Labour Cost
* Total Cost
* Delay Days

Outliers were retained because they represented genuine high-value festive orders.

### Feature Engineering:

Created new features such as:

#### Delay Days

```python
delay_days = delivery_date - expected_delivery_date
```

#### Days to Complete

```python
days_to_complete = delivery_date - order_date
```

#### Backlog

```python
backlog = cumulative_orders_placed - cumulative_orders_delivered
```

#### Other Features:

* Week Start
* Month
* Day Type
* Is Weekend
* Workload Category

---

## 📊 Exploratory Data Analysis

The following analyses were performed:

### 1. Daily Revenue Trend

Analyzed fluctuations in daily revenue.

### 2. Backlog Trend

Tracked pending workload over time.

### 3. Tailor Workload Distribution

Compared order distribution across tailors.

### 4. Demand Pattern Analysis

Used:

* 7-Day Moving Average
* Linear Forecasting

### 5. Workload vs Delivery Delay Analysis

Tailor-month level analysis to understand workload concentration effects.

---

## 📈 Key Insights

### 1. Delays are Structurally Driven

Delivery delays are caused more by workload concentration than individual skill.

### 2. Capacity Threshold Identified

Each tailor can handle approximately:

**18–20 orders per week**

Beyond this, delays increase sharply.

### 3. Predictable Demand Surges

Demand increases 2–3 weeks before festive peaks.

### 4. Cost Structure is Highly Predictable

Material + Labour explain:

**95% of total cost (R² = 0.946)**

This enables standardized pricing models.

### 5. Revenue Variability

Revenue fluctuates significantly due to garment complexity.

---

## 🛠 Tools & Technologies Used

* **Google Sheets / Excel** – Data cleaning and visualization
* **Python** (optional analysis)
* **Canva / PowerPoint** – Presentation design

---

## 📌 Recommendations

### 1. Implement Digital Order Tracking

Track:

* Order date
* Delivery date
* Tailor assigned
* Status
* Revenue

### 2. Set Workload Capacity Limits

Maximum:

**18–20 orders/week/tailor**

### 3. Proactive Festive Planning

* Booking cut-offs
* Advance slots
* Premium pricing for urgent orders

### 4. Cost Optimization

* Standardize material consumption
* Labour benchmarks

---

## 📉 Expected Impact

* Reduce average delay from **0.62 days** to **< 0.40 days**
* Improve revenue predictability
* Improve workload balance
* Increase customer satisfaction

---

## 📷 Visualizations Included

* Revenue Trend Graph
* Backlog Trend
* Tailor Workload Distribution
* Demand Forecasting Chart
* Workload vs Delay Scatter Plot
* Workload Category Delay Bar Chart

---

## 🚀 Learning Outcomes

This project helped me strengthen my understanding of:

* Business Data Management
* Data Cleaning
* Feature Engineering
* Exploratory Data Analysis
* Forecasting
* Business Insights Generation
* Operational Analytics

---

## 👩‍💻 Author

**Neha Mahagaonkar**

MSc Data Science Student
IIT Madras BS Degree Program

---

## 📜 License

This project is for academic and educational purposes.
