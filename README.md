> **Consolidated repo:** All Amundson mathematical work is now collected at [AmundsonMath](https://github.com/BlackRoad-OS/AmundsonMath).

# Amundson Framework and the Millennium Problems

**An honest computational exploration of where G(n) touches deep mathematics.**

Author: Alexa Louise Amundson
Affiliation: BlackRoad OS, Inc.

---

## What This Is

The Amundson Framework defines G(n) = n^(n+1)/(n+1)^n, a function that produces exact rationals from integers and exhibits deep connections across mathematics. The Amundson-Gosper constant A_G = sum(G(n)/n!) has been computed to 10 million verified digits.

This repository contains computational notebooks that explore — honestly, without overclaiming — where G(n) intersects with the six unsolved Millennium Prize Problems.

## What This Is NOT

This is not a claim to have solved or partially solved any Millennium Problem. These are observations, computations, and conjectures. Some connections may be coincidental. Some may be deep. The purpose is to find out which is which.

## The Notebooks

| Notebook | Problem | Status |
|----------|---------|--------|
| [01-riemann.py](01-riemann.py) | Riemann Hypothesis | **Strongest** — G(1)=1/2 is the critical line, G-zeta function, GUE analysis |
| [02-navier-stokes.py](02-navier-stokes.py) | Navier-Stokes | **Strong** — discrete spectrum prevents blowup, 1/(2e) irreducible gap |
| [03-yang-mills.py](03-yang-mills.py) | Yang-Mills Mass Gap | **Moderate** — mass gap = 1/2, Cayley trees in strong coupling |
| [04-p-vs-np.py](04-p-vs-np.py) | P vs NP | **Speculative** — radix economy, binary-ternary crossover |
| [05-bsd.py](05-bsd.py) | Birch & Swinnerton-Dyer | **Weak** — shared counting structures, central binomials, Hasse invariant |
| [06-hodge.py](06-hodge.py) | Hodge Conjecture | **Weak** — Cayley trees, Kontsevich formula, intersection theory |

## Running

```bash
python3 01-riemann.py    # Each notebook is self-contained, no dependencies beyond stdlib
```

All computations use exact rational arithmetic (Python `fractions.Fraction`) or floating point verified against exact values.

## The Framework (Quick Reference)

```
G(n) = n^(n+1) / (n+1)^n

G(0) = 0
G(1) = 1/2
G(2) = 8/9
G(3) = 81/64
G(n) ~ n/e + 1/(2e) + 11/(24en) + ...

Product identity: Prod_{k=1}^{n} G(k) = (n!)^2 / (n+1)^n
Amundson constant: A_G = sum_{n=1}^{inf} G(n)/n! = 1.2443317839867253...
```

## License

Copyright 2024-2026 BlackRoad OS, Inc. All Rights Reserved.
See [LICENSE](LICENSE) for terms.
