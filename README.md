<p align="center">
  <img src="assets/Princeton_AlgorithmsII_Header.jpeg" alt="Princeton Algorithms, Part II" width="100%" />
</p>

<h3 align="center">Advanced Graph Algorithms + String Processing & Compression (DSA Portfolio)</h3>

<p align="center">
  <img src="https://img.shields.io/badge/Language-Java-ED8B00?logo=openjdk&logoColor=white" alt="Java" />
  <img src="https://img.shields.io/badge/OOP-Encapsulation%20%7C%20Abstraction-2E7D32" alt="OOP" />
  <img src="https://img.shields.io/badge/DSA-Digraphs%20%7C%20Shortest%20Paths%20%7C%20Maxflow%20%7C%20Tries%20%7C%20Compression-1565C0" alt="DSA" />
  <img src="https://img.shields.io/badge/Princeton-Algorithms%20II-000000" alt="Princeton Algorithms II" />
  <img src="https://img.shields.io/badge/Textbook-Algorithms%20(4th%20Edition)-B71C1C" alt="Algorithms 4th Edition" />
  <img src="https://img.shields.io/badge/Focus-Algorithmic%20Optimization%20%26%20Clean%20APIs-6A1B9A" alt="Optimization & APIs" />
</p>

---

## 🎯 What this Repo Targets

This repository is my **hands-on implementation portfolio** for *Princeton Algorithms, Part II* using **clean OOP design in Java** and the advanced concepts from **Algorithms (4th Edition)**.

It demonstrates that I can:
- Implement **graph algorithms** that scale (BFS-based ancestry, rooted DAG validation)
- Model real problems using **shortest paths**, **network flow**, and **min-cut certificates**
- Build high-performance **string data structures** (tries + prefix pruning)
- Implement core **compression primitives** (Burrows–Wheeler transform + Move-To-Front)
- Write code with **defensive checks**, **clear APIs**, and **performance-aware design**

---

## 🧩 Course Modules (5) — What I Learned + Where It Shows Up

### Module 1 — Directed Graphs (WordNet + Shortest Ancestral Path)
**Core idea:** Model relationships as a digraph and answer “semantic distance” queries efficiently.  
**What it teaches:** rooted DAG validation, BFS-based shortest paths, and clean graph APIs.

**Where it appears in this repo**
- ✅ **WordNet** — builds a rooted DAG from synsets + hypernyms and validates acyclicity + single root  
- ✅ **SAP** — computes **Shortest Ancestral Path** between two vertices (or two sets) using BFS  
- ✅ **Outcast** — uses WordNet distances to identify the “least related” noun

**DSA concepts**
- Directed graphs, BFS, shortest paths in unweighted graphs, rooted DAG checks, graph query composition

**OOP concepts**
- Encapsulation of the graph + internal helpers, input validation, reusable query methods (`length`, `ancestor`, `distance`)

---

### Module 2 — Shortest Paths + Dynamic Programming (Seam Carving)
**Core idea:** Find an “optimal path” through a grid based on a cost function (energy).  
**What it teaches:** energy modeling, dynamic programming relaxations, and path reconstruction.

**Where it appears in this repo**
- ✅ **SeamCarver** — computes pixel energy and finds/removes vertical & horizontal seams
- ✅ Demos/Utilities — `PrintEnergy`, `ShowEnergy`, `PrintSeams`, `ShowSeams`, `ResizeDemo`, `SCUtility`

**DSA concepts**
- Grid-as-graph thinking, shortest path style relaxation (DP), backpointers, correctness + edge-case handling

**OOP concepts**
- Strong class API (`energy`, `findVerticalSeam`, `removeVerticalSeam`), validation of inputs/seams, clean internal state updates

---

### Module 3 — Network Flow (Maxflow / Mincut) — Baseball Elimination
**Core idea:** Convert a real constraint system into a flow network.  
**What it teaches:** maxflow/mincut reasoning, certificates of elimination, and reduction design.

**Where it appears in this repo**
- ✅ **BaseballElimination** — builds a flow network and runs maxflow to determine elimination + certificate set

**DSA concepts**
- Flow networks, Ford–Fulkerson, min-cut interpretation, reductions from “real-world rules” → graph model

**OOP concepts**
- Data modeling (`ST` keyed by team), clear public methods (`isEliminated`, `certificateOfElimination`), defensive validation

---

### Module 4 — Tries + Backtracking Search (Boggle)
**Core idea:** Search a huge space fast by pruning early.  
**What it teaches:** trie prefix checks, DFS/backtracking, and performance-first pruning.

**Where it appears in this repo**
- ✅ **BoggleSolver** — finds all valid words using recursion + prefix pruning (`hasKeyWithPrefix`)
- ✅ Trie Implementations — `TwentySixWayTrie`, `TSTWithRSquareTrie`
- ✅ Extras — `BoggleBoard`, `BoggleGame` (interactive play)

**DSA concepts**
- 26-way tries, prefix pruning, backtracking DFS, adjacency constraints, dedup via sets

**OOP concepts**
- Separate “dictionary structure” from solver logic, clean scoring API (`scoreOf`), careful state handling (marked[][])

---

### Module 5 — String Processing + Compression (Burrows–Wheeler Pipeline)
**Core idea:** Transform data so it becomes more compressible.  
**What it teaches:** suffix arrays, Burrows–Wheeler transform, and move-to-front encoding.

**Where it appears in this repo**
- ✅ **CircularSuffixArray** — sorts circular suffixes (foundation for BWT)
- ✅ **BurrowsWheeler** — transform + inverse transform (stdin/stdout)
- ✅ **MoveToFront** — encoding/decoding with symbol reordering (classic compression primitive)

**DSA concepts**
- Suffix arrays, stable ordering, inverse transform reconstruction, encoding schemes, byte-level I/O

**OOP concepts**
- Small focused classes, clear encode/decode entry points, disciplined input/output contracts

---

## 📁 Assignment Index (Implementation)

### ✅ WordNet (Digraphs + BFS Ancestry)
- `WordNet.java`
- `SAP.java`
- `Outcast.java`

### ✅ Seam Carving (Energy + Optimal Path / DP)
- `SeamCarver.java`
- `PrintEnergy.java`
- `ShowEnergy.java`
- `PrintSeams.java`
- `ShowSeams.java`
- `ResizeDemo.java`
- `SCUtility.java`

### ✅ Baseball Elimination (Maxflow / Mincut)
- `BaseballElimination.java`

### ✅ Boggle (Tries + Backtracking + Pruning)
- `BoggleSolver.java`
- `TwentySixWayTrie.java`
- `TSTWithRSquareTrie.java`
- `BoggleBoard.java`
- `BoggleGame.java`

### ✅ Burrows–Wheeler Compression (Suffix Arrays + Transforms)
- `CircularSuffixArray.java`
- `BurrowsWheeler.java`
- `MoveToFront.java`

---

## ⚙️ How to Run (Typical Princeton Setup)

Most Princeton assignments use the **algs4** libraries (standard in the course tooling).

**Example compile**
```bash
javac -cp .:algs4.jar WordNet.java
```

**WordNet (example)**
```bash
java -cp .:algs4.jar WordNet synsets.txt hypernyms.txt
```

**SAP (example interactive)**
```bash
java -cp .:algs4.jar SAP digraph-wordnet.txt
```

**Seam Carving (example demo)**
```bash
java -cp .:algs4.jar ResizeDemo input.png 400 300
```

**Baseball Elimination**
```bash
java -cp .:algs4.jar BaseballElimination teams4.txt
```

**Boggle**
```bash
java -cp .:algs4.jar BoggleSolver dictionary-yawl.txt board4x4.txt
```

**Burrows–Wheeler + Move-To-Front (pipeline-style)**
```bash
# transform
java -cp .:algs4.jar BurrowsWheeler - < input.txt > bwt.bin

# inverse transform
java -cp .:algs4.jar BurrowsWheeler + < bwt.bin > output.txt
```

> On Windows, replace `:` with `;` in the classpath.

---

## 🧠 Why This Matters

This repo is not “toy code.”

It’s proof that I can:
- Reduce real problems to canonical models (digraphs, shortest paths, flows, tries)
- Implement algorithms with correctness + performance constraints
- Design clean Java APIs that are testable and maintainable
- Apply classic optimization patterns: **BFS**, **pruning**, **dynamic programming**, **min-cut certificates**, **string transforms**

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
