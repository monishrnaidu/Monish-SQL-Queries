# Project Description: School-Supplies-Supply-Chain-Optimization
This project aims to analyze the demand growth of School Supplies Co. and develop an optimized supply chain network to minimize costs.

### Introduction
School Supplies Co. experienced a 70% demand surge in 2020. To manage this growth, the company needs to optimize its supply chain network, including warehouse locations and shipping strategies. This report analyzes potential warehouse locations and shipping costs to minimize overall expenses.
  
## Problem Statement:
* School Supplies Co. is experiencing a rise in demand for their products. To meet this demand efficiently, they need to optimize their supply chain network
* Warehouse locations: Identifying the optimal locations to store inventory to minimize transportation costs and ensure timely deliveries.
* Shipping strategies: Determining the most cost-effective methods for shipping products to various customer zones.

### Methodology:
The project will follow a data-driven approach to analyze the problem and develop a solution. 
* Demand forecasting: Using historical sales data and market trends to predict future demand for different product categories and regions.
* Cost modeling: Calculating the costs associated with various supply chain options, such as warehouse storage, transportation, and fulfillment.
* Optimization modeling: Utilizing optimization techniques (potentially using software like PuLP or Pyomo) to identify the optimal configuration of the supply chain that minimizes total costs while meeting customer demand.

### Assumptions

* Costs (fixed & variable) for warehouses and Indian Post are constant.
* Demand increases by 70% from 2020 to 2023.
* Single linear inventory applies due to initial low demand (<2 million in 2020).
* Y variable indicates warehouse presence (1) or absence (0) at a location.
* Zone demand remains constant until delivery.
* Lead times for ordering, shipping, and delivery are not considered.
* Shipping costs, warehouse costs, and warehouse capacities are fixed.
* Inventory cost uses the 475,000Y + 0.165F equation for each facility (Y = 1 for used, 0 for unused).
* Optimization prioritizes fulfilling each zone's demand (not total demand) at the lowest cost.

### Analysis
The provided information details the cost analysis of having all warehouses located in Bengaluru for School Supplies Co. across the years 2020 to 2023, considering factors like warehouse costs, inventory holding costs, transportation costs via Indian Post and customer shipping charges. It also lays the groundwork for optimizing the supply chain network configuration for 2023.

* Part 1: Cost Analysis in Bengaluru (2020-2023)
   * Warehouse Cost: Includes fixed cost (based on warehouse size - small or large) and variable cost (based on the number of units shipped).
   * Inventory Holding Cost: Calculated based on a single linear inventory equation involving the existence of a warehouse and the number of units shipped to each destination.
   * Transportation Cost:
   * Indian Post Cost: Determined by the number of units shipped to each destination and the unit cost for that destination.
   * Customer Shipping Charges: Referred to as "Shipping charges" and calculated based on the number of units shipped to each destination.
   * The cost analysis demonstrates how these factors affect the total cost as the demand for school supplies increases year-over-year.
* Part 2: Supply Chain Network Optimization for 2023
   * Decision Variables:
   * Number of small warehouses (S_i) at each location (i).
   * Number of large warehouses (L_i) at each location (i).
   * Number of units shipped (X_ij) from location i to destination j.
   * Objective Function (Minimize Z):
* Represents the total cost, which is the sum of:
   * Warehouse cost (fixed and variable)
   * Inventory holding cost
   * Indian Post cost minus customer shipping charges (effectively transportation cost)
* Constraints:
   * S_i and L_i must be integers and binary (either 0 or 1, indicating presence or absence of a warehouse).
   * Y_i (binary variable representing warehouse presence) for each location.
   * Supply to each region (j) must meet the demand (D_j).
   * Capacity constraint: Ensures the total number of units shipped from a location doesn't exceed the capacity of warehouses present there (considering capacities of small and large warehouses).

Optimal warehouse locations: 
* The project will identify the ideal locations for warehouses, considering factors like demand distribution, transportation costs, and storage capacities.
* Reduced total cost: Implementing the optimized supply chain should lead to significant cost savings for School Supplies Co.
* Sensitivity analysis: The project will examine how the optimal solution changes under different scenarios (e.g., fluctuating demand, changes in fuel prices).

### Conclusion:
* This project establishes a foundation for School Supplies Co. to optimize their supply chain and adapt to future changes. 
* Future work might delve into incorporating lead times, dynamic pricing, and multi-echelon inventory models for even greater efficiency.



