# Adaptive Deep Koopman MPC — EVHP 数据包

本仓库保存论文 *Adaptive Deep Koopman Model Predictive Control for Aortic Pressure Regulation in Ex Vivo Heart Perfusion* 的压力与流量时序 CSV 数据。

## 数据目录

- `experiment/`：压力预测验证与阶梯压力实验数据。
- `simulation/`：多步预测、参考值跟踪、阻力扰动及控制器比较数据。

| 文件 | 数据行数（不含表头） | 字节数 |
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

## 读取与校验

CSV 第一行为字段名。字段后缀 `_s`、`_mmHg` 和 `_mL_s` 分别表示秒、毫米汞柱和毫升/秒；其余标识字段保留原数据值。

`manifest.json` 记录每个 CSV 的字段名、数据行数、字节数和 SHA-256 校验值；`SHA256SUMS` 可用于验证文件完整性。CSV 按原始字节保存，未进行重采样、筛选或数值修改。

本仓库当前仅包含上述时序数据，不包含模型权重、训练代码或完整复现实验环境。

## 使用许可

本仓库尚未指定开放使用许可证。如需使用或再分发，请联系作者。
