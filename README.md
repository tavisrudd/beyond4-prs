# Deep holes beyond redundancy four

[![DOI](https://zenodo.org/badge/1315346158.svg)](https://doi.org/10.5281/zenodo.21682069)

This directory contains the manuscript
*Deep holes of projective Reed--Solomon codes beyond redundancy four:
exact classifications at redundancies five through seven* and its public
verification bundle.

The paper proves complete deep-hole classifications at redundancies five and
six over every prime power \(q\geq7\).  At redundancy seven it proves the
complete split-free classification over the same range and promotes it to a
deep-hole classification whenever the covering radius is six, in particular
for \(q\geq11\).  It makes no arbitrary-redundancy claim.

## Build

From this directory:

```text
make check
make tit-check
```

`make check` builds the 30-page canonical preprint
`prs-beyond-redundancy-four.pdf`.  `make tit-check` builds the 23-page
IEEEtran single-column review manuscript
`prs-beyond-redundancy-four-tit-submission.pdf`.

The canonical and IEEEtran drivers consume the same abstract, index terms,
eight active section files, acknowledgment, and bibliography.  Their layout
is recorded in `sections/README.md`.

## Verification

The electronic supplement contains public classification records, generators,
independent replays, checksums, toolchain locks, and the declaration-level map
of the conditional Lean formalization.

Run

```text
python3 supplement/verify.py
```

for the local bundle, classification-record, manuscript-label, and formal-scope
checks.  Add `--replay` to execute every paper-local Python replay.
`--release` is reserved for an immutable public candidate whose repository,
revision, archive, DOI, PDF, and independent-reader fields are complete.

Lean checks coordinate algebra, finite-record arithmetic, degree-specific
budgets, and conditional synthesis.  The geometric classifications, cited
point and covering-radius theorems, group actions, and certificate semantics
retain the explicit trust routes recorded in
`supplement/LEAN-STATEMENTS.md`.

The Lean sources are distributed in
[`finitegeom`](https://github.com/tavisrudd/finitegeom), pinned at commit
`77c0d6bb5a45a1aa15a0ab90b7db307e1a1804d2`. The paper-facing boundary is
`RelativeConicArcs.Gates.PRSBeyondRedundancyFourAxiomAudit`; its 17-module
closure and terminal axiom sets are recorded under `trust/`.
The version-independent archival locator is the Zenodo concept DOI
[`10.5281/zenodo.21650878`](https://doi.org/10.5281/zenodo.21650878).

## Scope

Redundancies eight and nine, ordered-Hessian geometry, arbitrary-level
stable-component assertions, and higher Lucas-carrier arithmetic are companion
work.  They are neither manuscript theorems nor inputs to the R5--R7
classifications.

The local verification commands do not upload or publish artifacts.
