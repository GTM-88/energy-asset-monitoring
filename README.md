# Energy Asset Monitoring Framework

An end-to-end Python project for monitoring and analysing the operation of an industrial energy asset using synthetic time-series data.

The project simulates the operation of a simplified Compressed Air Energy Storage (CAES) system and demonstrates a complete engineering workflow, from synthetic data generation to operational performance analysis through interactive dashboards.

The objective is **not** to develop a high-fidelity thermodynamic simulator, but to build a realistic and coherent dataset suitable for data analytics, monitoring and visualization.

---

# Project Objectives

This project explores a typical workflow adopted in industrial energy monitoring applications:

- Generate physically coherent synthetic time-series data.
- Simulate realistic sensor behaviour.
- Assess data quality and identify common anomalies.
- Compute operational Key Performance Indicators (KPIs).
- Visualize asset behaviour through interactive dashboards.

The implementation focuses on engineering consistency, readability and reproducibility rather than detailed physical modelling.

---

# Workflow

```text
Synthetic Plant
        │
        ▼
Synthetic Dataset Generation
        │
        ▼
Data Quality Assessment
        │
        ▼
Operational KPI Calculation
        │
        ▼
Interactive Monitoring Dashboard
```

Each stage is implemented as an independent notebook while preserving a coherent end-to-end workflow.

---

# Repository Structure

```text
EnergyAssetMonitoring/

├── data/
│   ├── raw/
│   └── processed/
│
├── figures/
│
├── notebooks/
│   ├── 01_generate_synthetic_dataset.ipynb
│   ├── 02_data_quality_assessment.ipynb
│   └── 03_operational_kpi_dashboard.ipynb
│
├── reports/
│
├── src/
│
├── PROJECT_OVERVIEW.md
└── README.md
```

---

# Synthetic Plant

The monitored asset is a simplified Compressed Air Energy Storage (CAES) system.

Although simplified, the implemented models preserve the main physical relationships between process variables, allowing the generation of coherent operating data suitable for engineering analyses.

The generated dataset includes:

- Operating mode
- Tank pressure
- Tank temperature
- Ambient temperature
- Compressor electrical power
- Turbine electrical power
- Air mass flow

Two datasets are generated:

| Dataset | Description |
|----------|-------------|
| Clean Dataset | Synthetic measurements without sensor imperfections |
| Noisy Dataset | Synthetic measurements including measurement noise and data quality anomalies |

---

# Engineering Assumptions

The project intentionally adopts simplified engineering models.

Rather than reproducing the detailed thermodynamic behaviour of a CAES plant, the implemented models aim to preserve the logical relationships between operating conditions and measured variables.

Examples include:

- pressure evolution through first-order dynamics;
- temperature convergence towards operating-mode-dependent equilibrium values;
- pressure-dependent compressor and turbine power;
- pressure-dependent mass flow;
- Gaussian measurement noise;
- configurable sensor anomalies.

This approach provides realistic datasets while keeping the implementation compact and easy to understand.

---

# Notebooks

## 01 — Synthetic Dataset Generation

Generates coherent operating data describing the behaviour of the synthetic CAES system.

Outputs:

- clean dataset
- noisy dataset
- interactive operating profile

---

## 02 — Data Quality Assessment

Evaluates the generated dataset and identifies common data quality issues, including:

- missing values;
- outliers;
- sensor anomalies;
- data completeness.

Detected anomalies are summarized in a report and highlighted through interactive visualizations.

---

## 03 — Operational KPI Dashboard

Calculates engineering KPIs from the generated dataset and visualizes the operational behaviour of the asset.

Example indicators include:

- charging duration;
- discharging duration;
- stand-by duration;
- compressor energy consumption;
- turbine energy production;
- round-trip efficiency;
- operating cycles.

Results are presented through an interactive Plotly dashboard.

---

# Technologies

- Python
- Pandas
- NumPy
- Plotly
- Jupyter Notebook

---

# Future Developments

Possible future extensions include:

- advanced fault detection;
- predictive maintenance;
- machine learning models;
- digital twin calibration;
- additional energy assets;
- HVAC monitoring applications.

---

# License

This repository is intended for educational and research purposes.