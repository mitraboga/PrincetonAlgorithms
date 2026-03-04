<p align="center">
  <img src="assets/Princeton_AlgorithmsI_Header.jpeg" alt="Princeton Algorithms, Part I" width="100%" />
</p>

<h3 align="center">Object-Oriented Java + Core Data Structures & Algorithms (DSA Portfolio)</h3>

<p align="center">
  <img src="https://img.shields.io/badge/Language-Java-ED8B00?logo=openjdk&logoColor=white" alt="Java" />
  <img src="https://img.shields.io/badge/OOP-Encapsulation%20%7C%20Abstraction-2E7D32" alt="OOP" />
  <img src="https://img.shields.io/badge/DSA-Union--Find%20%7C%20Sorting%20%7C%20PQ%20%7C%20Kd--Tree-1565C0" alt="DSA" />
  <img src="https://img.shields.io/badge/Princeton-Algorithms%20I-000000" alt="Princeton Algorithms I" />
  <img src="https://img.shields.io/badge/Textbook-Algorithms%20(4th%20Edition)-B71C1C" alt="Algorithms 4th Edition" />
  <img src="https://img.shields.io/badge/Focus-Performance%20%26%20Clean%20APIs-6A1B9A" alt="Performance & APIs" />
</p>

---

## 🎯 What this Repo Targets

This repository is my **hands-on implementation portfolio** for *Princeton Algorithms, Part I* using **clean OOP design in Java** and the core concepts from **Algorithms (4th Edition)**.

It demonstrates that I can:
- Build **production-style APIs** (well-defined methods, edge-case handling, defensive checks)
- Implement **canonical data structures** from scratch (linked lists, resizing arrays, kd-trees)
- Apply **algorithmic thinking** (time/space complexity, pruning, heuristics, correctness)
- Write code that is **readable, testable, and scalable**

---

## 🧩 Course Modules (5) — What I Learned + Where It Shows Up

### Module 1 — Dynamic Connectivity (Union-Find)
**Core idea:** Track connectivity in a changing system efficiently.  
**What it teaches:** near-constant-time connectivity queries via **Union-Find** (Disjoint Set Union).

**Where it appears in this repo**
- ✅ **Percolation** — connectivity in an N×N grid using Union-Find + virtual nodes  
- ✅ **PercolationStats** — Monte Carlo simulation + confidence intervals to estimate percolation threshold

**DSA concepts**
- Union-Find, connected components, amortized efficiency

**OOP concepts**
- Clean APIs (`open`, `isOpen`, `isFull`, `percolates`)
- Encapsulation of internal grid/structures + input validation

---

### Module 2 — Stacks, Queues, and Linked Structures (ADTs)
**Core idea:** Build reusable **Abstract Data Types** with strict performance requirements.  
**What it teaches:** pointer manipulation, invariants, iterators, correctness under edge cases.

**Where it appears in this repo**
- ✅ **Deque** — double-ended queue using a doubly-linked list (O(1) add/remove both ends)
- ✅ **RandomizedQueue** — queue with random removal/sample, built with a resizing array
- ✅ **Permutation** — client program demonstrating randomized sampling of input

**DSA concepts**
- Linked lists, resizing arrays, amortized analysis, iterators

**OOP concepts**
- Generics (`<Item>`), `Iterable`/`Iterator`, exception discipline, separation of concerns (ADT vs client)

---

### Module 3 — Sorting as a Tool (Order, Comparators, and Geometry)
**Core idea:** Sorting unlocks faster algorithms and elegant solutions.  
**What it teaches:** comparator-based sorting, reducing brute-force search, and correctness-by-ordering.

**Where it appears in this repo**
- ✅ **BruteCollinearPoints** — baseline brute-force approach for collinear detection
- ✅ **FastCollinearPoints** — sorting-by-slope approach to reduce runtime
- ✅ **Point / LineSegment** — immutable “value-like” objects + comparable/comparator design

**DSA concepts**
- Sorting, comparators, computational geometry, avoiding duplicates, algorithmic optimization

**OOP concepts**
- `Comparable` + custom comparator (`slopeOrder()`), immutability patterns, small reusable objects

---

### Module 4 — Priority Queues + Heuristics (A* Search)
**Core idea:** Make smart choices first using **priority** + **heuristics**.  
**What it teaches:** modeling problems as graphs of states and solving with **A\*** (best-first search).

**Where it appears in this repo**
- ✅ **Board** — puzzle state representation + heuristics (Hamming/Manhattan)
- ✅ **Solver** — A* search using a MinPQ and backpointers to reconstruct the solution path
- ✅ **PuzzleChecker** — correctness checking utility

**DSA concepts**
- Priority queues, A* search, admissible heuristics, path reconstruction

**OOP concepts**
- Private `SearchNode` class, `Comparable` ordering for PQ, caching computed values, clean state API

---

### Module 5 — Symbol Tables + Geometric Search (2D Trees)
**Core idea:** Searching efficiently needs the right structure (not brute force).  
**What it teaches:** sets/maps, range searching, nearest neighbor queries, and pruning logic.

**Where it appears in this repo**
- ✅ **PointSET** — baseline solution using a set (correctness-first reference)
- ✅ **KdTree** — optimized 2D search with recursive space partitioning + pruning
- ✅ Visualizers: `KdTreeVisualizer`, `RangeSearchVisualizer`, `NearestNeighborVisualizer`

**DSA concepts**
- Symbol tables / sets, kd-trees, rectangles as pruning bounds, range/nearest queries

**OOP concepts**
- Node-based recursion, helper methods, clean public API (`insert`, `contains`, `range`, `nearest`)

---

## 📁 Assignment Index (Implementation)

### ✅ Percolation (Connectivity + Simulation)
- `Percolation.java`
- `PercolationStats.java`

### ✅ Deques & Randomization (ADTs + Iteration)
- `Deque.java`
- `RandomizedQueue.java`
- `Permutation.java`

### ✅ Collinear Points (Sorting + Geometry)
- `Point.java`
- `LineSegment.java`
- `BruteCollinearPoints.java`
- `FastCollinearPoints.java`

### ✅ 8 Puzzle (A* + Priority Queue)
- `Board.java`
- `Solver.java`
- `PuzzleChecker.java`

### ✅ 2D Range + Nearest Search (KdTree)
- `PointSET.java`
- `KdTree.java`
- `KdTreeVisualizer.java`
- `RangeSearchVisualizer.java`
- `NearestNeighborVisualizer.java`

---

## ⚙️ How to Run (Typical Princeton Setup)

Most Princeton assignments use the **algs4** libraries (standard in the course tooling).

**Example compile**
```bash
javac -cp .:algs4.jar Percolation.java
```

**Example run**
```bash
java -cp .:algs4.jar PercolationStats 200 100
```

> On Windows, replace `:` with `;` in the classpath.

---

## 🧠 Why This Matters

This repo is not “toy code.”

It’s proof that I can:
- Translate specifications into clean Java implementations
- Maintain invariants and correctness under constraints
- Choose the right structure for the right query
- Optimize solutions using classic algorithmic strategies (sorting, pruning, heuristics)

---

## 👤 Author

<p align="center">
  <b>Mitra Boga</b><br/>
  <a href="https://www.linkedin.com/in/bogamitra/">
    <img src="https://img.shields.io/badge/LinkedIn-bogamitra-blue?logo=linkedin&logoColor=white" />
  </a>
  <a href="https://x.com/techtraboga">
    <img src="https://img.shields.io/badge/X-@techtraboga-black?logo=x&logoColor=white" />
  </a>
</p>
