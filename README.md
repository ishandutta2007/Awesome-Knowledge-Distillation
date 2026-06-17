# Awesome-Knowledge-Distillation
## Knowledge Distillation (KD) Variants in AI

Knowledge Distillation transfers dark knowledge from a large, cumbersome "Teacher" network to a compact, deployable "Student" network. This compression technique allows lightweight models to achieve near-server-class performance on edge devices.

## 1. Response-Based Distillation (Logit Distillation)
| Concept | Details | Year | Paper Link |
| :--- | :--- | :--- | :--- |
| **[Definition](docs/response_based_definition.md)** | The traditional distillation approach formalized by Geoffrey Hinton et al. | 2015 | [Distilling the Knowledge in a Neural Network](https://arxiv.org/abs/1503.02531) |
| **[Mechanism](docs/response_based_mechanism.md)** | The student directly mimics the final output layer (logits) of the teacher. | 2015 | [Distilling the Knowledge in a Neural Network](https://arxiv.org/abs/1503.02531) |
| **[Soft Targets](docs/response_based_soft_targets.md)** | Uses a "Temperature" parameter to soften output probabilities, revealing how much the teacher predicts secondary classes. | 2015 | [Distilling the Knowledge in a Neural Network](https://arxiv.org/abs/1503.02531) |
| **[Core Benefit](docs/response_based_core_benefit.md)** | Computationally simple to implement since it only requires access to the teacher's final predictions. | 2015 | [Distilling the Knowledge in a Neural Network](https://arxiv.org/abs/1503.02531) |

## 2. Feature-Based Distillation (Intermediate Layer Distillation)
| Concept | Details | Year | Paper Link |
| :--- | :--- | :--- | :--- |
| **[Definition](docs/feature_based_definition.md)** | Distillation that forces the student to mimic the internal thought process of the teacher. | 2014 | [FitNets: Hints for Thin Deep Nets](https://arxiv.org/abs/1412.6550) |
| **[Mechanism](docs/feature_based_mechanism.md)** | It aligns intermediate hidden layers, feature maps, or attention maps between networks. | 2014 | [FitNets: Hints for Thin Deep Nets](https://arxiv.org/abs/1412.6550) |
| **[FitNets](docs/feature_based_fitnets.md)** | An early breakthrough variant using "hints" from middle layers to train deeper, thinner students. | 2014 | [FitNets: Hints for Thin Deep Nets](https://arxiv.org/abs/1412.6550) |
| **[Core Benefit](docs/feature_based_core_benefit.md)** | Highly effective for complex tasks like Object Detection and Vision Transformers where final logits lack rich spatial awareness. | 2014 | [FitNets: Hints for Thin Deep Nets](https://arxiv.org/abs/1412.6550) |

## 3. Relation-Based Distillation
| Concept | Details | Year | Paper Link |
| :--- | :--- | :--- | :--- |
| **[Definition](docs/relation_based_definition.md)** | Distillation that transfers structural relationships between different data points or layers. | 2019 | [Relational Knowledge Distillation](https://arxiv.org/abs/1904.05068) |
| **[Mechanism](docs/relation_based_mechanism.md)** | Instead of passing single-data knowledge, it maps the similarity, vectors, or graphs between multiple samples. | 2019 | [Relational Knowledge Distillation](https://arxiv.org/abs/1904.05068) |
| **[Manifold Learning](docs/relation_based_manifold_learning.md)** | The student learns the geometry of the feature space developed by the teacher. | 2019 | [Relational Knowledge Distillation](https://arxiv.org/abs/1904.05068) |
| **[Core Benefit](docs/relation_based_core_benefit.md)** | Preserves the global clustering and embedding logic of the teacher model. | 2019 | [Relational Knowledge Distillation](https://arxiv.org/abs/1904.05068) |

## 4. Self-Distillation
| Concept | Details | Year | Paper Link |
| :--- | :--- | :--- | :--- |
| **[Definition](docs/self_distillation_definition.md)** | A variant where a model acts as its own teacher, requiring no separate large network. | 2018 | [Born-Again Neural Networks](https://arxiv.org/abs/1805.04770) |
| **[Mechanism](docs/self_distillation_mechanism.md)** | Deep layers of a model distill knowledge into its own shallower, early-exit layers during training. | 2019 | [Your Own Teacher: A Holistic Approach to Self-distillation](https://arxiv.org/abs/1905.08094) |
| **[Data Augmentation Effect](docs/self_distillation_data_augmentation_effect.md)** | Can also involve distilling a model's predictions from a previous epoch into the current epoch. | 2019 | [Your Own Teacher: A Holistic Approach to Self-distillation](https://arxiv.org/abs/1905.08094) |
| **[Core Benefit](docs/self_distillation_core_benefit.md)** | Significantly improves model accuracy and generalization without needing an expensive teacher model. | 2019 | [Your Own Teacher: A Holistic Approach to Self-distillation](https://arxiv.org/abs/1905.08094) |

## 5. Online & Co-Distillation
| Concept | Details | Year | Paper Link |
| :--- | :--- | :--- | :--- |
| **[Definition](docs/online_co_distillation_definition.md)** | Distillation where the teacher and student models are trained simultaneously. | 2017 | [Deep Mutual Learning](https://arxiv.org/abs/1706.00384) |
| **[Mechanism](docs/online_co_distillation_mechanism.md)** | Multiple models (often peer networks of similar size) train in parallel and exchange knowledge dynamically. | 2017 | [Deep Mutual Learning](https://arxiv.org/abs/1706.00384) |
| **[No Pre-training](docs/online_co_distillation_no_pre_training.md)** | Eliminates the static, computationally heavy two-step pipeline of pre-training a massive teacher first. | 2017 | [Deep Mutual Learning](https://arxiv.org/abs/1706.00384) |
| **[Core Benefit](docs/online_co_distillation_core_benefit.md)** | Prevents the student from hitting a performance ceiling caused by a static teacher. | 2017 | [Deep Mutual Learning](https://arxiv.org/abs/1706.00384) |

## 6. Algorithmic Optimization Variants
| Concept | Details | Year | Paper Link |
| :--- | :--- | :--- | :--- |
| **[Task-Specific KD](docs/algorithmic_task_specific_kd.md)** | Specialized variants designed for generative tasks, such as distilling Large Language Models (LLMs) or Stable Diffusion models into smaller versions. | 2019 | [DistilBERT, a distilled version of BERT](https://arxiv.org/abs/1910.01108) |
| **[Quantization-Aware KD](docs/algorithmic_quantization_aware_kd.md)** | Combines distillation with bit-width reduction (e.g., converting 32-bit floats to 8-bit integers) to achieve extreme model compression. | 2017 | [Apprentice: Using Knowledge Distillation for Training Low-Precision Network](https://arxiv.org/abs/1711.05852) |
| **[Black-Box Distillation](docs/algorithmic_black_box_distillation.md)** | Distillation where only the text/API outputs of a proprietary model (like GPT-4) are used to train an open-source student (like LLaMA fine-tuning). | 2023 | [Alpaca: A Strong, Replicable Instruction-Following Model](https://crfm.stanford.edu/2023/03/13/alpaca.html) |
