# Analysis of the Weisfeiler-Lehman Isomorphism Test

**Course:** Learning Graphs and its Applications  
**Institution:** Indian Institute of Technology Jodhpur  
**Date:** September 5, 2025  

---

## Project Description
This project presents an empirical study of the **1-Weisfeiler-Lehman (1-WL) graph isomorphism heuristic**.  
The experiment is divided into two main tasks designed to probe the algorithm's sensitivity to structural noise and its limitations in distinguishing structurally similar, non-isomorphic graphs. Using the **AIDS dataset**, we analyze the WL test's performance, fragility, and failure modes.

The final, detailed report can be found in **`report.pdf`**.

---

## Tasks Overview

### Task A: Noise and Robustness
This task investigates the sensitivity of the WL test to minimal structural changes.  
We selected the largest isomorphic group from the AIDS dataset and systematically generated **80 perturbed copies** by adding or removing a single random edge from each. We then analyzed:

- How many of the original isomorphic relationships were broken by this perturbation.  
- Whether any new, "accidental" isomorphic groups emerged from the set of perturbed graphs.  

### Task B: Is It Truly Isomorphic?
This task investigates the limitations of the 1-WL test, which is known to produce false positives ("WL-fakes").  
We identified several groups of graphs that the WL test marked as isomorphic and performed a deeper analysis to verify their true isomorphism using:

- **Structural Invariants:** Degree distribution, clustering coefficients.  
- **Global Invariants:** The multiset of edge betweenness centrality values, which captures global path structure.  
- **Exact Solvers:** The NetworkX implementation of the VF2 algorithm to find or disprove the existence of an explicit node-to-node mapping.  

---

## Dataset
The experiment uses the **AIDS dataset** from the **TUDataset** collection.  
It contains ~2,000 graphs representing molecular compounds, making it a valuable resource for testing graph algorithms on real-world, complex structures.  

---

## Setup and Installation

It is recommended to use a Python virtual environment to manage dependencies.

###  Clone the repository
```bash
git@github.com:champgithub06/graph-analysis-wl-experiments.git
cd graph-analysis-wl-experiments
```

### How to Run the Code
The entire experiment, including data loading, analysis for both tasks, and visualization generation, is contained in the **`[TASK_8_EXP_A].ipynb`** and **`[TASK_8_EXP_B].ipynb`**.ipynb  Jupyter Notebooks.  

To reproduce the results:
1. Open the notebook.  
2. Execute the cells sequentially.  
3. The code will automatically download the dataset, run the analyses, and save all visualizations as `.png` files in the root directory.  
