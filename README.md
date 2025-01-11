# Genetic Algorithm for Vehicle Routing Problem (VRP)

This project addresses the **Vehicle Routing Problem (VRP)** using a **Genetic Algorithm (GA)**. The objective is to determine the most efficient set of routes for a fleet of vehicles to serve a given set of customers while minimizing the total travel distance or time. The implementation utilizes the DEAP (Distributed Evolutionary Algorithms in Python) library.

## Table of Contents

- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
- [Algorithm Details](#algorithm-details)

## Introduction

The **Vehicle Routing Problem (VRP)** is a challenging optimization problem and a generalization of the Traveling Salesman Problem (TSP). The aim is to design the shortest possible routes for a fleet of vehicles that visit all customer locations while respecting constraints such as vehicle capacity and route length.

### Key Features:
- **Genetic Algorithm**: Utilizes selection, crossover, and mutation operations to evolve the population towards an optimal solution.
- **Multiple Routes**: Handles multiple vehicles with defined constraints like vehicle capacity.
- **DEAP Library**: Leverages DEAP, a flexible library for evolutionary algorithms.
- **Visualization**: Ability to visualize routes (if extended).


## Installation

To run this project, you'll need to install the following dependencies:

1. **DEAP**: The core library for evolutionary algorithms.
2. **NumPy**: For numerical operations.

# Evolutionary Algorithm for Routing Problem

## Algorithm Details
The algorithm uses DEAP's `eaSimple` function, which implements a simple evolutionary algorithm with the following components:

1. **Population Initialization:**  
   - A population of individuals (routes) is initialized, where each individual is a permutation of cities (excluding the depot).

2. **Selection:**  
   - Tournament Selection (`tools.selTournament`) is used to select parents for reproduction.

3. **Crossover:**  
   - Ordered Crossover (`tools.cxOrdered`) is applied to combine two parents and produce offspring.

4. **Mutation:**  
   - Shuffle Mutation (`tools.mutShuffleIndexes`) is applied to randomly shuffle the cities in an individual’s route.

5. **Fitness Function:**  
   - The fitness function calculates the total distance of a route using Euclidean distance between cities.

6. **Algorithm Execution:**  
   - The `eaSimple` function runs the algorithm for a set number of generations, evolving the population and selecting the best solution.

---

## Install Dependencies

To run the code, install the following dependencies:  

```bash
pip install deap numpy


