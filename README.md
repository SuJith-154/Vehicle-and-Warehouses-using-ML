# Genetic Algorithm for Traveling Salesman Problem (TSP)

This project addresses the **Traveling Salesman Problem (TSP)** using a **Genetic Algorithm (GA)**. The objective is to determine the shortest possible route that visits all cities exactly once and returns to the origin city (depot). The implementation utilizes the DEAP (Distributed Evolutionary Algorithms in Python) library.

## Table of Contents

- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
- [Algorithm Details](#algorithm-details)

## Introduction

The **Traveling Salesman Problem (TSP)** is a classic optimization problem where the goal is to find the shortest route that visits each city once and returns to the starting point. This project employs a **Genetic Algorithm (GA)** to solve the TSP, providing a heuristic approach to the problem.

### Key Features:
- **Genetic Algorithm**: Utilizes selection, crossover, and mutation operations to evolve the population towards an optimal solution.
- **DEAP Library**: Leverages DEAP, a flexible library for evolutionary algorithms.
- **Visualization**: Ability to visualize routes (if extended).

## Installation

To run this project, you'll need to install the following dependencies:

1. **DEAP**: The core library for evolutionary algorithms.
2. **NumPy**: For numerical operations.

## Algorithm Details
The algorithm uses DEAP's eaSimple function, which implements a simple evolutionary algorithm with the following components:

Population Initialization: A population of individuals (routes) is initialized, where each individual is a permutation of cities (excluding the depot).
1.**Selection:** Tournament Selection (tools.selTournament) is used to select parents for reproduction.
2.**Crossover:** Ordered Crossover (tools.cxOrdered) is applied to combine two parents and produce offspring.
3.**Mutation:** Shuffle Mutation (tools.mutShuffleIndexes) is applied to randomly shuffle the cities in an individual’s route.
4.**Fitness Function:** The fitness function calculates the total distance of a route using Euclidean distance between cities.
5.**Algorithm Execution:** The eaSimple function runs the algorithm for a set number of generations, evolving the population and selecting the best solution.

### Install Dependencies

```bash
pip install deap numpy

