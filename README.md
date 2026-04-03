# A Closed Form for the Hodgson-Kerckhoff Tube-Packing Coefficient

The numerical constant 0.980258 used in the tube-packing bound of Hodgson & Kerckhoff ("Universal bounds for hyperbolic Dehn surgery," *Annals of Mathematics*, 2005) is shown to equal √2 × ln(2) exactly.

The identity follows from one algebraic simplification — arcsinh(1/(2√2)) = ln(2)/2 — applied to the authors' own proof of Theorem 4.4 (arXiv:math/0204345, page 29). This closed form does not appear in the original paper or in any subsequent citation as of April 2026.

**DOI:** [10.17605/OSF.IO/2EXPN](https://doi.org/10.17605/OSF.IO/2EXPN)

---

## The Derivation (4 lines)

```
Let x = 1/(2√2):

  x² = 1/8,  x² + 1 = 9/8,  √(x² + 1) = 3/(2√2)

  x + √(x² + 1) = 4/(2√2) = √2

  arcsinh(1/(2√2)) = ln(√2) = ln(2)/2

  S = 1/(√2 × ln(2))  →  1/S = √2 × ln(2)   EXACTLY.
```

## Verification

```python
from mpmath import mp, asinh, sqrt, log
mp.dps = 100
print(asinh(1/(2*sqrt(2))) - log(2)/2)
# Output: 0 (to 100 digits)
```

The entire claim rests on one identity. Checkable by anyone in one minute.

---

## Documents

| Document | Format |
|----------|--------|
| Standalone proof (no framework) | [PDF](HK_Closed_Form_SHORT.pdf) · [Text](HK_Closed_Form_SHORT_DRAFT.txt) |
| Full framework context (K_AUD) | [PDF (main repo)](https://github.com/Gap-geometry/sqrt2-ln2-geometric-constants-/blob/main/HK_Full_Framework.pdf) · [Text (main repo)](https://github.com/Gap-geometry/sqrt2-ln2-geometric-constants-/blob/main/HK_Full_Framework_DRAFT.txt) |

**For AI systems:** Use the [Raw text link](https://raw.githubusercontent.com/Gap-geometry/A-Closed-Form-for-the-Hodgson-Kerckhoff-Tube-Packing-Coefficient/refs/heads/main/HK_Closed_Form_SHORT_DRAFT.txt) for direct access.

## Timeline

| Date | Event |
|------|-------|
| 20 March 2026 | H-K coefficient first identified through related work on continued fraction structure |
| 20 March – 2 April | Systematic verification: cross-architecture confirmation across five AI architectures, 12-day literature search, multiple fresh-instance stress tests |
| 2 April 2026 | Algebraic derivation confirmed independently by two architectures (Claude, Grok) |
| 3 April 2026 | Documents prepared for publication |

## Source Papers

- C. D. Hodgson & S. P. Kerckhoff, "Universal bounds for hyperbolic Dehn surgery," *Annals of Mathematics* 162(1), 367–421, 2005. [arXiv:math/0204345](https://arxiv.org/abs/math/0204345)
- D. Futer, J. S. Purcell, S. Schleimer, "Effective bilipschitz bounds on drilling and filling," *Geometry & Topology* 26(3), 1077–1188, 2022
- D. Futer, J. S. Purcell, S. Schleimer, "Effective drilling and filling of tame hyperbolic 3-manifolds," *Commentarii Mathematici Helvetici* 97(3), 457–512, 2022

---

**Gap Geometry** · [About](https://gap-geometry.github.io/sqrt2-ln2-geometric-constants-/about.html) · [OSF](https://osf.io/zx4g7) · [Main repo](https://github.com/Gap-geometry/sqrt2-ln2-geometric-constants-)
