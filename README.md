# The Anatomy of a Pandemic Highway: A Network Science Approach

Not all airports are equal. Not all hubs are dangerous in the same way. And the very thing that makes global aviation efficient is what makes it catastrophically fragile."*

This project provides a comprehensive Network Science analysis of the global air transportation infrastructure using the `inf-openflights` dataset. By exploring topological structures, network resilience, and contagion dynamics, this study investigates how structural characteristics of the global airport network govern both international logistics efficiency and global pandemic risks.

## Dataset Reference
* **Dataset Name:** OpenFlights Network (`inf-openflights`)
* **Source:** [Network Repository - OpenFlights](https://networkrepository.com/inf-openflights.php)

## Tech Stack & Key Libraries
* **Language:** Python
* **Network Analysis:** `NetworkX`, `ndlib` (Network Diffusion Library), `python-igraph`
* **Data Wrangling:** `Pandas`, `NumPy`
* **Visualisation:** `Matplotlib`, `Seaborn` (Styled in an academic-grade visual aesthetic)
* **Machine Learning:** `Scikit-Learn` (Spectral Clustering & Evaluation)

##  Core Methodological Acts

### Act 1: Network Characterisation & Topology
* Extracted the Largest Weakly Connected Component (WCC) consisting of **2,905 airports (nodes)** and **15,645 flight paths (edges)**.
* Evaluated degree distribution against synthetic mathematical models (**Erdős–Rényi** random graph and **Barabási–Albert** scale-free model).
* Calculated network metrics such as Density, Clustered Coefficients, and Avg Path Length.
* **Key Finding:** The real-world airport network exhibits scale-free features governed by a heavy-tailed power-law distribution ($`\gamma \approx`$ structural fit), confirming that a tiny elite group of hub airports exercises outsized structural control.

### Act 2: Centrality Analysis & "Single Points of Failure"
* Evaluated network properties through multiple centrality frameworks: **Degree Centrality** (volume), **Betweenness Centrality** (critical checkpoints), and **Closeness Centrality** (radial reach).
* Identified critical "Bridge Airports" that act as structural chokepoints between isolated topological communities.

### Act 3: Network Resilience (Attack Simulation)
* Simulated targeted cyber-physical attacks and random network failures.
* **Key Finding:** The global airport network demonstrates extreme robustness to random accidents but showcases a **catastrophic fragility to targeted disruption** when top-tier betweenness/degree hub nodes are systemically deleted.

### Act 4: Epidemiological Diffusion Modelling (SI, SIR, SIS)
Modelled viral spreading dynamics across international borders using standard compartment models.
Observed the "Epidemic Threshold" drop significantly on the scale-free OpenFlights network compared to random configurations, demonstrating how rapidly localised outbreaks escalate into global health crises.

### Act 5: Predictive Topology (Link Prediction)
* Implemented link-prediction algorithms to discover missing flight lines or forecast upcoming commercial routes using structural similarity indices.

---

## Key Conclusions
1. The global airport web is **scale-free**, meaning its efficiency relies entirely on key structural hubs.
2. High-volume hubs move traffic, but **high-betweenness bridge airports are the actual single points of failure** during systemic disruptions.
3. The network's epidemic threshold is dangerously low—any high-contagion pathogen will inevitably progress to a global pandemic stage through these predictable transmission highways.
