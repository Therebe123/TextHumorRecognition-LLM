# 论文介绍
## 标题
中文文本的幽默识别：基于大语言模型的少样本提示与监督微调
## 摘要
幽默是一种涉及语言学多个领域，受文化背景与个人认知影响的复杂语言表达。对计算机
而言文本幽默识别是一项常见而困难的挑战，而传统文本幽默识别高度依赖于人工设计的幽默
相关特征。受展现出强大自然语言理解能力的大语言模型启发，本文使用 Qwen1.5-7B 作为基座
大语言模型，并分别搭建了少样本提示与监督微调两个框架，使得基座模型在特定中文文本幽
默程度分类任务上具备更强且更有针对性的幽默识别能力。在少样本提示框架下，基于最相似
示例的提示增强方法使得模型在 macro F1 score 指标上达到 0.25，高于无示例的零样本提示情况
（0.21）。在基于 LoRA 微调方法的监督微调框架下，基座模型仅仅经过不到 3 个周期的训练后
便在 macro F1 score 指标上达到 0.48，显著高于 BERT 模型（0.27）与零样本提示情况下的
ChatGPT3.5-turbo（0.31）。基于少样本提示与监督微调框架的 Qwen1.5-7B 模型不仅能够更好地
适应中文文本的幽默识别任务，而且能够在本地个人电脑上实现简单部署，具有广泛的应用前
景。项目代码公布于：https://github.com/Therebe123/TextHumorRecognition-LLM 。

# Python环境介绍
## Python 版本
**3.10.8**
## Cuda版本
**12.1**
## 主要Python库
**torch**  2.1.2+cu121
**transformers**  4.38.2
accelerate  0.28.0
bitsandbytes  0.42.0
flash-attention  1.0.0
flash-attn  2.5.6
openai  1.13.3
