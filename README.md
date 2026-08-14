# Spatial Extension of the Geometric Matrix

**Rational Foundations for Modular 3D Systems**

**Author:** Carolina Johnson (CJ)  
**Date:** April 2026  
**DOI:** [10.5281/zenodo.19447062](https://doi.org/10.5281/zenodo.19447062)  
**ORCID:** [0009-0002-8819-3347](https://orcid.org/0009-0002-8819-3347)

---

## Overview

This paper extends the planar Geometric Matrix into three-dimensional Euclidean space without introducing alternative volume definitions, continuous metric approximations, or floating-point drift.

By parameterizing orthogonal depth through a discrete grid parameter `k`, the framework embeds the planar rectangular envelope `A_envelope = c·y` directly into a deterministic 3D spatial envelope. It provides a compact 3D state vector `P = (b, c, k)` that recovers the planar interval boundaries, 2D projections, 3D spatial depth, and classical right-prism volume.

---

## The Problem It Solves

Standard 3D pipelines rely on continuous coordinate spaces, post-hoc floating-point corrections, and ungrounded external spatial parameters to project 2D geometries into 3D environments.

This framework solves that by constructing spatial depth `z = 2k²` directly from primary planar invariants via `k = c·y·d / b`. It establishes exact Euclidean equivalence `V(k) = c·y·k²` with classical right-prism volumes (`V_standard = A_planar · z`) while providing an immediate arithmetic classification across space:

| State | Result |
|-------|--------|
| **Equilibrium Right (`[1, 5]`)** | Integer altitude (`y = 3`), integer grid value (`k = 20`), exact integer volume (`V = 4,800`) |
| **Obtuse & Acute States** | Same general volume expression with irrational factors preserved through non-vanishing Delta invariants (`Δ ≠ 0`) |

---

## Core Framework

### 1. Planar Foundations

For any primitive interval state `[a, d]` with `a < d`:

| Quantity | Formula | Description |
|----------|---------|-------------|
| Centroid | `b = (a + d) / 2` | Arithmetic midpoint |
| Span | `c = d - a` | Displacement between boundaries |
| Delta | `Δ = b² + c² - d² = (5a - d)(a - d) / 4` | Structural invariant |

**Family Classification:**

| Family | Condition | `Δ` | Offset `x = Δ / 2c` | Altitude `y = √(b² - x²)` |
|--------|-----------|-----|---------------------|---------------------------|
| Equilibrium Right | `d = 5a` | `0` | `x = 0` | `y = b` |
| Obtuse | `d < 5a` | `< 0` | `x < 0` | `y = √(b² - x²)` |
| Acute | `d > 5a` | `> 0` | `x > 0` | `y = √(b² - x²)` |

---

### 2. 3D Spatial Extension

The rectangular envelope area `A_envelope = c·y` is extruded along an orthogonal depth axis `z = 2k²` using the intrinsic Matrix Grid Parameter:

k = (c · y · d) / b

The resulting constructive triangular-prism volume is:

V(k) = c · y · k²

Because `A_planar = ½·c·y`, this matches classical Euclidean extrusion identically:

V_standard = A_planar · z = (½·c·y)(2k²) = c·y·k²


---

## Representative States Comparison

Evaluating normalized states (`a = 1`) across all three families:

| Parameter | Obtuse `[1, 3]` | Equilibrium Right `[1, 5]` | Acute `[1, 9]` |
|-----------|:---:|:---:|:---:|
| Centroid `b` | `2` | `3` | `5` |
| Span `c` | `2` | `4` | `8` |
| Delta `Δ` | `-1` | `0` | `+8` |
| Offset `x` | `-1/4` | `0` | `1/2` |
| Altitude `y` | `3√7/4` | `3` | `3√11/2` |
| Grid Parameter `k` | `9√7/4 ≈ 5.953` | **`20`** (Integer) | `108√11/5 ≈ 71.639` |
| Depth `z = 2k²` | `567/8` | **`800`** (Integer) | `256,608/25` |
| Volume `V` | `1701√7/32 ≈ 140.638` | **`4,800`** (Exact) | `1,539,648√11/25 ≈ 204,257.389` |

---

## The Unified 3D State Vector

The minimal spatial state vector is:

P = (b, c, k)


From `P = (b, c, k)`, the complete 3D spatial geometry is deterministically reconstructed:

1. **Interval Boundaries:** `a = b - c/2`, `d = b + c/2`
2. **Planar Invariants:** `Δ = b² + c² - d²`, `x = Δ/2c`, `y = √(b² - x²)`
3. **Envelope & Depth:** `A_envelope = c·y`, `z = 2k²`
4. **Euclidean Volume:** `V = c·y·k²`
5. **3D Space Diagonal:** `D_3D = √(c² + y² + z²) = √(b² + c² - x² + 4k⁴)`

For the canonical `[1, 5]` state with `k = 20`, `z = 800`, yielding:

D_3D = 5√25601


---

## Repository Contents

| File | Description |
|------|-------------|
| `README.md` | This file |
| `Module 3D Matrix.pdf` | Full technical paper |

---

## Dependencies

| Framework | DOI |
|-----------|-----|
| The Geometric Matrix | [10.5281/zenodo.19490969](https://doi.org/10.5281/zenodo.19490969) |

Full publication list: [https://www.SemanticDrift.net](https://www.semanticdrift.net)

---

## Citation
```
Johnson, C. (2026). Spatial Extension of the Geometric Matrix: Rational Foundations for Modular 3D Systems. Series: Mathematical Foundations for Universal Systems. SemanticDrift. DOI: 10.5281/zenodo.19447062
```

---

License
© 2026 Carolina Johnson (CJ)
Licensed under Creative Commons Attribution 4.0 International (CC BY 4.0). Attribution required.
