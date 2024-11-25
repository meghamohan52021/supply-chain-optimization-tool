# Supply Chain Optimization Tool

The **Supply Chain Optimization Tool** is a Python-based application designed to assist businesses in optimizing their supply chain operations. By minimizing transportation costs and ensuring that all demand points are satisfied, the tool uses linear programming techniques to efficiently solve transportation and network flow problems. It can process input data like production capacities, transportation costs, and demand at various destinations, ultimately providing businesses with the most cost-efficient routes and quantities for transporting goods.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Technologies Used](#technologies-used)
- [Contributing](#contributing)
- [License](#license)

## Overview

The **Supply Chain Optimization Tool** is designed to help companies reduce their operational costs by optimizing the transportation of goods across supply chains. The tool makes use of linear programming and network flow techniques to determine the most efficient shipping routes and quantities that satisfy production and demand constraints. This enables companies to reduce transportation expenses while meeting customer demands.

## Features

- **Cost Minimization**: Optimizes the transportation of goods, minimizing overall supply chain costs.
- **Linear Programming**: Utilizes libraries like **SciPy** to solve transportation problems and network flow issues.
- **Data Visualization**: Provides graphical visualizations of optimized transportation routes and supply chain networks.
- **Ease of Use**: The tool accepts input data for supply chain parameters and provides optimized, actionable results.


### Requirements:
- Python 3.x
- Google Colab (for running notebooks)
- Libraries: `SciPy`, `Matplotlib`, `NetworkX` , `Numpy`

## How the Code Works

The **Supply Chain Optimization Tool** uses **linear programming** to minimize transportation costs while ensuring that supply and demand constraints are satisfied. Here's an overview of how the code works:

### Input Data:
The user provides input data, including:
- **Transportation costs**: A matrix that defines the cost of transporting goods between different supply points and demand points.
- **Supply quantities**: The amount of goods available at each supply point.
- **Demand quantities**: The amount of goods required at each demand point.

### Optimization Process:
The optimization problem is formulated as a **linear programming model**, where the objective is to minimize the total transportation cost. The code performs the following steps:
- It sets up constraints to ensure that:
  - The total quantity shipped from each supply point does not exceed its available supply.
  - Each demand point receives at least the required amount of goods.
- The **SciPy** library (or **Google OR-Tools**) is used to solve the optimization problem by finding the optimal flow of goods from supply points to demand points.

### Objective Function:
The objective is to minimize the total transportation cost. This is done by calculating the cost for each possible transportation route and summing them up.

### Constraints:
The optimization model includes the following constraints:
- **Supply Constraints**: The total quantity shipped from each supply point must not exceed its available supply.
- **Demand Constraints**: The total quantity received at each demand point must meet or exceed the demand.

### Solution:
The optimal solution is calculated, providing the most cost-efficient way to transport goods across the supply chain. This minimizes transportation costs while satisfying both supply and demand constraints.

### Visualization:
The tool visualizes the optimized supply chain network using **NetworkX** and **Matplotlib**. It shows the flow of goods from supply points to demand points, with the quantities and transportation costs displayed on the graph.

## License
This project is licensed under the MIT License
