# Contribution Log --- BFS vs DFS Search System

## Project Details

-   **Project:** BFS vs DFS Search System
-   **Course:** 02AML204 --- Introduction to Artificial Intelligence
-   **Student:** Pallavi Vasant Koli
-   **PRN:** 25UAM037
-   **GitHub repository:**
    https://github.com/pallavikolii285-ops/IAI_SLE4

## Contribution Summary

  -----------------------------------------------------------------------
  SLE                                 Work documented
  ----------------------------------- -----------------------------------
  SLE-1                               Developed the BFS vs DFS search
                                      project.

  SLE-2                               Compared BFS and DFS on a 20-node
                                      graph, measured execution time and
                                      nodes expanded, and generated a
                                      `py-spy` profile.

  SLE-3                               Documented the architecture using
                                      the C4 Context, Container,
                                      Component, and Code levels.

  SLE-4                               Prepared an Architecture Decision
                                      Record (ADR) supporting a modular
                                      design and justified it using the
                                      measured results and architecture
                                      documentation.
  -----------------------------------------------------------------------

## SLE-2 --- Performance Analysis

The performance experiment used the same graph and search settings for
both algorithms:

-   Graph size: 20 nodes
-   Start node: `0`
-   Goal node: `19`
-   Measurement tool: Python `timeit`
-   Profiling tool: `py-spy`
-   Experiment: three runs, with results compared

  Metric                            BFS          DFS
  ------------------------ ------------ ------------
  Average execution time     9.45187 ms   4.35503 ms
  Average nodes expanded             20            6
  Goal found                        Yes          Yes

**Recorded observation:** DFS was faster and expanded fewer nodes in
this particular experiment. The result should not be generalized to all
graphs or goal positions.

## SLE-3 --- Architecture Documentation

The system architecture was described using the full C4 model:

-   **Context:** user interaction with the system and search results.
-   **Container:** graph/configuration, search engine, performance
    measurement, and result/output modules.
-   **Component:** BFS queue, DFS stack, visited set, goal test, and
    node counter.
-   **Code:** main functions and operations, including `bfs()`, `dfs()`,
    timing, average calculation, and result display.

The modular design separates responsibilities and helps make the project
easier to understand, test, and maintain.

## SLE-4 --- Architecture Decision Record

The documented decision was to keep BFS and DFS in a modular search
system using the same graph and start/goal nodes. This supports a fair
comparison and keeps configuration, search, measurement, and output
responsibilities separate.

### Alternatives considered

1.  **BFS only:** supports level-by-level search but does not provide a
    comparison with DFS.
2.  **DFS only:** removes the opportunity to compare its results with
    BFS.
3.  **Modular BFS and DFS system:** supports comparison and improves
    organization and maintainability.

### Trade-offs recorded

**Benefits** - Both algorithms can be tested with the same input. -
Separate modules are easier to understand and maintain. - Execution time
and expanded-node measurements provide practical evidence.

**Limitations** - Maintaining two algorithms requires additional code. -
Execution time can vary between runs. - Results from this 20-node graph
may not apply to every graph.

## AI Contribution Note

As documented in the SLE-4 report:

-   **AI tool used:** ChatGPT.
-   **AI assistance:** understanding the ADR format and organizing
    explanations of BFS/DFS results and the C4 model.
-   **Work reported as completed by the student:** running the program,
    collecting profiling results, generating the `py-spy` profile,
    checking the repository, and preparing the architecture
    documentation.

## Evidence and References

-   SLE-2: Profiling Report --- BFS vs DFS.
-   SLE-3: Architectural Design (Full C4 Model).
-   SLE-4: Final Viva & Architecture Decision Record (ADR).
-   GitHub repository: https://github.com/pallavikolii285-ops/IAI_SLE4

## Note

This log summarizes the work described in the SLE-4 report. Add actual
dates, commit hashes, or additional tasks only when they match the work
and Git history in the repository.
