# Geometric Engine
**Rational Geometry for Modular 3D Construction**

**Series:** Mathematical Foundations for Universal Systems
**Author:** Carolina Johnson (CJ) — **Date:** April 2026
**License:** CC BY 4.0, Attribution required
**DOI:** https://doi.org/10.5281/zenodo.19490969
**ORCID:** https://orcid.org/0009-0002-8819-3347

---

## What This Does

Replaces three separate mathematical frameworks (Trigonometry, Heron's Formula, and the Pythagorean Theorem) with a single coordinate matrix. One set of arithmetic derives any triangle, its circumscribed circle, and its bounding square from a boundary span. No forced right-angle dependencies. No post-hoc correction. No floating-point drift introduced at the source.

---

## The Problem It Solves

Standard 3D pipelines treat every shape as an independent object requiring separate formulas. Non-right triangles are sliced into right-angled components to satisfy coordinate projection math. Each operation accumulates rounding error.

The Geometric Engine eliminates this by deriving all three figures from the same four-variable matrix. The triangle, the circle, and the square are not separate primitives. They are states of the same system.

---

## The Protocol

For any anchor boundary [a, d] with a < d:

```
a = b - (c / 2)      — Anchor: boundary start
b = (a + d) / 2      — Centroid: arithmetic midpoint
c = d - a            — Span: displacement between anchors
d = b + (c / 2)      — Boundary: boundary end
```

Any two variables determine the other two. The system is closed by arithmetic.

---

## The Delta Constant

```
Δ = b² + c² - d²
  = (5a - d)(a - d) / 4
```

| Condition | Δ | Triangle |
|-----------|---|----------|
| d = 5a | 0 | Right (equilibrium) |
| d < 5a | < 0 | Obtuse |
| d > 5a | > 0 | Acute |

---

## The Full Cycle

From the same matrix:

```
SSP Matrix  =>  Triangle  =>  Circumcircle  =>  Bounding Square
```

**Circumcenter via rational partitioning:**
```
x  = (b² + c² - d²) / (2c)
y  = √(b² - x²)
Xc = c / 2
Yc = (b² - xc) / (2y)
R  = √((c/2)² + Yc²)
C  = (22/7) · 2R
D  = 2R
```

No trigonometry required. No Heron's formula. One square root at the end.

---

## Repository Contents

| File | Description |
|------|-------------|
| `README.md` | This file |
| `SSP Modular.pdf` | Full technical paper (English) |
| `Base Simétrica.pdf` | Full technical paper (Spanish) |
| `index.html` | Geometric Engine — live interactive tool |

**Live Demo:** https://semanticdrift.github.io/Rational-Geometry-in-Modular-3D/

---

## Citation

```
Johnson, C. (2026). Geometric Engine: Rational Geometry for Modular 3D Construction.
Series: Mathematical Foundations for Universal Systems.
SemanticDrift. DOI: https://doi.org/10.5281/zenodo.19490969
```

---

## Dependencies

| Framework | DOI |
|-----------|-----|
| SSP: Completing the Pythagorean Theorem | https://doi.org/10.5281/zenodo.19447063 |
| Law of Admissibility (R = 4) | https://doi.org/10.5281/zenodo.18993233 |
| The origami Principle | https://doi.org/10.5281/zenodo.18293884 |

Full publication list: https://www.semanticshift.net

---

## License

© 2026 Carolina Johnson (CJ)
Licensed under Creative Commons Attribution 4.0 International (CC BY 4.0)
Attribution required. https://creativecommons.org/licenses/by/4.0/
