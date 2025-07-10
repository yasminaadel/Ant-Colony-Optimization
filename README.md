#  Ant Colony Optimization for the Traveling Salesman Problem (TSP)

## Overview

This project implements *Ant Colony Optimization (ACO)* to solve the *Traveling Salesman Problem (TSP)* for city graphs with *10 and 20 cities*. The algorithm mimics the behavior of real ants searching for food, utilizing pheromone trails to probabilistically find optimal or near-optimal paths.

Experiments were run using various configurations:

* *City counts*: 10 and 20 cities
* *Ant populations*: 1, 5, 10, and 20 ants
* *Iterations*: 50 per configuration

The project tracks *pheromone development* and *best tour evolution* over time and saves results in CSV files for analysis.

## Algorithm

### Ant Colony Optimization Components:

* *Pheromone Model*: Tracks pheromone levels between city pairs.
* *Decision Rule*: Ants select paths based on pheromone strength and heuristic (1/distance).
* *Update Rule*: After each iteration, pheromones are updated with evaporation and deposit rules based on tour cost.

## Problem Statement

The *Traveling Salesman Problem (TSP)* aims to find the shortest possible route that visits each city once and returns to the starting city.
This project uses ACO to approximate solutions to TSP for:

* A sparse graph of 10 cities (2–7 connections/city)
* A dense graph of 20 cities (12–17 connections/city)

## Visualizations

The following plots are generated:

* *Pheromone Development*: Average pheromone level per iteration for each configuration
<img width="1232" height="605" alt="image" src="https://github.com/user-attachments/assets/c15941d8-ec66-45a9-ab3d-427c317feca8" />
<img width="1232" height="611" alt="image" src="https://github.com/user-attachments/assets/77b03455-f192-4284-b499-68c3b7218339" />

* *Best Tour Cost Evolution*: How the best route cost improves over time
<img width="1060" height="689" alt="image" src="https://github.com/user-attachments/assets/314674b6-2a6f-48ef-8970-015aa4a19199" />
<img width="1056" height="676" alt="image" src="https://github.com/user-attachments/assets/7b764785-d0fa-42c2-9777-bd6de4afaad3" />


## How to Run

### Requirements

* Python 3.x
* Libraries: matplotlib, seaborn, pandas, numpy

### Running the Code

1. *Clone the repository*
2. Install dependencies:

bash
pip install matplotlib seaborn pandas numpy


3. Run the main script:
This will generate:

* CSV files of best tours and pheromone maps
* Plots showing algorithm performance

## Key Findings

* *More ants = better performance*: Larger ant counts led to quicker convergence and more optimal paths.
* *10-city problem*: Optimal solution found within 10–30 iterations with 10–20 ants.
* *20-city problem*: Required higher ant counts and longer iterations to reach near-optimal solutions.
* *Pheromone dynamics*: Fewer ants led to slower pheromone convergence and less exploration.

## References

* Dorigo, M., & Gambardella, L. M. (1997). Ant colonies for the travelling salesman problem. BioSystems.
* Wikipedia: [Ant colony optimization algorithms](https://en.wikipedia.org/wiki/Ant_colony_optimization_algorithms)
