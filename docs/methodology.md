# Methodology

## Objective

The objective is to minimize total tardiness for jobs scheduled on identical parallel machines.

## Problem setting

The problem includes:

- A set of jobs
- A set of identical parallel machines
- Processing times
- Due dates
- A static and deterministic environment
- No preemption, cancellation, or job priority

## Genetic Algorithm design

The proposed GA includes:

### 1. Chromosome representation

Each chromosome represents a feasible schedule. Rows represent machines and genes represent jobs assigned to each machine.

### 2. Expanded initial population

The initial population is expanded to increase solution diversity.

### 3. Surrogate fitness function

The first stage uses the number of tardy jobs as a surrogate fitness function to locate promising regions.

### 4. Actual fitness function

The main objective is total tardiness.

### 5. Four mutation operators

- Two Genes Exchange Mutation
- Number of Jobs Mutation
- Flip Ends Mutation
- Flip Middle Mutation

### 6. Immigration operator

If no improvement occurs for a specified number of generations, the population is refreshed to reduce premature convergence.

### 7. Elitist selection

The best chromosomes are preserved for the next generation.

## Evaluation

The algorithm is evaluated using:

- Average total tardiness
- Standard deviation of total tardiness
- Number of times the optimal value is found
- Average time to the best solution
- Average number of generations
- Percentage deviation from the optimal value
