# Modelling and Stability Analysis of Thin, Hyperelastic Membranes

**B.Tech. Project Stage II — Department of Aerospace Engineering, IIT Bombay**  
**Author:** Anuttar Jain  
**Supervisor:** Professor Krishnendu Haldar  
**Final report:** May 2026

## Overview

This project investigates the modelling and stability of thin membranes undergoing moderate-to-large deformation. It examines the limitations of classical plate theories and develops a large-deformation plate formulation, then applies computational methods to study membrane response and spatial stability.

The work combines continuum mechanics, nonlinear strain measures, constitutive modelling, finite-element simulation, and eigenvalue-based stability classification. The final report also develops a magneto-elastic membrane formulation using a hyperelastic constitutive model.

## Project objectives

- Review classical plate models and understand their limitations when large deformations, wrinkling, and post-buckling behaviour are important.
- Formulate a large-deformation plate model using Green–Lagrange membrane strains and a linearised curvature tensor.
- Derive coupled equilibrium equations and natural boundary conditions using an energy-based formulation.
- Simulate membrane behaviour in COMSOL Multiphysics under uniaxial stretching and transverse loading.
- Formulate a magneto-elastic membrane model using a Mooney–Rivlin hyperelastic constitutive law and a field-dependent magneto-elastic contribution.
- Investigate spatial stability by linearising the governing system about an equilibrium solution and classifying regions using the eigenvalues of a quadratic eigenvalue problem.

## Methodology

### 1. Classical plate theories

The report reviews Classical Plate Theory (Kirchhoff–Love theory) and the Föppl–von Kármán model. Their assumptions and limitations motivate the use of a model that can represent larger deformations and more complex stability behaviour.

### 2. Large-deformation plate formulation

The model uses the Kirchhoff–Love kinematic assumptions and a Green–Lagrange membrane strain tensor. The total energy is separated into membrane and bending contributions, with bending described through a linearised curvature tensor. The governing equilibrium equations and associated natural boundary conditions are derived variationally.

### 3. COMSOL simulations

The governing equations are recast into a form suitable for finite-element implementation in COMSOL Multiphysics. The report considers two loading cases:

- A plate under uniaxial stretching.
- A plate under uniform transverse loading.

The simulations are used to examine deformation response, membrane stiffening, sensitivity to imperfections, and the influence of boundary constraints.

### 4. Magneto-elastic membrane model

The report extends the formulation to a magneto-elastic membrane. The constitutive model includes:

- A Mooney–Rivlin hyperelastic contribution.
- A volumetric energy contribution to account for compressibility.
- A field-dependent magneto-elastic contribution.
- A bending energy contribution.

The plane-stress condition is used to determine the through-thickness stretch, and the corresponding stress measures and equilibrium equations are formulated.

### 5. Spatial stability analysis

The governing equations are linearised about an equilibrium solution. The resulting coefficient matrices are used to construct a quadratic eigenvalue problem at spatial points across the membrane. A MATLAB post-processing workflow evaluates the eigenvalues and classifies points as elliptic or hyperbolic, producing a spatial stability map.

The report notes numerical sensitivity in some loading cases; these classifications should therefore be interpreted as qualitative results rather than definitive quantitative stability boundaries.

## Main observations

- Classical plate models have limitations when applied to large deformations and complex wrinkling or post-buckling behaviour.
- The large-deformation formulation couples in-plane and transverse responses through nonlinear membrane strains.
- COMSOL simulations demonstrate nonlinear response and sensitivity to boundary conditions and imperfections.
- The magneto-elastic formulation incorporates hyperelastic, volumetric, magnetic, and bending contributions into a common model.
- The spatial stability analysis identifies localized hyperbolic regions for some loading cases, while other cases remain elliptic. The report also identifies numerical sensitivity that requires further investigation.

## Repository contents

The repository contains the project reports and presentations shown below.

```text
.
├── README.md
├── Conference Presentation.pdf
├── Final Presentation.pdf
├── Final Report.pdf
├── Stage 1 Presentation.pdf
└── Stage 1 Report.pdf
```

### Files

| File | Description |
|---|---|
| `Final Report.pdf` | Main Stage-II report, covering the large-deformation model, COMSOL simulations, magneto-elastic formulation, and spatial stability analysis. |
| `Final Presentation.pdf` | Final project presentation. |
| `Conference Presentation.pdf` | Presentation prepared for a conference. |
| `Stage 1 Report.pdf` | Report documenting the first stage of the project. |
| `Stage 1 Presentation.pdf` | Presentation for the first stage of the project. |

## Tools and methods

- **COMSOL Multiphysics** — finite-element simulation of the governing plate equations.
- **MATLAB** — post-processing of COMSOL data and eigenvalue-based spatial stability classification.
- **Continuum mechanics** — finite-deformation kinematics, Green–Lagrange strain, stress measures, and energy-based equilibrium.
- **Nonlinear stability analysis** — linear perturbation equations, quadratic eigenvalue problems, and elliptic/hyperbolic classification.

## Limitations and future work

The report identifies numerical sensitivity in the spatial stability classification, particularly in cases where the results are inconsistent with the expected near-linear response. Further work could include:

- Improving numerical conditioning and validating the eigenvalue classification.
- Performing mesh and discretisation sensitivity studies.
- Comparing stability predictions against independent analytical or numerical results.
- Extending the post-buckling analysis and investigating bifurcation behaviour in greater detail.
- Validating the magneto-elastic model against experimental data.

## References

The final report discusses relevant work on nonlinear plate and membrane stability, including research by Healey and co-authors on wrinkling and stability boundaries, and Garai and Haldar on magneto-stiffening in magnetoactive polymers. Full bibliographic details are provided in `Final Report.pdf`.

## Academic context

This repository documents an undergraduate thesis project completed as **AE 494 B.Tech. Project Stage-II** in the Department of Aerospace Engineering at the Indian Institute of Technology Bombay.

## Disclaimer

This repository is intended for academic and research reference. The modelling assumptions and numerical results are described in the accompanying reports; stability classifications include cases noted in the report as numerically sensitive. Verify the formulation, implementation, and results independently before using them in further research or engineering applications.
