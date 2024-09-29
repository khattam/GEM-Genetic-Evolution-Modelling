
# GEM: Genetic Evolutionary Modelling



## Overview
**GEM (Genetic Evolutionary Modelling)** is an advanced simulation framework designed to replicate and study the principles of natural evolution through computational methods. The project utilizes genetic algorithms (GA) to model complex evolutionary systems, making it a powerful tool for optimization, research, and machine learning applications.

GEM allows users to explore evolutionary computation, optimizing solutions to complex problems through mutation, crossover, and selection mechanisms. It's suitable for fields such as computational biology, artificial intelligence, algorithmic trading, and automated system design.

## Table of Contents
- [Features](#features)
- [Core Algorithms](#core-algorithms)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [License](#license)
- [Contributing](#contributing)
- [Contact](#contact)

## Features
- **Genetic Algorithm Framework**: Implements core genetic algorithms (mutation, crossover, selection) that can be customized for various use cases.
- **Chromosome Encoding**: Supports binary, integer, and real-value encoded chromosomes.
- **Fitness Function Optimization**: Users can define custom fitness functions to suit different problem domains.
- **Selection Algorithms**: Provides different selection techniques, including roulette wheel selection, tournament selection, and rank selection.
- **Crossover Operators**: Includes single-point, two-point, and uniform crossover methods for recombination of chromosomes.
- **Mutation Operators**: Supports both bit-flip mutation (for binary encoding) and Gaussian mutation (for real-valued genes).
- **Multi-threading Support**: Speeds up simulations by utilizing multi-threaded processing.
- **Visualization Tools**: Includes Python scripts for visualizing fitness progression over generations.

## Core Algorithms

### 1. Genetic Algorithm (GA)
The core of GEM is built around a classic genetic algorithm (GA) structure, which evolves a population of candidate solutions to optimize a fitness function.

- **Population Initialization**: The algorithm starts by creating a random population of candidate solutions (chromosomes). Chromosomes can be encoded in different formats depending on the problem (e.g., binary strings, integer arrays).

#### Selection
- **Roulette Wheel Selection**: Candidates are selected for reproduction with probabilities proportional to their fitness scores.
- **Tournament Selection**: A set of candidates is chosen at random, and the best-performing candidate is selected for reproduction.
- **Rank Selection**: Candidates are ranked by fitness, and their selection probability is based on their rank.

#### Crossover Operators
- **Single-Point Crossover**: A crossover point is selected randomly, and the genes from two parent chromosomes are swapped after that point.
- **Two-Point Crossover**: Two crossover points are selected, and the genes between the two points are swapped.
- **Uniform Crossover**: Each gene is swapped between two parents with a fixed probability.

#### Mutation Operators
- **Bit-Flip Mutation (Binary Chromosomes)**: Each gene has a small probability of being flipped (0 to 1 or vice versa).
- **Gaussian Mutation (Real-Valued Chromosomes)**: For real-valued genes, small random values are added, drawn from a Gaussian distribution.

#### Fitness Evaluation
The fitness function is problem-dependent and evaluates how well each candidate solution performs in relation to the optimization goal.

- **Elitism**: A technique where the best individuals are guaranteed to survive to the next generation, ensuring that the highest fitness is not lost.

### 2. Advanced Selection Mechanisms
- **Rank-Based Selection**: Candidates are ranked, and their selection probability is based on their rank, which reduces the impact of large differences in fitness.
- **Fitness-Proportionate Selection (Roulette Wheel)**: Candidates with higher fitness are more likely to be selected, but with a chance for lower-fitness candidates to reproduce, maintaining genetic diversity.

### 3. Customizable Fitness Functions
You can define various fitness functions for different types of optimization problems. Common examples include:
- **Minimization of Error**: In machine learning or optimization tasks, the fitness function could minimize an error metric, such as mean squared error.
- **Maximization of Utility**: In trading systems, the goal might be to maximize profit, where the fitness is proportional to the return on investment.
- **Constraint Satisfaction**: In scheduling or packing problems, the fitness function could reward solutions that meet all constraints.

### 4. Chromosome Representations
The GEM framework supports various chromosome encodings:
- **Binary Encoding**: Suitable for combinatorial optimization problems (e.g., knapsack problem, TSP).
- **Integer Encoding**: Used for problems where the solution space consists of integers (e.g., job scheduling).
- **Real-Value Encoding**: Useful for problems requiring continuous variables, such as function optimization.

## Installation

### Prerequisites
- **Java 8 or higher** (Main Application)
- **Git** (Version Control)
- **Python 3.x** (Optional for visualization tools)
- **Maven** (If you want to manage dependencies)

### Clone the Repository
```bash
git clone https://github.com/khattam/GEM-Genetic-Evolution-Modelling.git
cd GEM-Genetic-Evolution-Modelling
```


# Build the Project

If you are using Maven:

```bash
mvn clean install
```

Alternatively, you can use your IDE to directly import and build the project.

## Usage
After setting up the project, you can start running evolutionary simulations by executing the main class. Below is a basic example of how to run a simulation with custom parameters.

### Example Command:

```bash
java -jar GEM.jar --population 200 --generations 500 --mutation-rate 0.05 --crossover-rate 0.7
```

### Parameters:
- **--population**: The number of chromosomes in each generation.
- **--generations**: The number of generations to evolve.
- **--mutation-rate**: The probability of mutation occurring for each gene in a chromosome.
- **--crossover-rate**: The likelihood of performing crossover during reproduction.

## Example Python Script for Visualization:
If you want to visualize how fitness improves over generations, you can use the following Python script:

```python
import matplotlib.pyplot as plt

# Data: generations vs average fitness
generations = [1, 2, 3, ..., 500]
avg_fitness = [0.2, 0.25, 0.3, ..., 0.9]

plt.plot(generations, avg_fitness)
plt.xlabel('Generations')
plt.ylabel('Average Fitness')
plt.title('Fitness Progression Over Generations')
plt.show()
```

## Project Structure

```bash
GEM-Genetic-Evolution-Modelling/
├── src/                     # Source files for the application
│   ├── mainApp/             # Main Java classes
│   ├── Population.java      # Class handling population structure
│   ├── Chromosome.java      # Class defining a chromosome and its genes
│   ├── Selection.java       # Class defining selection algorithms
│   ├── Crossover.java       # Class for implementing crossover mechanisms
│   ├── Mutation.java        # Class defining mutation operators
├── ChromosomeFiles/         # Chromosome representations
├── grading_rubrics/         # Miscellaneous files from initial development
├── milestones/              # Project milestones and notes
├── README.md                # This README file
└── .gitignore               # Git ignore file for untracked files
```

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Contributing

We welcome contributions to the GEM project. To contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add some feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Create a new Pull Request.

For major changes, please open an issue first to discuss what you would like to change.

## Contact

Feel free to reach out if you have any questions or ideas!

- Email: khattam@rose-hulman.com
- GitHub: @khattam
