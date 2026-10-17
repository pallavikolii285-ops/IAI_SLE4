# BFS vs DFS Search System

## Overview

The **BFS vs DFS Search System** is a Python-based project that compares
Breadth-First Search (BFS) and Depth-First Search (DFS) on the same
graph. The system searches from start node `0` to goal node `19` in a
graph containing 20 nodes.

The project focuses on comparing the algorithms using measured execution
time and the number of nodes expanded, while keeping the system
organized through a modular architecture.

## Objectives

-   Implement and compare BFS and DFS.
-   Use the same graph and start/goal nodes for a fair comparison.
-   Measure execution time and count expanded nodes.
-   Profile program execution using `py-spy`.
-   Organize the system into separate modules for configuration, search,
    measurement, and output.

## Algorithms Used

### Breadth-First Search (BFS)

BFS explores the graph level by level. It uses a **queue** to manage
nodes waiting to be explored.

### Depth-First Search (DFS)

DFS explores one path as far as possible before backtracking. It uses a
**stack** to manage nodes waiting to be explored.

Both algorithms use a visited set to avoid repeatedly exploring nodes
and a goal test to check whether the target node has been reached.

## Experimental Setup

-   **Graph size:** 20 nodes
-   **Start node:** `0`
-   **Goal node:** `19`
-   **Timing tool:** Python `timeit`
-   **Profiling tool:** `py-spy`
-   **Runs:** Three runs, with results compared

## Performance Results

  Metric                            BFS          DFS
  ------------------------ ------------ ------------
  Graph size                   20 nodes     20 nodes
  Start node                          0            0
  Goal node                          19           19
  Average execution time     9.45187 ms   4.35503 ms
  Average nodes expanded             20            6
  Goal found                        Yes          Yes

In this experiment, DFS had a lower average execution time and expanded
fewer nodes than BFS. This result applies to the tested graph and goal
position; it does **not** mean DFS will always be faster. Performance
can vary with graph structure and the location of the goal.

## Architecture

The system uses a modular design with these responsibilities:

1.  **Graph/Configuration Module** --- defines the graph and search
    settings.
2.  **Search Engine** --- runs BFS and DFS.
3.  **Performance Measurement** --- records execution time and related
    measurements.
4.  **Result/Output Module** --- presents the search results.

The architecture can be described using the four C4 levels:

-   **Context:** shows the user interacting with the search system.
-   **Container:** shows the main system modules.
-   **Component:** shows internal parts such as the BFS queue, DFS
    stack, visited set, goal test, and node counter.
-   **Code:** identifies functions and operations such as `bfs()`,
    `dfs()`, time measurement, average calculation, and result display.

## Tools and Technologies

-   Python
-   `timeit` for execution-time measurement
-   `py-spy` for profiling
-   Git and GitHub for version control and project hosting

## Project Learning Outcomes

-   Understand the working difference between BFS and DFS.
-   Compare algorithms using measured evidence.
-   Understand profiling and performance measurement.
-   Apply modular design principles.
-   Document architecture decisions using an Architecture Decision
    Record (ADR).

## Repository

GitHub repository: https://github.com/pallavikolii285-ops/IAI_SLE4

## Related SLE Work

-   **SLE-1:** Developed the search project.
-   **SLE-2:** Measured and profiled BFS and DFS performance.
-   **SLE-3:** Documented the system architecture using the full C4
    model.
-   **SLE-4:** Recorded and justified the modular architecture decision
    using performance results and architecture design.

## Conclusion

The project compares BFS and DFS on a shared 20-node graph and documents
the results alongside a modular architecture. DFS performed better in
the measured experiment, but the outcome may differ for other graphs.
Separating configuration, search, measurement, and output makes the
system easier to understand, test, maintain, and extend.
