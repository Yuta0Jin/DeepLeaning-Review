# 深度学习面试复习材料（大厂算法岗向）

这份仓库用于**快速复习深度学习基础知识**，偏“面试能讲清楚 + 现场能写出来/排查出来”的视角整理，适合作为大厂算法/机器学习岗位面试前的冲刺笔记与查漏补缺清单。

目前内容以 1 份笔记型 Notebook 为主，后续可以逐步扩展为“按模块拆分 + 配套题单/代码模板”的复习包。

## 目录结构

- `基础.ipynb`：深度学习基础速记 + 面试高频问题（含部分实现/示例）

## 覆盖主题（来自 `基础.ipynb`）

### 1) 梯度爆炸与梯度消失
- 核心原因：链式法则下多层梯度连乘
- 梯度消失/爆炸的表现与常见触发点
- 常用解决：ReLU、Xavier/He 初始化、残差连接、LSTM/GRU、BN/LN、梯度裁剪（`clip_grad_norm_` / `clip_grad_value_`）
- 项目排查经验：先排数据/数值稳定性与代码逻辑，再调超参/正则/裁剪

### 2) 激活函数（Activation Function）
- 为什么需要激活函数
- Sigmoid / Tanh / ReLU / Leaky ReLU / GELU（Transformer 常用）
- 使用场景与面试问法（例如：为什么 ReLU 优于 sigmoid、为什么 Transformer 常用 GELU）
- 含一部分“手写实现/直观解释”的练习内容

### 3) 损失函数
- 回归：MSE、MAE、Huber
- 分类：BCE、Cross Entropy
-（Notebook 内也包含一些常见对比点与记忆要点）

### 4) 过拟合与欠拟合
- 表现、常见原因
- 常用解决手段与排查顺序（数据、模型容量、正则化、训练策略等）

### 5) 优化器
- SGD、Momentum、AdaGrad、RMSProp、Adam、AdamW（Transformer 常用）
- 面试速记：什么时候用、优缺点、关键超参含义

## 使用方式

### 推荐打开方式
- **VS Code**：直接打开 `基础.ipynb`
- **JupyterLab / Jupyter Notebook**：本地启动后打开 `基础.ipynb`

> 说明：在终端里直接 `cat`/`Get-Content` 查看 `.ipynb` 往往不方便（Notebook 是 JSON 格式），建议用 VS Code 或 Jupyter 打开阅读与运行。
