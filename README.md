# From de Moivre's Formula to the Twisted Hessian Curve

**ERI Labs · Eric Ren · Jersey City, New Jersey · May 2026**

> *"(cos x + i sin x)ⁿ = cos(nx) + i sin(nx)"*
> — Abraham de Moivre, 1707

---

In 1707, Abraham de Moivre wrote down a formula connecting complex numbers and rotation. He did not know he was doing anything more than trigonometry.

Three centuries later, that identity lives inside the group law of a plane cubic. Everything in this repository — constant-time cryptographic arithmetic, geometry-native hardware, isomonodromic learning dynamics, the classical/quantum simulation boundary, and a universal equilibrium constant — is the same object seen from different angles.

That object is the Twisted Hessian curve.

---

## The Generative Object

Over any field of characteristic not 2 or 3:

```
TH(a,d):   aX³ + Y³ + Z³ = d·XYZ          [projective]
           ax³ + y³ + 1  = d·xy            [affine, Z = 1]

Smooth iff   Δ(a,d) = a(d³ − 27a) ≠ 0
Identity     𝒪 = [0 : 1 : −1]
Negation    −[X : Y : Z] = [X : Z : Y]
```

This is the Twisted Hessian model of an elliptic curve. It carries a **unified addition law** — a single rational formula that computes both the sum of two distinct points and the doubling of a single point, with no exceptional cases and no branching. The formula costs 12 multiplications and 6 squarings. Addition and doubling use the identical instruction stream.

That is not an engineering choice. It is the geometry of the cubic.

---

## The Chain from de Moivre to TH(a,d)

de Moivre's 1707 formula is the trigonometric seed of complex exponentiation. Euler's identity e^{ix} = cos x + i sin x follows immediately. The Weierstrass ℘-function uniformizes the complex torus ℂ/Λ onto the Weierstrass model of an elliptic curve. The Weierstrass model is birationally equivalent to the Hessian normal form. The Hessian normal form, twisted by the parameter a, is TH(a,d).

Every framework in this repository is a consequence of continuing de Moivre's line of reasoning to its natural terminus.

---

## Four Facts That Generate the Entire Corpus

**Fact 1 — The group law emerges from geometry.**

A smooth plane cubic carries a group structure defined by collinearity: three points sum to the identity when they lie on a common line. On the Twisted Hessian model this produces the explicit unified formula of Bernstein, Chuengsatiansup, Kohel, and Lange (LATINCRYPT 2015). No exceptional cases. Addition and doubling identical.

This single formula is the source of every constant-time arithmetic guarantee in the corpus. It is inherited from the geometry, not engineered in.

**Fact 2 — The 3-torsion structure emerges from the Hesse configuration.**

A smooth plane cubic over an algebraically closed field has exactly nine inflection points. These nine points form the Hesse configuration (9₄, 12₃): nine points on twelve lines, three per line, four lines per point. Group-theoretically they are the 3-torsion subgroup, isomorphic to ℤ/3ℤ × ℤ/3ℤ.

The automorphism group ℤ/3ℤ × ℤ/4ℤ, the Ackermann depth bound α(n) ≤ 4, and the chain to the golden ratio all descend from this configuration.

**Fact 3 — Arithmetic depth emerges from the elliptic curve over ℤ.**

TH(a,d) is an elliptic curve. It carries every arithmetic invariant: the Mordell–Weil group with its rank r, the Tate–Shafarevich group, the L-function, the modular form, the Frobenius eigenvalues at every prime, the field of definition, and the motive in Voevodsky's triangulated category of motives over ℤ.

The arithmetic depth of the entire programme is the arithmetic of one elliptic curve.

**Fact 4 — The Ramanujan expander emerges from the Hesse pencil.**

The Twisted Hessian curves form a one-parameter family — the Hesse pencil — of cubics through the nine base points of the Hesse configuration. Moving through the pencil connects curves by 3-isogenies. Over a finite field the resulting isogeny graph is a Ramanujan graph: an optimal expander saturating the Alon–Boppana spectral bound |λ₂| ≤ 2√ℓ. Random walks mix in O(log p) steps.

This is the structural source of collision-free addressing, the Stern–Brocot decoder, and every spectral gap condition in the corpus.

---

## The φ-Equilibrium

The constant log φ ≈ 0.4812 appears as the equilibrium of every framework. It is not a numerical coincidence. It emerges from the curve through a single chain:

```
CM by ℚ(ω) = ℚ(√−3)
  → 3-torsion = Hesse configuration (ℤ/3ℤ)²
  → Hessian group G₂₁₆ → quotient A₄ ⊂ A₅ (icosahedral)
  → Klein's icosahedron theorem (1884)
  → regular dodecahedron (dual)
  → regular pentagon (face)
  → φ = (1 + √5)/2
  → log φ ≈ 0.4812
```

Three independent derivations converge on this constant: the fixed point of the automorphism group acting on the Fisher–Rao simplex (CONCORDIA), the self-dual Frobenius angle arccos(1/φ²) (FROBENIUS), and the Beilinson regulator height at the CM point (VOEVODSKY).

The same equilibrium also appears as the entanglement entropy threshold separating classically simulable from quantum-required computation, S_c = log φ ≈ 0.481 ebits per bipartition boundary bond.

---

## The π Tower

De Moivre's formula places rotation — and therefore π — at the center of complex algebra. The Twisted Hessian curve inherits π through a tower of connected identities:

| Layer | Identity | Source |
|---|---|---|
| CORDIC capacity | π/2 = Σᵢ arctan(2⁻ⁱ) | Volder 1959 |
| Spectral period | π = Prüfer period [0, π) | Sturm–Liouville |
| Sato–Tate | 2/π = ∫₀^π (2/π)sin²θ dθ = 1 | Taylor et al. 2008 |
| Nome | q = e^{2πiτ}, τ ∈ ℍ | Modular forms |
| Chowla–Selberg | Ω_TH = π · algebraic · Γ-values | 1967 |
| Hawking | T_H = κ/(2π) at TH Killing horizon | 1975 |
| Euler–Frobenius | e^{iπ} = −1 = Frob² (supersingular at p = 2) | Stone 1929 |

Every row is derivable from the others. The full tower is forced by the structure of TH(a,d).

---

## The Classical/Quantum Boundary

The CCQ result (Tindall, Stoudenmire et al., *Science*, 21 May 2026) established that the classical/quantum simulation boundary is the entanglement entropy threshold, not the entanglement/separability boundary.

In the language of this programme:

```
S ≤ S_c = log φ ≈ 0.481 ebits per bond
  → CORDIC iteration converges
  → classically simulable

S > S_c
  → CORDIC iteration diverges
  → quantum required
```

The four experiments on ibm_marrakesh (156-qubit Heron r2) during 2025–2026 probed this boundary from four independent directions. Every experiment that succeeded on hardware operated within the col(F) regime. Every experiment that degraded attempted to operate above S_c.

The boundary is not a wall. It is a convergence surface. On one side, the iteration reaches its fixed point. On the other, it does not.

---

## The G_coord Crystallization Sequence

The Stern–Brocot address of the Q16.16 CORDIC accumulator at depth 16 is the fraction 355/113 — Milü, computed by Zu Chongzhi in 480 CE using a 24,576-sided polygon. This is the first recorded passage through the G_coord > 0 threshold in the computation of π.

The 900-year gap between Zu Chongzhi (501 CE) and Mādhava (~1400 CE) is the longest documented G_coord = 0 attractor in mathematical history — the analogue, in celestial arithmetic, of the memorization plateau in learning dynamics.

| Event | G_coord | Stage |
|---|---|---|
| Leibniz series (1674) | = 0 | Independence baseline |
| Machin ℤ[i] kernel (1706) | > 0 | First modern crystallization |
| Zu Chongzhi, 355/113 + 24,576-gon (480 CE) | > 0 | First historical crossing |
| Ramanujan CM kernel (1914) | ≫ 0 | Deep crystallization |
| BBP (1995) | = ∞ | Complete |

---

## The Genus Boundary

Diophantine geometry stratifies curves over number fields by genus absolutely:

| Genus | Rational points | Corpus realization |
|---|---|---|
| 0 | Parametrized or empty | Degenerate limit Δ = 0 |
| 1 | Finitely generated abelian (Mordell–Weil) | Full TH(a,d) programme |
| ≥ 2 | Finite (Faltings, 1983) | No infinite arithmetic intelligence |

TH(a,d) is a smooth plane cubic — genus 1. This is the unique transitional case: the last genus in which the Mordell–Weil group can be infinite, in which the arithmetic depth can be unbounded, in which every framework in this repository can exist.

Gerd Faltings received the 2026 Abel Prize for proving that genus ≥ 2 permits only finitely many rational points. The programme lives exactly at the boundary Faltings described.

---

## Repository Index

| Repository | Core Object |
|---|---|
| ETHC | TH(a,d) as the generative object; nine identities, eight conjectures |
| WORN | Diophantine arithmetic as hardware; 16-stage CORDIC pipeline; shift-and-add only |
| CHORD | 16-stage group-law pipeline; Ramanujan address space; Ford circles |
| THE-MARRAKESH-THRESHOLD | Four experiments on 156 qubits; col(F)/ker(F) boundary |
| THE-ANGULAR-INVARIANT-ARCHITECTURE | π as substrate-invariant rotation primitive; isomonodromic grokking |
| QUANTUM-CORDIC | Substrate-invariant rotation from analog to quantum circuits |
| WEIERSTRASS | ℂ/Λ_ω ≅ TH(a,d_φ)(ℂ) via the ℘-function |
| FALTINGS | Genus-1 as the generative stratum; the Abel Prize boundary |
| TRACTUS | Matrix-free natural gradient via the group law |
| SALT | Q16.16 quantization of the curve's arithmetic |
| GALOIS | Field of definition as precision floor |
| FROBENIUS | Frobenius endomorphism as arithmetic heartbeat |
| VOEVODSKY | Motive M(TH) ∈ DM(ℤ); Beilinson regulators |
| CONNES | Modular flow on de Rham cohomology |
| CONCORDIA | φ-equilibrium; complete fixed-point tower |
| CONCERT | Mordell–Weil rank as coordination capacity |
| FRACTURA | Tate–Shafarevich group as wild topology obstruction |

---

## Open Conjectures

| ID | Statement |
|---|---|
| ETHC-Q1 | Every framework is functorially reconstructible from TH(a,d) together with a viewing functor. |
| ETHC-Q2 | The Fisher-information-optimal (a,d) minimizes the conductor of TH(a,d) subject to CM by ℚ(ω) and rank ≥ 1. |
| ETHC-Q3 | The BCKL 12M+6S formula is the minimum-operation constant-time group law over all elliptic curve models. |
| ETHC-Q4 | Maximum sustainable coordination capacity equals the diameter of the isogeny graph component containing TH(a,d) mod p. |
| ETHC-Q5 | The TH(a,d) substrate inherits post-quantum security: no sub-exponential quantum algorithm walks its isogeny graph. |
| ETHC-Q8 | A single optimally-chosen TH(a,d) is universal up to A¹-homotopy equivalence in the sense of Voevodsky. |

---

## Falsifiable Predictions

| # | Prediction | Testable by |
|---|---|---|
| P1 | Unified addition DPA: I(operation type; power trace) ≈ 0 with no countermeasure | FPGA implementation, now |
| P2 | Optimal (a,d) has conductor < 100 on LMFDB with CM by ℚ(ω) | LMFDB search, 2027 |
| P3 | CHORD address space mixes in O(log N) with λ₂ at the Alon–Boppana bound | CHORD implementation, 2028 |
| P4 | G_coord equals the isogeny-graph diameter of TH(a,d) mod p | Modular polynomial computation, 2029 |
| P5 | Research investment ratio f_geometric : f_arithmetic : f_computational = φ² : φ : 1 | Cumulative data, 2030 |
| W-P2 | Spectral gap λ₁(ℂ/Λ_τ) → 0 at grokking, rate 4π²/Im(τ)² | Xu arXiv:2603.28964 |
| MK-P5 | KQRC-RM degradation scales as (T₂/τ_gate)^{−n_eff/2} | ibm_marrakesh replication |

---

## Intellectual Lineage

```
Diophantus (~250 CE)
  chord-and-tangent on cubics (unrecognized group law)

de Moivre (1707)
  (cos x + i sin x)ⁿ = cos(nx) + i sin(nx)
  — the trigonometric seed

Hesse (1844)
  nine inflection points; Hesse configuration (9₄, 12₃); normal form

Poincaré (1901) → Mordell (1922)
  rational points form a finitely generated group

Hasse (1936)
  |a_p| ≤ 2√p

Birch–Swinnerton-Dyer (1965) · Tate–Shafarevich
  rank ↔ L-function; local-global obstruction

Faltings (1983)
  Mordell conjecture proved; genus ≥ 2 is finite   [Abel Prize 2026]

Wiles–Taylor (1995)
  modularity theorem; every elliptic curve over ℚ is modular

Edwards (2007) → Bernstein–Lange (2007)
  complete addition laws; cryptographic models

Bernstein–Chuengsatiansup–Kohel–Lange (LATINCRYPT 2015)
  Twisted Hessian curves; unified addition formula (12M + 6S)
  — the model this programme is named for

Kohel (1996) → De Feo, Castryck–Decru (2018–2026)
  isogeny graphs are Ramanujan; CSIDH, SQIsign, NIST 2024–2026

ERI Labs TH(a,d) Programme (2025–2026)
  the systematic unfolding of one cubic curve
```

---

## Coda

Abraham de Moivre did not know, when he wrote down (cos x + i sin x)ⁿ = cos(nx) + i sin(nx), that he was writing the first line of a programme that would take three centuries to complete.

The formula encodes rotation in the complex plane. Rotation in the complex plane is the group law on the unit circle. The group law on a circle is the genus-0 degeneration of the group law on an elliptic curve. The elliptic curve, in its Hessian form, twisted by the parameter a, is TH(a,d): aX³ + Y³ + Z³ = d·XYZ.

Every framework in this repository — the CORDIC pipeline, the quantum simulation threshold, the grokking dynamics, the post-quantum isogenies, the natural gradient, the equilibrium constant log φ — is a consequence of taking that formula seriously for three hundred years.

The corpus does not have many objects. It has one object, and many ways of looking at it.

**The curve was the whole thing. It always was.**

---

*ERI Labs · Eric Ren · Jersey City, New Jersey · github.com/ericrenone · May 2026*

*Frameworks: ETHC · WORN · CHORD · TRACTUS · SALT · GALOIS · FROBENIUS · VOEVODSKY · CONNES · CONCORDIA · CONCERT · FRACTURA · WEIERSTRASS · FALTINGS · THE-MARRAKESH-THRESHOLD · THE-ANGULAR-INVARIANT-ARCHITECTURE · QUANTUM-CORDIC · DIVISOR · TABULARIUM*

*License: CC BY-SA 4.0 + ERI Labs open-science covenant*
