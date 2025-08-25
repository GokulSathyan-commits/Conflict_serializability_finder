# Precedence Graph Cyclicity Detection

## Overview
This project implements a directed graph to represent precedence relationships or dependencies between tasks, transactions, or events. It includes a cycle detection algorithm to detect cyclic dependencies, which indicate conflicts or deadlocks in scheduling or transaction processing.

## Key Features
- Efficient graph representation using Python's `defaultdict` for adjacency lists.
- Directed edge insertion to model precedence constraints.
- Cycle detection using Depth-First Search (DFS) and recursion stack tracking.
- Determines conflict serializability by checking if the graph contains cycles.

## Explanation of Class Methods

- **`__init__(self, vertices)`**  
  Initializes the graph with a given number of vertices. Sets up an adjacency list for graph edges and stores the total vertex count.

- **`add_edge(self, u, v)`**  
  Adds a directed edge from vertex `u` to vertex `v`, representing a precedence or dependency relation.

- **`is_cyclic(self, v, visited, rec_stack)`**  
  Recursive helper method that performs DFS from vertex `v` to detect cycles. Tracks visited vertices and recursion stack to identify back edges indicating cycles. Returns `True` if a cycle is found, `False` otherwise.

- **`has_cycle(self)`**  
  Iterates over all vertices and uses `is_cyclic` to check if any cycle exists in the graph. Returns `True` if the graph is cyclic, else `False`.

## Usage
1. Define the number of vertices (nodes) in the graph.
2. Use `add_edge(u, v)` to add directed edges from node `u` to node `v`.
3. Run `has_cycle()` to check for any cycles in the graph.
4. The example script demonstrates usage and prints whether a cycle is detected.

