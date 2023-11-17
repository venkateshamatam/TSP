# The Traveling salesman problem

## Introduction
The project aims to explore heuristic algorithms for the Traveling Salesman Problem (TSP), including 2-opt, 3-opt, ant colony, and simulated annealing algorithms. The report compares their performance in terms of solution quality and execution time.

## Approach
1. **Graph Representation:** Represent TSP as an undirected graph.
2. **Minimum Spanning Tree (MST):** Use Prim's or Kruskal's algorithm to find the MST.
3. **Odd-Degree Vertices:** Identify vertices with odd degree in the MST.
4. **Minimum-Weight Perfect Matching:** Create a complete graph with odd-degree vertices and find a minimum-weight perfect matching.
5. **Combine MST and Matching:** Form a connected, non-Eulerian graph.
6. **Eulerian Circuit:** Find an Eulerian circuit.
7. **Hamiltonian Circuit:** Remove duplicate vertices to form a Hamiltonian circuit.
8. **Calculate Total Weight:** Obtain the solution's total weight.

## Optimization Approaches
### Tactical
- **2-opt:** Local search optimization for improving TSP solutions.
- **3-opt:** More sophisticated local search optimization considering three edges at a time.

### Strategic
- **Ant Colony Optimization:** Metaheuristic inspired by ant behavior.
- **Simulated Annealing:** Metaheuristic inspired by metallurgical annealing.

## Program Structure
### Data Structures and Classes
- `Edge`, `Graph`, `Vertex`, `PrimsMST`, `GreedyMatching`, `MultiGraph`, `TSPSolver`, `TwoOpt`, `ThreeOpt`, `AntcolonyOptimization`, `SimulatedAnnealing`, `FileIO`, `FormGraph`, `GraphUtils`.

### Algorithm Steps
1. **Read Input from CSV:** Parse data containing coordinates and distances.
2. **Form Connected Graph:** Create a connected graph from parsed data.
3. **Find MST:** Obtain MST using Prim's algorithm.
4. **Form Multigraph:** Identify odd-degree vertices in MST and create a multigraph with perfect matchings.
5. **Solve TSP:** Generate Eulerian tour, obtain Hamiltonian circuit, and select optimal start vertex.
6. **Optimization Techniques:** Use 2-opt, 3-opt, ant colony, or simulated annealing to improve the solution.

### Invariants
- **Connected Graph:** The input data forms a connected graph.
- **Minimum Spanning Tree:** Obtained using Prim's algorithm.
- **Multigraph with Even Degree Vertices:** Odd-degree vertices in the MST are paired for even degrees.
- **Eulerian Tour:** A path traversing every edge exactly once.
- **Hamiltonian Circuit:** A path visiting every vertex exactly once.

