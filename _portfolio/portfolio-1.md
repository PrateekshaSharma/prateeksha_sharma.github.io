---
title: "Beam Deflection Uncertainty Propagation"
excerpt: "Monte Carlo simulation of beam deflection with uncertain load and elastic modulus inputs.<br/><img src='/images/500x300.png'>"
collection: portfolio
---

## Overview

What happens to beam deflection when inputs aren't fixed but uncertain? Instead of plugging in single values, this project treats load *P* and elastic modulus *E* as random variables and runs a Monte Carlo simulation to capture the full range of possible deflection outcomes.

**Formula used:** δ = PL³ / (48 × E × I) — mid-span deflection for a simply supported beam under a central point load.

## Inputs

| Parameter | Distribution | Mean | Std Dev |
|-----------|-------------|------|---------|
| Load P | Normal | 50 kN | 7.5 kN |
| Elastic Modulus E | Normal | 200 GPa | 10 GPa |
| Span L | Fixed | 5.0 m | — |
| Moment of Inertia I | Fixed | 2.5 × 10⁻⁴ m⁴ | — |

## Results

| Metric | Value |
|--------|-------|
| Deterministic deflection | 2.6042 mm |
| Mean (Monte Carlo) | 2.6108 mm |
| Standard deviation | 0.4131 mm |
| 95th percentile | 3.2982 mm |
| 99th percentile | 3.6025 mm |

**[View on GitHub](https://github.com/PrateekshaSharma/stochastic-mechanics)**
