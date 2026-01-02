# ⭐ Finite Structural Area Experiment (FSAE)

**Squaring the Circle via Structural Geometry**

![Open Standard](https://img.shields.io/badge/License-Open%20Standard-brightgreen) ![GitHub Repo stars](https://img.shields.io/github/stars/OMPSHUNYAYA/SSUM-Finite-Structural-Area-Experiment?style=flat&color=brightgreen)

**Deterministic • Exact Geometry • Finite Enumeration • Certified Counts • Browser-Verifiable**

---

## 🔎 **What is FSAE?**

The **Finite Structural Area Experiment (FSAE)** is a deterministic geometric study of how **finite square lattices** can be packed inside a circle under **strict, exact geometric constraints**.

FSAE is developed using structural principles from **Shunyaya Structural Universal Mathematics (SSUM)**, focusing on finite enumeration, exact certification, and deterministic geometric behavior.

FSAE evaluates configurations where **every square must lie fully inside the circle**, verified using an exact analytic rule applied to **all four square corners**.

There are:
- no approximations  
- no probabilistic sampling  
- no heuristic acceptance  

Every reported square count is **explicitly certified**.

---

## 🔗 **Quick Links**

### 📘 **Docs**
- [Concept-Flyer_FSAE_v1.3.pdf](Concept-Flyer_FSAE_v1.3.pdf)
- [FSAE_v1.3.pdf](FSAE_v1.3.pdf)

---

## 🎯 **Problem Statement — Squaring the Circle (Finite Case)**

Given:
- a circle of radius `R`
- squares of side length `s`

Determine the maximum number of squares `N` that can be placed such that:

`x_corner^2 + y_corner^2 <= R^2`

for **all four corners of every square**.

This experiment compares:
- axis-aligned square lattices
- rotated and translated square lattices  

under **identical certification rules**.

---

## 📐 **Certification Rule (Exact Geometry)**

A square is considered valid only if:

- all four rotated corners satisfy  
  `x^2 + y^2 <= R^2`

No tolerances are used beyond floating-point evaluation of analytic expressions.

There is:
- no partial acceptance  
- no boundary relaxation  
- no visual inference  

---

## 📊 **Primary Result Metric**

The primary result produced by FSAE is:

`N = number of squares fully contained in the circle`

All reported values of `N` are:
- discrete  
- deterministic  
- repeatable  
- certified  

---

## 📏 **Secondary Metric (Descriptive Only)**

For interpretability, area utilization is reported as:

`U = (N * s^2) / (pi * R^2)`

Utilization is **descriptive only** and does **not** affect certification.

---

## 📊 **Certified Results Snapshot (Example: R = 10, s = 1)**

For the reference configuration:

- `R = 10`
- `s = 1`

**Certification rule**

`x_corner^2 + y_corner^2 <= R^2`

**Certified results (strict 4-corner containment)**

**Axis-aligned lattice (best translation search)**  
`N_baseline = 277` → `N_certified = 279` (`DeltaN = +2`)

**Rotated lattice (bounded translation search)**  
`N_baseline = 277` → `N_certified = 279` (`DeltaN = +2`)

**Utilization (descriptive only)**

`U = (N * s^2) / (pi * R^2)`

**Important**

Certification binds to the **exact parameter tuple**:  
`(R, s, theta, dx, dy)`

Any change means **NOT CERTIFIED**.

**Structural note (interpretive)**

These results illustrate **structural plateaus**: improvements occur only when geometric alignments change, not through smooth parameter variation.

---

## 🧭 **Practical Benefits of FSAE**

FSAE provides several concrete benefits that are uncommon in classical geometric packing studies:

- **Exact certification**  
  Every reported square count is provably valid under a strict geometric rule, with no tolerance or approximation.

- **Deterministic reproducibility**  
  Identical inputs always produce identical results across machines and environments.

- **Visual and analytical agreement**  
  Browser-based visualization and analytical certification apply the same rule, enabling independent verification.

- **Baseline comparability**  
  Axis-aligned and rotated configurations are evaluated under identical constraints, enabling fair comparison.

- **Method reusability**  
  The same certification discipline can be applied to other shapes, containers, and finite geometry experiments.

- **Structural insight**  
  Reveals that packing improvements occur discretely due to alignment effects, not smoothly or asymptotically.

---

## 🔁 **Axis vs Rotated Lattices**

FSAE evaluates two lattice families:

**Axis-aligned lattice**
- `theta = 0`

**Rotated lattice**
- `theta > 0`, with bounded translations `(dx, dy)`

Both families:
- use identical certification rules  
- are evaluated deterministically  
- are directly comparable  

Observed improvements arise **only from geometry**, not rule changes.

---

## ⚖️ **Baseline Fairness (Translation Matters)**

A fair axis-aligned baseline is **not** defined by:

- `theta = 0, dx = 0, dy = 0`

A fair baseline is defined by:

- `theta = 0` with the **best translation** `(dx, dy)` within one lattice cell

Translation alone can increase `N` even when `theta = 0`.

FSAE certified tables reflect this fairness by separating:
- baseline counts  
- certified optimal counts  

---

## 🧠 **Structural Insight**

FSAE demonstrates that:

- optimal square counts are **discrete**
- improvements occur at **specific rotation plateaus**
- small angular changes often yield identical results
- translation effects are **bounded and periodic**

The experiment reveals **structured geometric behavior**, not continuous optimization.

---

## 🌐 **Browser-Based Verification**

Interactive verification for FSAE is hosted in the  
**SSUM Observatory — Case 08**.

The browser implementation:
- evaluates the same strict corner-containment rule  
- renders only certified squares  
- recomputes counts deterministically  
- enables independent external review  

**Visualization note**

When `apply_theta = 0`, squares are rendered axis-aligned for both datasets; different certified packings may therefore appear visually similar.

Certification, comparison, and correctness must be determined from verification output:
- `N`
- `bad_corners`
- `worst_margin`
- `R_min_needed`
- `PASS / FAIL`

—not from visual appearance.

---

## 🔗 **Implementation & Scripts**

The canonical implementation, datasets, and browser-verifiable certification logic for this study are maintained in the **Shunyaya SSUM Observatory**:

**Shunyaya SSUM Observatory (Canonical Repository)**  
https://github.com/OMPSHUNYAYA/ssum-observatory

**Case 08 — Finite Structural Area Experiment (Squaring the Circle)**  
https://ompshunyaya.github.io/ssum-observatory/08_finite_structural_area_experiment/

This repository serves as a **conceptual and certified case-study entry point**.  
The SSUM Observatory remains the **single source of truth** for executable artifacts, verification logic, and reproducible results.

---

## 📐 **Reproducibility & Determinism**

FSAE guarantees:
- identical results across executions  
- independence from machine, OS, or execution order  
- explicit failure when constraints are violated  
- no silent acceptance  

Given identical inputs `(R, s, theta, rotation_mode, centers)`, the same `N` is always produced.

---

## 🧾 **Certification Scope (Important)**

`PASS / FAIL` is a **certification result**, not an error indicator.

PASS or FAIL always refers to the **currently loaded square centers** evaluated under the **currently displayed parameters**.

The included demo datasets are certified only for:
- `R = 10`
- `s = 1`
- the dataset’s intended rotation setting

If any of the following are changed:
- `R`
- `s`
- `theta`
- rotation toggle behavior

then the same square centers are **not certified** for that geometry.

In that situation, **FAIL is expected** and correct.

---

## 🚫 **What FSAE Is Not**

FSAE is not:
- a numerical approximation  
- a Monte Carlo experiment  
- a heuristic packing algorithm  
- a visual estimation tool  
- a continuous optimizer  

All results are derived from **finite, explicit geometry**.

---

## 🧭 **Why FSAE Matters**

FSAE shows that even classical geometric problems reveal new structure when approached through:
- finite constraints  
- exact certification  
- deterministic enumeration  

It reframes “squaring the circle” as a **finite structural problem**, not an asymptotic or symbolic one.

---

## 📄 **Safety & Usage Notice**

This project is intended for:
- research  
- education  
- observation  
- structural geometry experimentation  

Not intended for:
- real-time control  
- safety-critical systems  

Failures are explicit.  
Silent errors are not allowed.

---

## 📄 **License — Open Standard (FSAE)**

Open Standard.

This project applies structural concepts inspired by **Shunyaya Structural Universal Mathematics (SSUM)**.  
Reference to SSUM is recommended for conceptual context but not mandatory.

No warranty; use at your own risk.  
No redistribution of third-party datasets unless permitted by their original licenses.

---

## 🏷 **Topics**

structural-geometry, finite-packing, square-in-circle, deterministic-geometry,  
certified-counts, exact-verification, reproducible-research, shunyaya, ssum

---

© The Authors of the Shunyaya Framework, Shunyaya Structural Universal Mathematics and Shunyaya Symbolic Mathematics  
