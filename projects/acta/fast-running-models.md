# Fast-Running Simulation Models

**Context:** ACTA-SH
**Stack:** LISA FEM, Python
**Focus:** Reduced-Order Modeling, Structural Dynamics, Simulation

---

## Overview

Developed fast-running simulation models of building infrastructure to enable large-scale risk analysis under blast and debris loading conditions.

These models were derived from higher-fidelity finite element simulations and reduced into efficient representations using precomputed frequency response functions (FRFs).

---

## Problem

* Full finite element simulations were too computationally expensive for large-scale analysis
* Required simulation of thousands of scenarios for Monte Carlo workflows
* Needed accurate representation of structural response under both blast and debris loading
* Experimental validation was required to ensure model fidelity

---

## Approach

Built a reduced-order modeling pipeline:

1. Created detailed finite element models of infrastructure systems using LISA FEM
2. Generated frequency response functions (FRFs) for each system
3. Validated FRFs against experimental data
4. Used FRFs as efficient runtime models for simulation

This enabled simulation of complex structural responses without running full FEM models.

---

## Model Construction

* Built simplified “digital twin” representations of:

  * HVAC systems
  * Water systems
  * Electrical infrastructure
* Focused on capturing dominant structural dynamics rather than full geometric fidelity
* Extracted system response characteristics through frequency-domain analysis

---

## Loading Methods

Implemented different loading strategies depending on physical mechanism:

### Blast Loading

* Applied distributed pressure loads across surfaces
* Modeled spatial and temporal variation of blast waves

### Debris Impact Loading

* Applied point impulse forces at impact locations
* Represented discrete, high-energy events

This separation allowed accurate modeling of fundamentally different loading conditions.

---

## Validation

* Compared model outputs directly against experimental data from blast tests
* Correlated predicted and observed structural responses
* Iteratively refined models to improve agreement

---

## Key Features

* Orders-of-magnitude faster than full FEM simulations
* Compatible with large-scale Monte Carlo pipelines
* Flexible across multiple infrastructure types
* Physically grounded through experimental validation

---

## Results / Impact

* Enabled large-scale simulation of blast and debris scenarios
* Provided validated inputs for risk and safety analysis workflows
* Bridged high-fidelity simulation and real-time or batch analysis systems
