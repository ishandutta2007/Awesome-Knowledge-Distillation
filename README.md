<div align="center">

<img src="assets/banner.svg" width="800" alt="Awesome Knowledge Distillation Banner">

# 🧠 Awesome Knowledge Distillation 🚀

[![GitHub stars](https://img.shields.io/github/stars/ishandutta2007/Awesome-Knowledge-Distillation?style=flat-square)](https://github.com/ishandutta2007/Awesome-Knowledge-Distillation/stargazers)
[![GitHub license](https://img.shields.io/github/license/ishandutta2007/Awesome-Knowledge-Distillation?style=flat-square)](https://github.com/ishandutta2007/Awesome-Knowledge-Distillation/blob/main/LICENSE)
[![GitHub issues](https://img.shields.io/github/issues/ishandutta2007/Awesome-Knowledge-Distillation?style=flat-square)](https://github.com/ishandutta2007/Awesome-Knowledge-Distillation/issues)
[![Repo Size](https://img.shields.io/github/repo-size/ishandutta2007/Awesome-Knowledge-Distillation?style=flat-square)](https://github.com/ishandutta2007/Awesome-Knowledge-Distillation)
<a href="https://github.com/ishandutta2007"><img alt="GitHub followers" src="https://img.shields.io/github/followers/ishandutta2007?label=Follow&style=flat-square" /></a>

**A curated list of Knowledge Distillation (KD) variants, techniques, and seminal papers for modern AI model compression.**

[Explore Docs](docs/response_based_definition.md) • [Paper Links](#1-response-based-distillation-logit-distillation) • [Contribute](.github/CONTRIBUTING.md)

---

<!-- SEO Meta Description: A comprehensive guide to Knowledge Distillation in AI, covering Response-based, Feature-based, Relation-based, and Self-distillation techniques. Learn how to compress Teacher models into lightweight Student models for edge deployment. -->
<!-- Keywords: AI, Machine Learning, Knowledge Distillation, Model Compression, Deep Learning, Student-Teacher, Logit Distillation, Neural Network, Edge AI -->

</div>

## 📖 Introduction

**Knowledge Distillation (KD)** is a powerful machine learning technique that transfers "dark knowledge" from a large, complex **Teacher** network to a compact, deployable **Student** network. This allowed lightweight models to achieve near-server-class performance on edge devices. 📱💻

---

## 🏗️ 1. Response-Based Distillation (Logit Distillation) 🎯
*Traditional approach where the student mimics the teacher's final predictions.*

| Concept | Details | Year | Paper Link |
| :--- | :--- | :--- | :--- |
| **[Definition](docs/response_based_definition.md)** | The traditional distillation approach formalized by Geoffrey Hinton et al. | 2015 | [Distilling the Knowledge in a Neural Network](https://arxiv.org/abs/1503.02531) |
| **[Mechanism](docs/response_based_mechanism.md)** | The student directly mimics the final output layer (logits) of the teacher. | 2015 | [Distilling the Knowledge in a Neural Network](https://arxiv.org/abs/1503.02531) |
| **[Soft Targets](docs/response_based_soft_targets.md)** | Uses a "Temperature" parameter to soften output probabilities. | 2015 | [Distilling the Knowledge in a Neural Network](https://arxiv.org/abs/1503.02531) |
| **[Core Benefit](docs/response_based_core_benefit.md)** | Computationally simple; requires only final predictions. | 2015 | [Distilling the Knowledge in a Neural Network](https://arxiv.org/abs/1503.02531) |

---

## 🧩 2. Feature-Based Distillation (Intermediate Layer Distillation) 🧠
*Forcing the student to mimic the internal "thought process" of the teacher.*

| Concept | Details | Year | Paper Link |
| :--- | :--- | :--- | :--- |
| **[Definition](docs/feature_based_definition.md)** | Mimicking the internal representations/feature maps. | 2014 | [FitNets: Hints for Thin Deep Nets](https://arxiv.org/abs/1412.6550) |
| **[Mechanism](docs/feature_based_mechanism.md)** | Aligns hidden layers or attention maps between networks. | 2014 | [FitNets: Hints for Thin Deep Nets](https://arxiv.org/abs/1412.6550) |
| **[FitNets](docs/feature_based_fitnets.md)** | Using "hints" from middle layers to train deeper, thinner students. | 2014 | [FitNets: Hints for Thin Deep Nets](https://arxiv.org/abs/1412.6550) |
| **[Core Benefit](docs/feature_based_core_benefit.md)** | Highly effective for complex tasks like Object Detection. | 2014 | [FitNets: Hints for Thin Deep Nets](https://arxiv.org/abs/1412.6550) |

---

## 🔗 3. Relation-Based Distillation 🕸️
*Transferring structural relationships between different data points or layers.*

| Concept | Details | Year | Paper Link |
| :--- | :--- | :--- | :--- |
| **[Definition](docs/relation_based_definition.md)** | Transfers relationships between multiple data samples. | 2019 | [Relational Knowledge Distillation](https://arxiv.org/abs/1904.05068) |
| **[Mechanism](docs/relation_based_mechanism.md)** | Maps similarity vectors or graphs between samples. | 2019 | [Relational Knowledge Distillation](https://arxiv.org/abs/1904.05068) |
| **[Manifold Learning](docs/relation_based_manifold_learning.md)** | Student learns the geometry of the teacher's feature space. | 2019 | [Relational Knowledge Distillation](https://arxiv.org/abs/1904.05068) |
| **[Core Benefit](docs/relation_based_core_benefit.md)** | Preserves global clustering and embedding logic. | 2019 | [Relational Knowledge Distillation](https://arxiv.org/abs/1904.05068) |

---

## 🔄 4. Self-Distillation 🤳
*A variant where a model acts as its own teacher, needing no external network.*

| Concept | Details | Year | Paper Link |
| :--- | :--- | :--- | :--- |
| **[Definition](docs/self_distillation_definition.md)** | Model acts as its own teacher; no separate large network. | 2018 | [Born-Again Neural Networks](https://arxiv.org/abs/1805.04770) |
| **[Mechanism](docs/self_distillation_mechanism.md)** | Deep layers distill into own shallower, early-exit layers. | 2019 | [Your Own Teacher](https://arxiv.org/abs/1905.08094) |
| **[Data Augmentation](docs/self_distillation_data_augmentation_effect.md)** | Distilling predictions from previous epochs into current ones. | 2019 | [Your Own Teacher](https://arxiv.org/abs/1905.08094) |
| **[Core Benefit](docs/self_distillation_core_benefit.md)** | Improves accuracy without an expensive separate teacher. | 2019 | [Your Own Teacher](https://arxiv.org/abs/1905.08094) |

---

## ⚡ 5. Online & Co-Distillation 🤝
*Teacher and student models are trained simultaneously in parallel.*

| Concept | Details | Year | Paper Link |
| :--- | :--- | :--- | :--- |
| **[Definition](docs/online_co_distillation_definition.md)** | Teacher and student models are trained simultaneously. | 2017 | [Deep Mutual Learning](https://arxiv.org/abs/1706.00384) |
| **[Mechanism](docs/online_co_distillation_mechanism.md)** | Multiple models exchange knowledge dynamically in parallel. | 2017 | [Deep Mutual Learning](https://arxiv.org/abs/1706.00384) |
| **[No Pre-training](docs/online_co_distillation_no_pre_training.md)** | Eliminates the static two-step pre-training pipeline. | 2017 | [Deep Mutual Learning](https://arxiv.org/abs/1706.00384) |
| **[Core Benefit](docs/online_co_distillation_core_benefit.md)** | Prevents performance ceilings caused by static teachers. | 2017 | [Deep Mutual Learning](https://arxiv.org/abs/1706.00384) |

---

## 🛠️ 6. Algorithmic Optimization Variants ⚙️
*Specialized variants for unique tasks and extreme compression.*

| Concept | Details | Year | Paper Link |
| :--- | :--- | :--- | :--- |
| **[Task-Specific KD](docs/algorithmic_task_specific_kd.md)** | Specialized for generative tasks (e.g., LLMs, Stable Diffusion). | 2019 | [DistilBERT](https://arxiv.org/abs/1910.01108) |
| **[Quantization-Aware](docs/algorithmic_quantization_aware_kd.md)** | Combined with bit-width reduction (e.g., 32-bit to 8-bit). | 2017 | [Apprentice](https://arxiv.org/abs/1711.05852) |
| **[Black-Box Distillation](docs/algorithmic_black_box_distillation.md)** | Using only text/API outputs of proprietary models (GPT-4). | 2023 | [Alpaca](https://crfm.stanford.edu/2023/03/13/alpaca.html) |

---

<div align="center">
  <sub>Built with ❤️ for the AI community.</sub>
</div>
