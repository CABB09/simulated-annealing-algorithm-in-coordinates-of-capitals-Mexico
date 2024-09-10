# simulated-annealing-algorithm-in-coordinates-of-capitals-Mexico


# Algorithm Analysis Project

## Project Overview

This project applies the **Simulated Annealing** algorithm to solve the **Traveling Salesman Problem (TSP)**, specifically focusing on finding the shortest route between the capitals of Mexico, including Mexico City. Simulated Annealing is used as an optimization technique to explore and identify global solutions, and the results are compared to those obtained using brute-force methods for smaller problem sizes. 

The project also includes a performance comparison based on error metrics and execution time between the two approaches.

### Author

**Carlos Alexis Barrios Bello**  
Email: zs23000636@estudiantes.uv.mx  
Master's in Artificial Intelligence  
IIIA Instituto de Investigaciones en Inteligencia Artificial, Universidad Veracruzana

---

## Table of Contents

1. [Introduction](#introduction)
2. [Theoretical Framework](#theoretical-framework)
   - [Simulated Annealing](#simulated-annealing)
   - [Traveling Salesman Problem](#traveling-salesman-problem)
3. [Activity](#activity)
4. [Results](#results)
5. [Conclusions](#conclusions)
6. [References](#references)

---

## Introduction

The goal of this project is to explore the **Simulated Annealing (SA)** algorithm for solving the **Traveling Salesman Problem (TSP)**. The TSP is a well-known problem in artificial intelligence where the objective is to find the shortest possible route that visits a set of cities exactly once and returns to the starting city. The algorithm was applied to Mexican capital cities, and the results were evaluated in terms of accuracy and computation time.

---

## Theoretical Framework

### Simulated Annealing

Simulated Annealing is an optimization algorithm inspired by the metallurgical process of heating and controlled cooling. In this analogy, the algorithm simulates a search for a global optimum by exploring random solutions and gradually reducing the likelihood of accepting worse solutions as it approaches a better solution.

The key idea is to avoid getting trapped in local optima by allowing occasional uphill moves (worse solutions) early in the process and focusing more on exploitation of promising regions as the temperature decreases. The algorithm follows a schedule where the temperature is gradually reduced to zero.

### Traveling Salesman Problem

The **Traveling Salesman Problem (TSP)** consists of finding the shortest possible route that visits a set of cities, with each city being visited exactly once before returning to the starting point. In this project, the TSP is formulated as finding the optimal route among the capital cities of Mexico.

The TSP can be modeled as a **Hamiltonian cycle**, a cycle that visits each vertex of a graph exactly once. The brute-force approach for solving TSP involves generating all possible permutations of city visits, which becomes computationally infeasible for larger numbers of cities due to the factorial growth in complexity.

---

## Activity

The main tasks in this project were as follows:

1. **Define the number of cities (N)**: Select a random subset of N cities from Mexico.
2. **Solve the TSP**: Use Simulated Annealing to find the shortest route among the selected cities.
3. **Compare with brute-force solution**: For small values of N (e.g., N < 10), compare the SA results with the optimal solution from brute-force enumeration. The error between the two results is calculated as \( e = d^* - d_s \), where \( d^* \) is the optimal distance and \( d_s \) is the distance found by SA.
4. **Execution time comparison**: Measure and compare the execution time (\( \Delta T \)) for both methods.
5. **Test with different values of N**: Perform experiments with at least three different values of N, including the case where N equals the total number of Mexican capital cities.
6. **Graphical display**: Display the optimal route graphically for each case.

---

## Results

The project was implemented in Python, and the following steps were followed:

- Random subsets of cities were chosen, and the TSP was solved using both brute-force and simulated annealing.
- Distances were calculated using Euclidean metrics between city coordinates, and the total distance of each route was computed.
- Results were displayed graphically, comparing the routes found by brute-force and simulated annealing.

### Example Graphs

The graphs below illustrate the solutions obtained for different values of N:

#### N = 3 (Randomly selected cities)

Graph for three randomly selected cities.

#### N = 5 (Randomly selected cities)

Graph for five randomly selected cities.

#### N = 8 (Randomly selected cities)

Graph for eight randomly selected cities.

#### N = 11 (Randomly selected cities)

Graph for eleven randomly selected cities.

### Full Set of Mexican Capital Cities

The final test was performed using all 31 capital cities of Mexico, including Mexico City. Due to the complexity and random selection of cities, slight variations in the routes were observed. Below are the graphical results of several attempts:

- **First attempt**: Suboptimal route.
- **Second attempt**: Improved, but still not optimal.
- **Third attempt**: Near-optimal route.
- **Optimal route (approximate)**: Final result showing the best approximation of the optimal route using simulated annealing.

The geographical distortions in the map are due to the negative coordinates and the curvature of the Earth, which would ideally be represented by geodesic lines rather than straight lines.

---

## Conclusions

This project successfully demonstrated the **Simulated Annealing** algorithm as an effective method for solving the **Traveling Salesman Problem (TSP)**. It was found that SA outperforms brute-force methods for larger numbers of cities, as brute-force approaches become computationally infeasible beyond N = 11 due to the factorial complexity.

For smaller values of N, the error between the SA solution and the brute-force solution was minimal, and SA's ability to find near-optimal solutions with significantly reduced computation time was highlighted.

The project also highlighted the limitations of brute-force methods and confirmed that for larger problem sizes, SA provides a practical and efficient alternative.

---

## References

- Russell, S., & Norvig, P. (2022). *Artificial Intelligence: A Modern Approach* (4th ed.).
- Ríos, Homero V., et al. (2013). *Análisis de Algoritmos*. Universidad Veracruzana, Mexico.

