# Modelling-Simulation-and-Optimization
The shortest delivery routes are found using the A* search method, and these routes are then further refined using a heuristic technique. 

# We-Doo Last-Mile Delivery Optimization Project

## Overview

This project aims to optimize the location of warehouses for the "We-Doo" company, a startup focusing on last-mile delivery using electric bikes. The project uses simulations to evaluate various delivery center locations based on cost, time, and distance. Statistical methods such as ANOVA and F-statistics are employed to ascertain the significance of cost differences between potential warehouse sites. The study provides key insights to decision-makers to help select ideal fulfillment centers, thereby increasing the efficiency and profitability of last-mile delivery services.

## Introduction

"We-Doo" is a startup focused on optimizing last-mile delivery solutions using electric bikes. This project uses simulations to evaluate various delivery center locations based on parameters such as cost, time, and distance. The study involves generating map data, creating parcel data, finding the shortest delivery routes, and evaluating operational costs to identify the best warehouse locations.

## Datasets

- **Customer Data**: Locations of customers encoded as (x, y) coordinates.
- **Warehouse Data**: Potential warehouse sites encoded as vertices in the map graph.
- **Parcel Data**: Information about packages to be delivered on specific days.

## Project Structure

- **data/**: Contains the datasets used in the project.
- **notebooks/**: Jupyter notebooks demonstrating the analysis and modeling processes.
- **src/**: Source code for data preparation, modeling, and evaluation.
- **results/**: Generated results, including plots and model evaluation metrics.
- **README.md**: Project overview and instructions.

## Requirements

- Python 3.x
- Jupyter Notebook
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- NetworkX

Install the required libraries using:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn networkx
```

## Usage

### Step 1: Generating Map Data

Generate a sample map using the last four digits of the student ID (9340). The map consists of vertices (intersections) and edges (road segments). 

```python
# Generate map data
generate_map_data(student_id=9340)
```

### Step 2: Generate Parcel Data

Create data for packages to be delivered based on customer locations and delivery days.

```python
# Generate parcel data
parcel_data = generate_delivery_data(p=0.2, C=10, days=5)
```

### Step 3: Finding Shortest Path

Use the A* search algorithm to find the shortest path between two points.

```python
# Find shortest path
shortest_path = a_star_search(start, goal, graph)
```

### Step 4: Finding Shortest Delivery Route

Determine the optimal path from the delivery center to each customer location and back using a heuristic approach.

```python
# Find shortest delivery route
delivery_route = find_shortest_delivery_route(delivery_center, customer_locations)
```

### Step 5: Developing Event Graphs

Create event graphs for parcels, customers, drivers, and delivery centers to simulate the delivery process.

### Step 6: Model Verification

Verify the model by simulating package deliveries and comparing the results to real-world data.

### Step 7: Visualization and Statistics Summary

Visualize driver working hours, tour durations, and leftover packages using histograms and plots.

```python
# Visualize results
visualize_results(simulation_data)
```

### Step 8: Cost and Optimal Delivery Location

Calculate the average daily operating cost for each potential delivery center location and identify the optimal location.

```python
# Calculate costs and find optimal location
optimal_location = find_optimal_location(warehouse_locations, simulation_data)
```

## Results

The project includes detailed analysis and visualization of the simulation outcomes, such as driver working hours, delivery tour lengths, and leftover parcels. The statistical evaluation using ANOVA and descriptive statistics supports the findings, identifying the optimal warehouse location with the lowest operational cost.

## Evaluation and Future Work

While the current study shows consistent operational expenses across different sites, future work should focus on improving data quality, model complexity, and dynamic optimization techniques. This will help in better decision-making and resource allocation for "We-Doo."

