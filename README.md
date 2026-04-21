# 基于 Bi-LSTM 的测井岩性识别系统

## 1. 项目简介
本项目旨在利用深度学习技术解决石油钻探中自动识别地层岩性的难题。基于 **PaddlePaddle 2.x** 框架，通过双向长短期记忆网络（Bi-LSTM）对测井序列进行时序建模。

## 2. 核心算法
- **模型架构**：双向 LSTM（Bi-Directional LSTM）
- **特征工程**：选取 GR, RDEP, RHOB, NPHI, DTC 五类核心物理曲线，采用 Z-Score 标准化处理。
- **训练策略**：Adam 优化器 + 动态学习率衰减 + 早停机制。

## 3. 实验结果
| 模型 | 准确率 | 优势 |
| :--- | :--- | :--- |
| **Bi-LSTM** | **69.39%** | 能够捕捉地层上下接触关系的全局特征 |
| **Uni-LSTM** | 69.64% | 计算开销小，推理速度快 |

## 4. 如何运行
1. 下载 `main.ipynb`。
2. 在飞桨 AI Studio 或本地 Jupyter 环境打开。
3. 挂载 [FORCE 2020 测井数据集](https://www.kaggle.com/datasets/faresazzam/well-logs-dataset-for-machine-learning)。
