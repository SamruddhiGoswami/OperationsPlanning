# OperationsPlanning

# Executive Summary

The Vikings Division, a subsidiary of AK Enterprise, is headquartered in Pleasanton, CA. Vikings Products especially focus on producing five main products, namely Product 1, 2, 3, 4 and 5. The company had been facing multiple issues with respect to production.

The problem started right at the beginning. The forecasting models were not accurate and led to disproportionate production. Hence, a formal forecasting methodology was adapted based on the historical behavior of products. The next step was to tabulate the Master Production Schedule (MPS) for the end products. This forms the steppingstone toward ensuring least number of backorders and work-in-progress inventory. Keeping the MPS as the basis, an aggregate plan was computed based on the cost constraints. This was a bird&#39;s eye view of the production plan, giving estimated orders for associated estimated timelines.

The detailed planning started with the Material Planning Requirements (MRP) where the sub-products&#39; production plan was devised. This, again, would directly aid in reducing work-in-progress inventory and ensure that the production is completed within the expected lead time. To make sure the production deadlines are met, the next technique implemented was the Capacity Planning. This technique assesses whether the sub-products can be produced based on the existing capacity of the allocated resources. This also illustrated if the resources were being utilized to the correct measure.

Finally, the production schedule is developed. This required the routing information of the sub-products, the processing and setup time per sub-product, and the resources that could be used. The production schedule is an imperative step toward ensuring that the allocated resources are being utilized in most cost-effective manner and optimal timelines.

# 1.0 Introduction

## Background

The Vikings Division, a subsidiary of AK Enterprise, is headquartered in Pleasanton, CA. The company produces a variety of nutritional products, including adult medical nutrition supplements and pediatric infant formulas, as well as ancillary equipment.

Vikings Products especially focus on producing five main products, namely Product 1, 2, 3, 4 and 5. These products are sold directly to various distributors and wholesalers.

## Problem Statement

Over the years, the firm has experienced a loss of profit due to not meeting their demand on time (i.e., backorders) and maintaining high work-in-process (WIP) inventory resulting in long production times. This was due to many factors including inaccurate forecasting leading to incorrect production quantities of different types of products, running inappropriate lot sizes, and using no formal scheduling methodology.

## Objective

The objective of the project is to aid the Vikings Division in better planning their operations for the future. This can be achieved through establishing a formal method for forecasting the demand, planning the production based on BOM and capacity, and scheduling the production of the different product types. In essence, streamlining the overall operations at the Vikings Division in an effort to increase the chances of meeting the required product demand(s) on time.

# 2.0 Methods and Procedures

**Assumptions:**

1. The demand of the products depends on the category/type of the product and remains independent from the demand of other type of products. Hence, the forecasting methods for each product type will be tested and experimented independently
2. Undertime: This is defined as the amount of time that the allocated resources (workers, machines, etc.) remain idle and for which the costs must be incurred
3. Standard Setup Time/unit: For L4L and Fixed 2 period lot sizing techniques, the standard setup time per unit is calculated by taking the average of lot sizes for periods 21-25
4. Decimal values: All decimal values have been rounded up to the nearest whole number to account for real, physical resources which cannot be practically used partially and undertime is calculated based on their partial idle time
5. Resale value of machine(s): The cost of selling a machine is 50% and the company receives the leftover 50% as resale value of the machine(s)
6. Available time per machine per week: There are 2400 minutes available per machine per week

## Forecasting

Establishing a formal forecasting method ensures standardization in the forecasting methodology so that historical data can be easily compared to the new (future) data being recorded. The parameters in different forecasting models were computed to help in obtaining the minimum MAD which further ensured the accuracy of the forecast.
## Aggregate Planning

Computed the production and labor cost for each product type by implementing Level and Chase policies and selected the policy which gave the minimum cost.

## Master Production Scheduling

**Purpose** : To understand which products must be produced in what quantity and when
 Since no customer orders other than the forecasted ones have been provided, considering the maximum of the customer orders and forecasted orders, the forecasted orders are taken as the MPS for each product type. 

## Material Requirements Planning

**Purpose** : To understand which sub-products must be produced in what quantity and when

1. Compiled the level-wise Bill of Materials (BOM).
2. Calculated the Gross requirement for each sub-product based on the level-wise BOM.
3. Calculated net requirement and the corresponding planned order receipt and release(s) based on the Gross requirement, lot sizing technique, project available balance and lead time for each sub product.

## Capacity Planning

**Purpose** : To understand how many machines are needed to produce the required sub-products based on routings and BOM

1. Calculated the Standard total time/unit of sub-product using the given processing time/unit of sub-product and the setup time/lot, by converting setup time per lot to setup time/unit of sub-product.
2. Calculated downtime/work center/week and computed the total available time/work center/machine/week by subtracting the downtime.
3. Calculated the total time required/work center/week to produce all types of sub-products using the planned order release of sub products and the standard total time/unit of sub-product.
4. Calculated the average number of machines required using total available time/work center/ machine/week and total capacity required/work center/week for all sub-products.
5. Calculated the number of additional machines needed/work center. 
6. Finally calculated all costs – Regular costing of ordering all sub-products, Purchasing/resale cost of machine(s), undertime cost(s). 

**Note:** If the undertime cost if higher than the resale cost of machine(s) then it is beneficial to resale the machine at a much lower cost than to keep it running and pay for the idle machine(s). **Simulation and Scheduling**

**Purpose:** To determine the priority sequence that optimally utilizes the machines while requiring the minimum number of machines

Each sub-product manufactured in the same lot. The number of machines modeled time. Different lot sizes were experimented with using 25%, 50% and 75% of the existing lot size. The simulation was done by using ProModel with the results of the number of machines possible with their percentage utilization for available time of 2400 minutes. Downtimes for the stations are included in the clock of the locations.

# 3.0 Results

Based on the provided historical data for all product types, the behavior of each product type was obtained. This aided in the accuracy of the forecasting for the following weeks.

Forecasting model was chosen based on experimentation with models and obtaining the minimum MAD. Consequently, as a part of aggregate planning, Level and Chase strategies were implemented to calculate product related costs as seen in Table 1.

Table 1: Summarized chosen forecasting models with corresponding aggregate costs of products

| **Product type** | **Seasonality** | **Comments** | **Chosen forecasting model** | **α** | **β** | **γ** | **Policy** | **Product cost ($)** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | No | - | Exponential Smoothing (without trend) | 0.2 | - | - | Chase | 2013,68.83 |
| 2 | Yes | Decreasing trend | Seasonality with trend | 0.4 | 0.9 | 0.9 | Level | 170,532.88 |
| 3 | Yes | Increasing trend | Seasonality with trend | 0.1 | 0.2 | 0.8 | Level | 174,149.90 |
| 4 | No | Increasing trend | Linear Regression | - | - | - | Level | 243,518.80 |
| 5 | No | - | Moving average (8-week cycle) | - | - | - | Chase | 257,490.62 |

The computations of MRP and capacity planning (based on the routing and BOM), the required number of machines was calculated per work center. Consequently, additional number of machines needed per work center was estimated as seen in Table 2.

Table 2: Summarized machines needed based on Capacity planning of sub-products

| **Work Center** | **Average machines needed per work center** | **Machines per work center** | **Additional machines needed per work center** |
| --- | --- | --- | --- |
| 1 | 17 | 10 | 7 |
| 2 | 22 | 20 | 2 |
| 3 | 17 | 10 | 7 |
| 4 | 14 | 15 | -1 |
| 5 | 22 | 15 | 7 |
| 6 | 16 | 20 | -4 |
| 7 | 7 | 5 | 2 |


The scheduling of production was accomplished using the ProModel software. The First in first out (FIFO) scheduling was used to schedule the production plan. The utilization percentage obtained using FIFO was the highest and hence, this proved to be an efficient model.


# 4.0 Conclusions and recommendations

As per the aforementioned assumptions, the devised production plan gives a final, total cost of $41,414,653.47 to produce the forecasted demand for the weeks 21-25.

The measures taken to achieve the production plan address the primary causes of concern at the Vikings Division. With continuous management and leveraging the techniques used, Vikings Division should be able to manage their demand, contain costs and maintain necessary inventory as well as recoup their losses.

A major inference from the Promodel was understanding how to use multiple machines of the same work center to execute production parallelly and serially at the same time, i.e., using different lot sizes. It was found that with higher lot sizes, the utilization of the machines increased, but the average wait time remained constant. Hence, the recommendation is to schedule production with various lot sizes to get the optimal schedule which decreases the overall wait time and utilizes the machines in a balanced manner.
