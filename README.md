# AI Search Coursework – Artificial Intelligence

## Overview

This project, part of the second year **Artificial Intelligence** module at Durham University (2024–25 academic year), implements and compares two heuristic algorithms for the **Travelling Salesperson Problem (TSP)**.
Using the provided skeleton framework, the project develops both **basic** and **enhanced** implementations for two algorithms, **A*** Search and **Ant Colony Optimization (ACO)**, to generate efficient tours across 10 benchmark city files.

---

## Key Features

### A* Search (AlgA):

  * Basic implementation using standard heuristic cost estimation
  * Enhanced version introduces:

    * MST-based admissible heuristic for tighter lower bounds
    * Upper-bound pruning for faster search space reduction
    * Greedy tour completion with 2-Opt optimisation for improved final paths

### Ant Colony Optimization (AlgB):

  * Basic implementation follows the standard pheromone–heuristic balance approach
  * Enhanced version adds:

    * Candidate list restriction (L-nearest neighbours)
    * Local pheromone updates for intra-iteration diversification
    * Dynamic parameter scheduling for α (pheromone influence) and ρ (evaporation)

---

## Usage

1. Clone the repository and ensure the `city-files/` and `alg_codes_and_tariffs.txt` are located one directory above your user folder.
2. Run any algorithm file (e.g. `AlgAbasic.py`) from your user folder:

   ```bash
   python AlgAbasic.py AISearchfile012.txt
   ```
3. A tour file will be automatically generated in the same directory, containing the computed tour and its total cost.

---

## Repository Structure

```
├── city-files/                # Contains 10 city datasets (12–535 cities)
│   ├── AISearchfile012.txt
│   ├── ...
│   └── AISearchfile535.txt
│ 
├── tsp_algs/
│   ├── AlgAbasic.py           # Basic A* Search
│   ├── AlgAenhanced.py        # Enhanced A* Search 
│   ├── AlgBbasic.py           # Basic Ant Colony Optimization
│   └── AlgBenhanced.py        # Enhanced ACO Ant Colony Optimization
│ 
├── alg_codes_and_tariffs.txt  # Algorithm code references
├── skeleton.py                # Provided base code (framework)
└── validate_before_handin.py  # Algorithm validation code

```
