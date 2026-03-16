# Fulfilment-Operations-Performance-Analysis
## Project Overview

This project analyses the operational performance of an e-commerce order fulfilment system to identify the drivers of late deliveries and assess operational risks associated with SLA breaches.

Using Power BI and Excel, the analysis explores the entire fulfilment process — from order processing to final delivery — and evaluates how operational variability across stages contributes to delayed orders.

The project simulates a real-world operations analyst scenario where a business reports increasing delivery delays and rising operational costs.

## Dashboard Preview

<img width="2194" height="1227" alt="Fulfilment performance overview" src="https://github.com/user-attachments/assets/8e84b8e8-bd43-478f-910b-dcaab5f1500d" />


## Business Problem

**The operations team observed:**

- Increasing number of late deliveries

- Rising operational costs

- Growing risk to customer experience

**Management wanted to understand:**

- Why orders are getting delayed

- Whether specific warehouses are underperforming

- Which stage of the fulfilment process contributes most to delays

- The financial impact of SLA breaches

## Key Objectives

1. Analyze overall fulfilment performance

2. Identify operational bottlenecks in the fulfilment pipeline

3. Evaluate SLA breach rates and revenue exposure

4. Determine whether delays are caused by specific warehouses or system-wide issues

5. Assess operational variability across fulfilment stages

6. Provide insights to improve process reliability

## Dataset

| Column                 | Description                                      |
| ---------------------- | ------------------------------------------------ |
| order_id               | Unique order identifier                          |
| order_date             | Date the order was placed                        |
| warehouse              | Warehouse fulfilling the order                   |
| processing_time_hours  | Time taken to process the order                  |
| shipping_time_hours    | Time taken for shipment to reach destination hub |
| delivery_time_hours    | Final delivery time to customer                  |
| order_value_gbp        | Revenue value of the order                       |
| customer_type          | New or returning customer                        |
| late_delivery          | Indicator of delivery delay                      |
| total_fulfillment_time | Total time from order placement to delivery      |

## SLA Definition

For the purpose of this analysis, a 72-hour fulfilment SLA was assumed, which is a common delivery promise in e-commerce logistics.

Orders exceeding 72 hours were classified as SLA breaches.

## Analytical Approach

The analysis was conducted in several stages.

### 1. KPI Analysis

Key operational metrics were calculated:

- Total Revenue

- Late Delivery Rate

- Revenue at Risk from SLA breaches

- Average Fulfilment Time

These KPIs provide an overview of operational performance and financial exposure.

### 2. Fulfilment Time Distribution

Orders were grouped into fulfilment time buckets:

- 0–40 hrs

  40–60 hrs

- 60–72 hrs

- 72–80 hrs

- 80–100 hrs

- 100+ hrs

This distribution revealed how close the fulfilment process operates to the SLA threshold.

### 3. Warehouse Performance Comparison

Fulfilment times were compared across warehouses to determine whether delays were location-specific.

**Result:**
Performance across warehouses was largely consistent, indicating the issue was system-wide rather than location-specific.

### 4. Stage-Level Operational Analysis

The fulfilment process was broken into three operational stages:

1. Order Processing

2. Shipping

3. Delivery

Average time for each stage was analyzed to understand how time is distributed across the process.

### 5. Variability Analysis

To understand operational instability, the standard deviation of each stage was calculated.
| Stage      | Avg Time (hrs) | Std Dev |
| ---------- | -------------- | ------- |
| Processing | 18.2           | 6.36    |
| Shipping   | 37.4           | 12.73   |
| Delivery   | 12.0           | 4.50    |

Shipping exhibited the highest variability, indicating greater unpredictability compared to other stages.

## Key Insights
### 1. High SLA Breach Rate

Approximately 26% of orders exceed the 72-hour SLA, representing a significant operational and customer experience risk.

### 2. Revenue Exposure

Late deliveries account for approximately £22.6K of revenue, highlighting potential risks related to customer dissatisfaction and retention.

### 3. Fulfilment Process Operates Close to SLA Threshold

Most orders are fulfilled within 40–72 hours, leaving a small buffer against the SLA limit.

This makes the system highly sensitive to operational variability.

### 4. No Single Warehouse Is Responsible

Performance across warehouses is largely consistent, indicating that delays are not driven by a specific location.

### 5. Shipping Is the Most Unstable Stage

Shipping shows the highest variability (~12.7 hours) compared with processing and delivery.

This suggests that shipping introduces the greatest uncertainty into the fulfilment process and increases the likelihood of SLA breaches when delays accumulate across stages.

## Tools Used

**Power BI –** 
Data modelling and dashboard development

**Excel -**
Exploratory data analysis and statistical calculations

**DAX -** 
KPI calculations and operational metrics

## Business Recommendations

Based on the analysis, the following actions could reduce SLA breaches:

### 1. Reduce Shipping Variability

Investigate shipping logistics, carrier reliability, and routing processes.

### 2. Increase Operational Buffer

Target reducing average fulfilment time from ~67.7 hours to closer to 60 hours, creating greater tolerance for operational variability.

### 3. Implement Exception Handling

Introduce systems to flag and prioritize orders approaching the SLA threshold.
