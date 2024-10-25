# ACO_MTZ_CVRP Solver

This repository provides a Python-based implementation of two approaches to solve the **Capacitated Vehicle Routing Problem (CVRP)**:
1. **Ant Colony Optimization (ACO)** — A heuristic method inspired by ant foraging behavior.
2. **Miller-Tucker-Zemlin (MTZ) Formulation** — A mathematical approach utilizing linear programming to achieve optimal results.

## Capacitated Vehicle Routing Problem (CVRP)
CVRP aims to find the optimal route for a fleet of vehicles to deliver goods to various locations, ensuring the total demand at each location does not exceed the vehicle's capacity.

### Problem Formulation
Given:
- A set of locations (nodes) with specific demands.
- A vehicle with a fixed capacity constraint.
- A central depot from where each route begins and ends.

### Solution Methods
1. **ACO Approach**: Utilizes pheromone trails and probabilistic selection to build solutions iteratively.
2. **MTZ Approach**: Uses subtour elimination constraints and continuous variables to create a single, optimal solution.

## Code Structure and Explanation

### Dependencies
To run this code, you need:
- **Matplotlib** (for plotting, if required)
- **NumPy** (for mathematical operations)
- **PuLP** (for linear programming in MTZ)

### File Structure
1. **`ACO_MTZ_CVRP.py`**: Main script implementing both ACO and MTZ solutions for CVRP.
2. **`RegExService.py`**: Auxiliary file handling data extraction from the problem file.

### Parameters
The code allows configuration through command-line arguments:
- `alpha`, `beta`, `sigma`, `rho`, `theta`: Parameters specific to the ACO algorithm, which control pheromone influence, importance of edges, and pheromone evaporation.
- `fileName`: Problem data file (e.g., `E-n101-k14.txt`).
- `iterations`, `ants`: Control the ACO search process.

### Usage
Run the script from the command line:
```bash
python ACO-MTZ_CVRP.py -f <fileName> -a <alpha> -b <beta> -s <sigma> -r <rho> -t <theta> -i <iterations> -n <numberOfAnts>
