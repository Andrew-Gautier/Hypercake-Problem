# Hypercake and other Combinatorial Experiments in multiple languages

This repository contains solutions to the **hypercake problem**, a generalization of the classic pancake (2‑D) and cake (3‑D) cutting problems to an arbitrary number of dimensions. The maximum number of pieces obtainable from a *k‑dimensional hypercake* with `n` hyperplanar cuts is given by the sum of binomial coefficients:


$\text{hypercake}(n,k) = \sum_{i=0}^{k} \binom{n}{i}$

where 
$\(\binom{n}{i} = 0\) if \(i > n\).$


The code follows the specifications of two programming surveys assignments. It demonstrates different language paradigms, subprogram nesting, memoization, unit testing, and strict adherence to the combinatorial definitions.

---

## File Overview

| File | Language | Paradigm | Key Features / Survey Reference |
|------|----------|----------|----------------------------------|
| `HyperCake.js` | JavaScript | Scripting | `factorial` nested inside `combinations` inside `hypercake`; memoization of `factorial` with a non‑local cache. (Survey 1, step B) |
| `HyperCake.py` | Python | Scripting | Two versions: one commented recursive, one dynamic‑programming based. Illustrates alternative approaches. |
| `HyperCakePascal.pas` | Pascal | Domain‑specific | Straightforward implementation without nesting/memoization (as allowed). Reads user input. (Survey 1, step D) |
| `main(1).rs` | Rust | Compiled | `factorial`, `combinations`, `hypercake`; extensive unit tests covering all example cases from the survey; user input. (Survey 1, step C) |
| `Test.js` | JavaScript | – | Standalone test snippet for `combinations(6,5)`. |



---

## Theoretical Background

The hypercake problem is a classic combinatorial exercise. Each term \(\binom{n}{i}\) counts the number of regions created by the intersection of `i` cuts in `k` dimensions. Summing from \(i = 0\) to \(k\) yields the maximum number of pieces because each new cut can intersect all previous ones in a way that maximises new regions. The implementations strictly follow the mathematical definitions:

- `factorial(n)` returns $\(n!\) (with \(0! = 1\))$.
- `combinations(n, r)` returns $\(\binom{n}{r}\) for \(0 \le r \le n\)$, otherwise 0.
- `hypercake(n, k)` returns $\(\sum_{i=0}^{k} \binom{n}{i}\)$.

---


Surveys 1, 2, and 3 for CS 310: Principles of Programming Languages at West Virginia University
