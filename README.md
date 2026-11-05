# Adaptive Deep Koopman MPC — EVHP Dataset

This repository contains pressure and flow time-series data in CSV format for the paper *Adaptive Deep Koopman Model Predictive Control for Aortic Pressure Regulation in Ex Vivo Heart Perfusion*.

## Data directories

- `experiment/`: experimental data for pressure prediction validation and stepwise pressure regulation.
- `simulation/`: simulation data for multistep prediction, reference tracking, resistance disturbances, and controller comparisons.

| File | Data rows (excluding header) | Size (bytes) |
| --- | ---: | ---: |
| `experiment/pressure_prediction_validation.csv` | 1,242 | 27,327 |
| `experiment/stepwise_pressure.csv` | 3,604 | 56,189 |
| `simulation/multistep_prediction.csv` | 327,680 | 13,663,532 |
| `simulation/reference_controller_comparison.csv` | 7,200 | 260,963 |
| `simulation/reference_step.csv` | 576,000 | 22,247,518 |
| `simulation/reference_tracking.csv` | 3,328 | 131,867 |
| `simulation/resistance_controller_comparison.csv` | 7,200 | 260,061 |
| `simulation/resistance_disturbance.csv` | 1,916,928 | 74,243,105 |
| `simulation/resistance_tracking.csv` | 3,328 | 132,349 |

## Reading and verifying the data

The first row of each CSV file contains the column names. The suffixes `_s`, `_mmHg`, and `_mL_s` indicate seconds, millimeters of mercury, and milliliters per second, respectively. Other identifier fields retain their original values.

`manifest.json` lists the column names, data row counts, file sizes in bytes, and SHA-256 checksums for each CSV file. `SHA256SUMS` can be used to verify file integrity. The CSV files preserve the original bytes; no resampling, filtering, or numerical modifications have been applied.

## License

No open-use license has been specified for this repository. Please contact the authors regarding use or redistribution.
