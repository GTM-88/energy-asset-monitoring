# PROJECT OVERVIEW

## Energy Asset Monitoring Framework

---

## 1. Project Vision

This project aims to demonstrate a complete data-driven workflow for monitoring and analysing the operation of an industrial energy asset using synthetic time-series data.

The objective is **not** to develop a high-fidelity physical simulator, but to build a realistic engineering case study that showcases the complete analytics pipeline typically adopted in industrial energy monitoring projects.

The final deliverable is an interactive monitoring dashboard supported by a well-structured Python project and documented Jupyter notebooks.

---

## 2. Motivation

The project has been designed as a portfolio case study for positions related to:

- Energy Data Engineering
- Energy Analytics
- Building and HVAC Optimization
- Digital Twins
- Industrial Monitoring
- Energy Performance Analysis

The implementation intentionally emphasizes:

- engineering reasoning;
- data quality;
- reproducibility;
- code readability;
- interactive visualization.

---

## 3. Project Scope (MVP)

The Minimum Viable Product (MVP) includes:

- Synthetic time-series dataset generation
- Simplified physical modelling of an energy storage system
- Data quality assessment
- Rule-based operating state analysis
- Operational KPI calculation
- Interactive Plotly dashboard
- Complete project documentation

The project deliberately avoids unnecessary complexity while maintaining engineering consistency.

---

## 4. Out of Scope

The following topics are intentionally excluded from the MVP:

- Machine Learning
- CFD simulations
- Detailed thermodynamic modelling
- Optimization algorithms
- Cloud deployment
- Web applications
- Real industrial datasets

These features are considered future developments.

---

## 5. Synthetic Plant Description

The monitored asset is a simplified Compressed Air Energy Storage (CAES) system.

The synthetic plant operates according to predefined operating schedules and generates coherent process variables including:

- Tank pressure
- Tank temperature
- Compressor electrical power
- Turbine electrical power
- Air mass flow
- Ambient temperature

The generated dataset does not represent any confidential or proprietary industrial process.

---

## 6. Engineering Philosophy

Instead of generating random signals independently, the project first defines the operating behaviour of the asset.

The workflow is:

Operating Schedule

↓

Operating Mode

↓

Simplified Physical Model

↓

Measured Signals

↓

Data Analytics

↓

Operational KPIs

↓

Interactive Dashboard

This approach guarantees that all generated variables remain physically consistent.

---

## 7. Engineering Assumptions

The project intentionally adopts simplified engineering models.

### Pressure

Pressure follows a first-order dynamic.

Charging increases pressure progressively towards an upper limit.

Discharging decreases pressure towards a minimum operating pressure.

Stand-by introduces small leakage losses.

---

### Temperature

Tank temperature evolves towards an operating-mode-dependent equilibrium.

Charging produces heating.

Discharging produces cooling.

Stand-by naturally converges towards ambient temperature.

---

### Power

Electrical power is estimated using simplified empirical relationships.

The compressor consumes power only during charging.

The turbine produces power only during discharging.

Small Gaussian noise emulates measurement uncertainty.

---

### Mass Flow

Positive values represent charging.

Negative values represent discharging.

Stand-by flow is zero.

---

### Noise

Synthetic Gaussian noise is added to selected variables to emulate sensor uncertainty.

Future versions may also include:

- sensor drift;
- missing values;
- stuck sensors;
- outliers.

---

## 8. Repository Structure

```text
EnergyAssetMonitoring/

│
├── data/
│   ├── raw/
│   └── processed/
│
├── figures/
│
├── notebooks/
│   ├── 01_generate_synthetic_dataset.ipynb
│   ├── 02_data_quality_assessment.ipynb
│   └── 03_monitoring_dashboard.ipynb
│
├── reports/
│
├── src/
│
├── README.md
│
└── PROJECT_OVERVIEW.md
```

---

## 9. Development Roadmap

### Notebook 1

Generate synthetic operating data.

Output:

- CSV dataset
- Interactive Plotly overview

---

### Notebook 2

Assess dataset quality.

Topics:

- Missing values
- Outliers
- Sensor anomalies
- Data completeness

---

### Notebook 3

Perform operational analysis.

Topics:

- Energy KPIs
- Cycle detection
- Efficiency
- Interactive dashboard

---

## 10. Current Status

Completed

- Project architecture
- Repository structure
- Timeline generation
- Operating schedule
- Operating modes
- Pressure model
- Initial temperature model

In Progress

- Improved temperature dynamics
- Compressor power model
- Turbine power model
- Mass flow model

Planned

- Energy calculation
- Operational KPIs
- Plotly dashboard
- Documentation
- GitHub publication

---

## 11. Future Improvements

Possible future developments include:

- ML-based operating mode classification
- Fault detection
- Predictive maintenance
- Digital Twin calibration
- Weather integration
- Multiple assets
- HVAC case studies
- Real industrial datasets

---

## 12. Design Principles

During development, the following principles are adopted:

- Engineering consistency over mathematical complexity.
- Readability over optimization.
- Modular code.
- Well-documented notebooks.
- Interactive visualizations.
- Reproducible workflow.
- Every modelling assumption should be explainable during a technical interview.

---
