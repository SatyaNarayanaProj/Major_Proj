# Inverse Design Model (L, W, G Prediction)

This project predicts geometric parameters (L, W, G) from frequency response curves using deep learning and compares them with classical ML models.

## Overview

- Input: Frequency response curve (1001 points)
- Output: Parameters → L, W, G
- Models:
  - Hybrid CNN (Inverse + Forward model)
  - Random Forest
  - Gradient Boosting
  - SVR
  - KNN
  - Ridge Regression
  - Simple 1D CNN (baseline)

## Dataset

- Training samples: 2789
- Test samples: 21

## Best Model

Hybrid CNN (InverseNet + ForwardNet)

### Final Metrics (Unclipped)

| Metric | L | W | G |
|------|------|------|------|
| MAE  | 1.061 | 0.282 | 2.790 |
| RMSE | 2.082 | 0.392 | 4.560 |
| MSE  | 4.338 | 0.153 | 20.797 |

## Baseline Comparison

| Model | MAE_L | MAE_W | MAE_G | R2_L | R2_W | R2_G |
|------|------|------|------|------|------|------|
| Random Forest | 1.616 | 1.069 | 4.407 | 0.874 | 0.644 | 0.022 |
| Gradient Boosting | 1.384 | 1.495 | 5.341 | 0.910 | 0.464 | -0.259 |
| SVR | 2.104 | 1.148 | 4.626 | 0.800 | 0.614 | 0.054 |
| KNN | 1.557 | 0.936 | 4.392 | 0.901 | 0.752 | 0.033 |
| Ridge | 1.862 | 4.023 | 11.983 | 0.856 | -7.611 | -7.282 |
| Simple CNN | 0.894 | 0.595 | 2.648 | 0.980 | 0.928 | 0.528 |

## Files

- training script: :contentReference[oaicite:0]{index=0}
- testing / optimization: :contentReference[oaicite:1]{index=1}
- baseline ML models: :contentReference[oaicite:2]{index=2}

## Run
