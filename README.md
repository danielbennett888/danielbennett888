<h2 align="center">Daniel (Bennett) Bai · 白</h2>

<p align="center">
  澳门科技大学在读 · 声学大模型方向 · 升学 / 深造中的科研项目实践<br/>
  <em>把「统一声学表示」接入大模型的声学理解，坚持可复现、离线优先的开源实现。</em>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Focus-声学大模型-1f6feb?style=flat-square" alt="focus" />
  <img src="https://img.shields.io/badge/School-澳门科技大学 MUST-2ea44f?style=flat-square" alt="school" />
  <img src="https://img.shields.io/badge/Style-可复现 · 离线优先-blueviolet?style=flat-square" alt="style" />
</p>

---

### 👋 关于我

我是 **澳门科技大学** 的学生，正在为升学 / 深造做准备，围绕**声学大模型**做一系列科研项目实践。研究关注两条主线：

- **统一声学表示** —— 用一致的接口把声学特征前端与自监督编码器串起来，让不同下游任务共享同一套表示。
- **接入大模型的声学理解** —— 在表示之上做场景理解，并交给大模型（或离线模板）产出自然语言的声学场景描述。

工程上我偏好**可复现**、**离线优先**：核心逻辑尽量用纯 Python / NumPy 写清楚，联网大模型与深度学习框架只作为**可选**后端，方便在没有 GPU、没有外网的环境里也能完整跑通。

---

### 📦 精选项目

#### [`sonoscribe`](https://github.com/danielbennett888/sonoscribe) — 声学大模型工具包

> 统一声学自监督表示 + 大模型声学场景理解与描述的轻量工具包。（纯 NumPy 内核，离线优先，可选 PyTorch）

把「声学特征前端 → 自监督表示 → 大模型场景描述」串成一条清晰、可复现的流水线：

| 阶段 | 能力 | 入口 |
|------|------|------|
| **特征** | STFT / 梅尔谱 / 对数梅尔谱 / MFCC 与差分 / 频谱与时域描述子 | `sonoscribe.features` |
| **表示** | 统一 `Encoder` 接口：纯 NumPy 自监督 `PredictiveEncoder`、统计池化 `HandcraftedEncoder`，可选 `TorchGRUEncoder` | `sonoscribe.represent` |
| **描述** | 启发式场景理解 + 结构化报告 + 大模型 / 离线模板描述 | `describe_audio` |

- 🧩 **纯 Python / NumPy 内核**：特征、自监督编码器、场景描述全部离线可跑，不依赖 PyTorch 或联网。
- 🔌 **可选后端**：需要时再启用 PyTorch 编码器，或 OpenAI 兼容的大模型接口。
- 🖥️ **命令行**：`sonoscribe info / features / embed / describe`，可直接产出中 / 英文场景描述。
- 🧪 **工程完备**：CI、CodeQL、发布流水线、pre-commit、成套单元测试与架构 / 使用 / 设计 / API 文档。

<sub>技术栈：`Python 3.9+` · `NumPy` · 可选 `PyTorch` / OpenAI 兼容接口 · MIT · v0.1.0</sub>

---

### 🛠️ 常用技术

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="python" />
  <img src="https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white" alt="numpy" />
  <img src="https://img.shields.io/badge/PyTorch%20(可选)-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" alt="pytorch" />
  <img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" alt="actions" />
  <img src="https://img.shields.io/badge/Ruff-000000?style=flat-square&logo=ruff&logoColor=white" alt="ruff" />
  <img src="https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white" alt="pytest" />
</p>

---

### 🔭 正在做的事

- 打磨 **SonoScribe** 的表示层，让自监督编码器与场景理解在更多声学任务上复用同一套接口。
- 探索**声学场景描述**与大模型的更自然衔接：离线模板保底、联网大模型增强，两条路都保持可复现。
- 为升学 / 深造持续积累**可离线复现**的科研项目实践与工程记录。

<sub>📍 Macau · 澳门科技大学　｜　方向：声学大模型 · 统一声学表示 · 大模型声学理解</sub>
