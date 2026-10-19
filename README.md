# Awesome-Causality-and-LLMs

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
![Papers](https://img.shields.io/badge/papers-286-4b6bfb)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](#contributing)

> An awesome list of papers delving into **Causality and Large Language Models**.

This repository accompanies the survey **“Causality and Large Language Models: A Survey of System Design, Capabilities, Trustworthiness, and Applications”** by Samar Kale, Vineeth Bekal, Aman Chadha, and Raha Moraffah.

- **Paper:** unpublished manuscript (link coming soon)
- **Project website:** coming soon

## Reference

If you find this collection useful, please cite:

```bibtex
@misc{kale2026causalityllms,
  title  = {Causality and Large Language Models: A Survey of System Design,
            Capabilities, Trustworthiness, and Applications},
  author = {Kale, Samar and Bekal, Vineeth and Chadha, Aman and Moraffah, Raha},
  year   = {2026},
  note   = {Unpublished manuscript}
}
```

## Table of Contents

- [Surveys](#surveys)
- [1. System Design](#1-system-design)
  - [1.1 Post Training](#11-post-training)
    - [1.1.1 Knowledge Editing](#111-knowledge-editing)
    - [1.1.2 Distillation](#112-distillation)
    - [1.1.3 Reinforcement Learning](#113-reinforcement-learning)
  - [1.2 Architecture Design](#12-architecture-design)
    - [1.2.1 Information Retrieval](#121-information-retrieval)
    - [1.2.2 Skill Retrieval](#122-skill-retrieval)
    - [1.2.3 Memory Retrieval](#123-memory-retrieval)
- [2. Capability](#2-capability)
  - [2.1 Generation](#21-generation)
    - [2.1.1 Counterfactual Generation](#211-counterfactual-generation)
    - [2.1.2 Causal Generation](#212-causal-generation)
  - [2.2 Reasoning](#22-reasoning)
    - [2.2.1 Causal Reasoning](#221-causal-reasoning)
      - [2.2.1.1 Causal Discovery](#2211-causal-discovery)
      - [2.2.1.2 Causal Inference](#2212-causal-inference)
      - [2.2.1.3 Counterfactual Reasoning](#2213-counterfactual-reasoning)
    - [2.2.2 Causality for Reasoning](#222-causality-for-reasoning)
      - [2.2.2.1 General Reasoning](#2221-general-reasoning)
      - [2.2.2.2 Multi-Hop Reasoning](#2222-multi-hop-reasoning)
      - [2.2.2.3 Mathematical Reasoning](#2223-mathematical-reasoning)
      - [2.2.2.4 Temporal Reasoning](#2224-temporal-reasoning)
      - [2.2.2.5 Cognitive Reasoning](#2225-cognitive-reasoning)
  - [2.3 Planning and Decision Making](#23-planning-and-decision-making)
    - [2.3.1 Model-Free Systems](#231-model-free-systems)
    - [2.3.2 Environment Modeled Systems](#232-environment-modeled-systems)
- [3. Trustworthiness](#3-trustworthiness)
  - [3.1 Fairness](#31-fairness)
    - [3.1.1 Detection](#311-detection)
    - [3.1.2 Debiasing](#312-debiasing)
  - [3.2 Faithfulness](#32-faithfulness)
    - [3.2.1 Output](#321-output)
    - [3.2.2 Explanation](#322-explanation)
    - [3.2.3 Reasoning](#323-reasoning)
  - [3.3 Interpretability](#33-interpretability)
    - [3.3.1 Instance-Based](#331-instance-based)
    - [3.3.2 Model-Based](#332-model-based)
  - [3.4 Robustness](#34-robustness)
    - [3.4.1 Output](#341-output)
    - [3.4.2 Reasoning](#342-reasoning)
  - [3.5 Unlearning](#35-unlearning)
    - [3.5.1 Modeling](#351-modeling)
    - [3.5.2 Editing](#352-editing)
  - [3.6 Security and Alignment](#36-security-and-alignment)
    - [3.6.1 Attacks](#361-attacks)
    - [3.6.2 Detection](#362-detection)
    - [3.6.3 Defense](#363-defense)
    - [3.6.4 Alignment (Human Values)](#364-alignment-human-values)
- [4. Applications](#4-applications)
  - [4.1 Traditional Causal Analysis](#41-traditional-causal-analysis)
  - [4.2 Data Analysis](#42-data-analysis)
  - [4.3 Scientific Discovery](#43-scientific-discovery)
  - [4.4 Software Engineering](#44-software-engineering)
- [5. Evaluation and Benchmarking](#5-evaluation-and-benchmarking)
  - [5.1 System Design Evaluation](#51-system-design-evaluation)
    - [5.1.1 Post Training](#511-post-training)
    - [5.1.2 Architecture Design](#512-architecture-design)
  - [5.2 Capability Evaluation](#52-capability-evaluation)
    - [5.2.1 Generation](#521-generation)
    - [5.2.2 Reasoning](#522-reasoning)
    - [5.2.3 Planning and Decision Making](#523-planning-and-decision-making)
  - [5.3 Trustworthiness Evaluation](#53-trustworthiness-evaluation)
    - [5.3.1 Fairness](#531-fairness)
    - [5.3.2 Faithfulness](#532-faithfulness)
    - [5.3.3 Interpretability](#533-interpretability)
    - [5.3.4 Robustness](#534-robustness)
    - [5.3.5 Unlearning](#535-unlearning)
    - [5.3.6 Security and Alignment](#536-security-and-alignment)
  - [5.4 Application Evaluation](#54-application-evaluation)
    - [5.4.1 Traditional Causal Analysis](#541-traditional-causal-analysis)
    - [5.4.2 Data Analysis](#542-data-analysis)
    - [5.4.3 Scientific Discovery](#543-scientific-discovery)
    - [5.4.4 Software Engineering](#544-software-engineering)
- [Additional Papers](#additional-papers)
- [Contributing](#contributing)

## Surveys

- **Understanding Causality with Large Language Models: Feasibility and Opportunities** [[Paper]](<https://arxiv.org/abs/2304.05524>)
- **Causal Parrots: Large Language Models May Talk Causality But Are Not Causal** [[Paper]](<https://openreview.net/forum?id=tv46tCzs83>)
- **Causal Reasoning and Large Language Models: Opening a New Frontier for Causality** [[Paper]](<https://openreview.net/forum?id=mqoxLkX210>)
- **Causality for Large Language Models** [[Paper]](<https://arxiv.org/abs/2410.15319>)
- **The Odyssey of Commonsense Causality: From Foundational Benchmarks to Cutting-Edge Reasoning** [[Paper]](<https://aclanthology.org/2024.emnlp-main.932/>)
- **Causal Inference with Large Language Model: A Survey** [[Paper]](<https://aclanthology.org/2025.findings-naacl.327/>)
- **Large Language Models and Causal Inference in Collaboration: A Comprehensive Survey** [[Paper]](<https://aclanthology.org/2025.findings-naacl.427/>)
- **CausalEval: Towards Better Causal Reasoning in Language Models** [[Paper]](<https://aclanthology.org/2025.naacl-long.622/>)
- **Uncertainty in Causality: A New Frontier** [[Paper]](<https://aclanthology.org/2025.acl-long.396/>)
- **Causal MAS: A Survey of Large Language Model Architectures for Discovery and Effect Estimation** [[Paper]](<https://arxiv.org/abs/2509.00987>)
- **Large Language Models for Causal Discovery: Current Landscape and Future Directions** [[Paper]](<https://www.ijcai.org/proceedings/2025/1186.pdf>)
- **Causal methods for LLM development and evaluation** [[Paper]](<https://arxiv.org/abs/2605.25998>)
- **A Survey on Enhancing Causal Reasoning Ability of Large Language Models** [[Paper]](<https://arxiv.org/abs/2503.09326v1>)

## 1. System Design

### 1.1 Post Training

#### 1.1.1 Knowledge Editing

- **From Fact Overwriting to Knowledge Evolution: Causal Editing via On-Policy Self-Distillation** [[Paper]](<https://arxiv.org/abs/2605.28303>)
- **CAKE: Causal-Guided Adaptive Knowledge Editing for LLMs** [[Paper]](<https://aclanthology.org/2026.acl-long.918/>)
- **Pruning via Causal Attribution Preserves Reasoning Performance in Large Language Models** [[Paper]](<https://openreview.net/forum?id=yH7yrtUwbp>)

#### 1.1.2 Distillation

- **Learning to Focus: Causal Attention Distillation via Gradient-Guided Token Pruning** [[Paper]](<https://proceedings.neurips.cc/paper_files/paper/2025/hash/236264ac647eef86b41991d53452fd0b-Abstract-Conference.html>)

#### 1.1.3 Reinforcement Learning

- **Group Causal Policy Optimization for Post-Training Large Language Models** [[Paper]](<https://arxiv.org/abs/2508.05428v1>)

### 1.2 Architecture Design

#### 1.2.1 Information Retrieval

- **CausalRAG2: Hierarchical Causal Knowledge Graph Design for RAG** [[Paper]](<https://openreview.net/forum?id=F2zHYjBAEv>)
- **CausalRAG: Integrating Causal Graphs into Retrieval-Augmented Generation** [[Paper]](<https://aclanthology.org/2025.findings-acl.1165/>)
- **Structure Over Scale: Schema-Constrained Causal Graphs for RAG** [[Paper]](<https://arxiv.org/abs/2607.22592v1>)

#### 1.2.2 Skill Retrieval

- **CaSKG: Counterfactual-Causal Skill Graphs for Scalable Agent Skill Retrieval** [[Paper]](<https://arxiv.org/abs/2608.25500v1>)

#### 1.2.3 Memory Retrieval

- **Causal Intervention-Based Memory Selection for Long-Horizon LLM Agents** [[Paper]](<https://arxiv.org/abs/2605.17641>)
- **ActMem: Bridging the Gap Between Memory Retrieval and Reasoning in LLM Agents** [[Paper]](<https://arxiv.org/abs/2603.00026>)

## 2. Capability

### 2.1 Generation

#### 2.1.1 Counterfactual Generation

- **Episodic Memory Retrieval from LLMs: A Neuromorphic Mechanism to Generate Commonsense Counterfactuals for Relation Extraction** [[Paper]](<https://aclanthology.org/2024.findings-acl.146/>)
- **Counterfactual Token Generation in Large Language Models** [[Paper]](<https://arxiv.org/pdf/2409.17027>)
- **Gumbel Counterfactual Generation From Language Models** [[Paper]](<https://openreview.net/forum?id=TUC0ZT2zIQ>)
- **Guiding LLMs to Generate High-Fidelity and High-Quality Counterfactual Explanations for Text Classification** [[Paper]](<https://arxiv.org/abs/2503.04463v2>)
- **Dually Self-Improved Counterfactual Data Augmentation Using Large Language Model** [[Paper]](<https://aclanthology.org/2025.acl-long.260/>)

#### 2.1.2 Causal Generation

- **Language Models as Causal Effect Generators** [[Paper]](<https://aclanthology.org/2025.emnlp-main.107.pdf>)

### 2.2 Reasoning

#### 2.2.1 Causal Reasoning

##### 2.2.1.1 Causal Discovery

- **Efficient Causal Graph Discovery Using Large Language Models** [[Paper]](<https://openreview.net/forum?id=5RBUTx75yr>)
- **Causal Order: The Key to Leveraging Imperfect Experts in Causal Inference** [[Paper]](<https://openreview.net/forum?id=3fzCBL6ar7>)
- **Structured Thinking Matters: Improving LLMs Generalization in Causal Inference Tasks** [[Paper]](<https://arxiv.org/abs/2505.18034v2>)
- **Causal-LLM: A Unified One-Shot Framework for Prompt- and Data-Driven Causal Graph Discovery** [[Paper]](<https://aclanthology.org/2025.findings-emnlp.439/>)
- **Step-by-Step Causality: Transparent Causal Discovery with Multi-Agent Tree-Query and Adversarial Confidence Estimation** [[Paper]](<https://arxiv.org/abs/2601.10137>)
- **ChatCEE: a causality extraction framework based on large language model** [[Paper]](<https://link.springer.com/article/10.1007/s10799-026-00484-7>)
- **Paths to Causality: Finding Informative Subgraphs Within Knowledge Graphs for Knowledge-Based Causal Discovery** [[Paper]](<https://dl.acm.org/doi/10.1145/3711896.3737076>)
- **CAT: Causal Attention Tuning For Injecting Fine-grained Causal Knowledge into Large Language Models** [[Paper]](<https://arxiv.org/abs/2509.01535v2>)
- **Causal Reasoning in Large Language Models: A Knowledge Graph Approach** [[Paper]](<https://arxiv.org/pdf/2410.11588>)
- **C2P: Featuring Large Language Models with Causal Reasoning** [[Paper]](<https://arxiv.org/pdf/2407.18069>)
- **Multi-Agent Causal Discovery Using Large Language Models** [[Paper]](<https://openreview.net/forum?id=Idygh9MX0N>)

##### 2.2.1.2 Causal Inference

- **DoubleLingo: Causal Estimation with Large Language Models** [[Paper]](<https://aclanthology.org/2024.naacl-short.71/>)
- **Teaching Transformers Causal Reasoning through Axiomatic Training** [[Paper]](<https://openreview.net/forum?id=vnFtU3fO9h>)
- **Estimating Causal Effects of Text Interventions Leveraging LLMs** [[Paper]](<https://aclanthology.org/2025.findings-ijcnlp.10/>)
- **Causal-Audit: Explicit and Auditable Graph-based Reasoning via Target-Aware Causal Chain Construction** [[Paper]](<https://aclanthology.org/2026.findings-acl.607.pdf>)

##### 2.2.1.3 Counterfactual Reasoning

- **Reasoning Elicitation in Language Models via Counterfactual Feedback** [[Paper]](<https://proceedings.iclr.cc/paper_files/paper/2025/hash/bf145010b30dc5f14fa87dc152074e4d-Abstract-Conference.html>)
- **Abstract Counterfactuals for Language Model Agents** [[Paper]](<https://openreview.net/forum?id=ifMZw5fm7K>)
- **Executable Counterfactuals: Improving LLMs' Causal Reasoning Through Code** [[Paper]](<https://openreview.net/forum?id=Lm46gJA0q8>)

#### 2.2.2 Causality for Reasoning

##### 2.2.2.1 General Reasoning

- **Causal Sufficiency and Necessity Improves Chain-of-Thought Reasoning** [[Paper]](<https://proceedings.neurips.cc/paper_files/paper/2025/hash/b7870bd43b2d133a1ed95582ae5d82a4-Abstract-Conference.html>)

##### 2.2.2.2 Multi-Hop Reasoning

- **Counterfactual Multihop QA: A Cause-Effect Approach for Reducing Disconnected Reasoning** [[Paper]](<https://aclanthology.org/2023.acl-long.231/>)

##### 2.2.2.3 Mathematical Reasoning

- **CAMA: Enhancing Mathematical Reasoning in Large Language Models with Causal Knowledge** [[Paper]](<https://ojs.aaai.org/index.php/AAAI/article/view/40756/>)

##### 2.2.2.4 Temporal Reasoning

- **Counterfactual-Consistency Prompting for Relative Temporal Understanding in Large Language Models** [[Paper]](<https://aclanthology.org/2025.acl-short.97/>)

##### 2.2.2.5 Cognitive Reasoning

- **Large Language Models as Theory of Mind Aware Generative Agents with Counterfactual Reflection** [[Paper]](<https://arxiv.org/abs/2501.15355v1>)
- **CoSToM: Causal-oriented Steering for Intrinsic Theory-of-Mind Alignment in Large Language Models** [[Paper]](<https://aclanthology.org/2026.acl-long.421/>)
- **SOM: Structured Opponent Modeling for LLM-based Agents via Structural Causal Model** [[Paper]](<https://arxiv.org/abs/2605.07301v1>)

### 2.3 Planning and Decision Making

#### 2.3.1 Model-Free Systems

- **CausalPlan: Empowering Efficient LLM Multi-Agent Collaboration Through Causality-Driven Planning** [[Paper]](<https://openreview.net/forum?id=Zk87VXBW8A>)
- **ARGORA: Orchestrated Argumentation for Causally Grounded LLM Reasoning and Decision Making** [[Paper]](<https://arxiv.org/abs/2601.21533>)
- **CausalMACE: Causality Empowered Multi-Agents in Minecraft Cooperative Tasks** [[Paper]](<https://aclanthology.org/2025.findings-emnlp.777/>)

#### 2.3.2 Environment Modeled Systems

- **Language Agents Meet Causality – Bridging LLMs and Causal World Models** [[Paper]](<https://openreview.net/forum?id=y9A2TpaGsE>)
- **Causal-aware large language models: enhancing decision-making through learning, adapting and acting** [[Paper]](<https://www.ijcai.org/proceedings/2025/0478>)
- **Should I Have Expressed a Different Intent? Counterfactual Generation for LLM-Based Autonomous Control** [[Paper]](<https://openreview.net/forum?id=fKsDQLjyIb>)
- **Counterfactual Planning for Generalizable Agents’ Actions** [[Paper]](<https://ojs.aaai.org/index.php/AAAI/article/view/40184>)

## 3. Trustworthiness

### 3.1 Fairness

#### 3.1.1 Detection

- **Uncovering Bias Paths with LLM-guided Causal Discovery: An Active Learning and Dynamic Scoring Approach** [[Paper]](<https://ojs.aaai.org/index.php/AAAI/article/view/41308>)
- **Toward Systematic Counterfactual Fairness Evaluation of Large Language Models: The CAFFE Framework** [[Paper]](<https://dl.acm.org/doi/10.1145/3744916.3787848>)
- **Unbiased Evaluation of Large Language Models from a Causal Perspective** [[Paper]](<https://proceedings.mlr.press/v267/chen25bi.html>)

#### 3.1.2 Debiasing

- **A Causal Explainable Guardrails for Large Language Models** [[Paper]](<https://dl.acm.org/doi/abs/10.1145/3658644.3690217>)
- **Prompting Fairness: Integrating Causality to Debias Large Language Models** [[Paper]](<https://openreview.net/forum?id=7GKbQ1WT1C>)
- **Causal Prompting: Debiasing Large Language Models based on Front-Door Adjustment** [[Paper]](<https://ojs.aaai.org/index.php/AAAI/article/view/34777>)
- **Unbiased Reasoning for Knowledge-Intensive Tasks in Large Language Models via Conditional Front-Door Adjustment** [[Paper]](<https://arxiv.org/abs/2508.16910v1>)
- **Debiasing Large Language Models via Adaptive Causal Prompting with Sketch-of-Thought** [[Paper]](<https://arxiv.org/abs/2601.08108v1>)
- **CFL: Causally Fair Language Models Through Token-level Attribute Controlled Generation** [[Paper]](<https://aclanthology.org/2023.findings-acl.720>)
- **C2PO: Diagnosing and Disentangling Bias Shortcuts in LLMs** [[Paper]](<https://aclanthology.org/2026.findings-acl.1226>)
- **Aligning as Debiasing: Causality-Aware Alignment via Reinforcement Learning with Interventional Feedback** [[Paper]](<https://aclanthology.org/2024.naacl-long.262>)
- **DeCoT: Debiasing Chain-of-Thought for Knowledge-Intensive Tasks in Large Language Models via Causal Intervention** [[Paper]](<https://aclanthology.org/2024.acl-long.758>)
- **STEERING LLMS TOWARDS UNBIASED RESPONSES: A CAUSALITY-GUIDED DEBIASING FRAMEWORK** [[Paper]](<https://openreview.net/pdf?id=RYdozB0GdB>)

### 3.2 Faithfulness

#### 3.2.1 Output

- **Causal What-Ifs: Rethinking Counterfactuals with LLM Agents** [[Paper]](<https://link.springer.com/chapter/10.1007/978-981-95-4367-0_13>)
- **Counterfactual Probing for Hallucination Detection and Mitigation in Large Language Models** [[Paper]](<https://arxiv.org/abs/2508.01862v1>)
- **Hallucinate Less by Thinking More: Aspect-Based Causal Abstention for Large Language Models** [[Paper]](<https://arxiv.org/abs/2511.17170v1>)

#### 3.2.2 Explanation

- **Walk the Talk? Measuring the Faithfulness of Large Language Model Explanations** [[Paper]](<https://openreview.net/forum?id=4ub9gpx9xw>)
- **LLMs Don’t Know Their Own Decision Boundaries: The Unreliability of Self-Generated Counterfactual Explanations** [[Paper]](<https://aclanthology.org/2025.emnlp-main.1231/>)
- **Do Models Explain Themselves? Counterfactual Simulatability of Natural Language Explanations** [[Paper]](<https://proceedings.mlr.press/v235/chen24bl.html>)
- **Are self-explanations from Large Language Models faithful?** [[Paper]](<https://aclanthology.org/2024.findings-acl.19/>)
- **Counterfactual Simulatability of LLM Explanations for Generation Tasks** [[Paper]](<https://aclanthology.org/2025.inlg-main.38/>)
- **Would this change your answer? Evaluating Explanations of LLM Behavior In The Wild with Counterfactual Experiments** [[Paper]](<https://arxiv.org/abs/2608.16747v1>)

#### 3.2.3 Reasoning

- **Grounding Multi-Hop Reasoning in Structural Causal Models via Group Relative Policy Optimization** [[Paper]](<https://openreview.net/forum?id=vfIUEpSTji>)
- **Mitigating Hallucinations in Large Language Models via Causal Reasoning** [[Paper]](<https://ojs.aaai.org/index.php/AAAI/article/view/40454>)
- **CASE: Causal Alignment and Structural Enforcement for Improving Chain-of-Thought Faithfulness** [[Paper]](<https://arxiv.org/pdf/2607.18820>)
- **FRIT: Using Causal Importance to Improve Chain-of-Thought Faithfulnes** [[Paper]](<https://arxiv.org/pdf/2509.13334>)
- **On the Causal Identifiability of Chain-of-Thought in Language Models** [[Paper]](<https://www.techrxiv.org/doi/full/10.36227/techrxiv.176153550.09433591/v1>)
- **CausalGPT: Illuminating Faithfulness and Causality for Knowledge Reasoning with Foundation Models** [[Paper]](<https://arxiv.org/pdf/2308.11914>)

### 3.3 Interpretability

#### 3.3.1 Instance-Based

- **Faithful Explanations of Black-box NLP Models Using LLM-generated Counterfactuals** [[Paper]](<https://openreview.net/forum?id=UMfcdRIotC>)
- **LLM Explainability with Counterfactual Chains and Causal Graphs** [[Paper]](<https://arxiv.org/abs/2606.05972v1>)

#### 3.3.2 Model-Based

- **Competition of Mechanisms: Tracing How Language Models Handle Facts and Counterfactuals** [[Paper]](<https://aclanthology.org/2024.acl-long.458/>)
- **CodeSCM: Causal Analysis for Multi-Modal Code Generation** [[Paper]](<https://aclanthology.org/2025.naacl-long.345/>)
- **Counterfactual Effect Decomposition in Multi-Agent Sequential Decision Making** [[Paper]](<https://openreview.net/forum?id=jHLSnYNt1m>)
- **Causality-Aided Evaluation and Explanation of Large Language Model-Based Code Generation** [[Paper]](<https://dl.acm.org/doi/abs/10.1145/3728938>)
- **CAM: A Causality-based Analysis Framework for Multi-Agent Code Generation Systems** [[Paper]](<https://arxiv.org/abs/2602.02138>)
- **CausalFlow: Causal Attribution and Counterfactual Repair for LLM Agent Failures** [[Paper]](<https://arxiv.org/abs/2605.25338>)
- **Do Large Code Models Understand Programming Concepts? Counterfactual Analysis for Code Predicates** [[Paper]](<https://dl.acm.org/doi/10.5555/3692070.3692823>)
- **Causal abstraction: a theoretical foundation for mechanistic interpretability** [[Paper]](<https://dl.acm.org/doi/10.5555/3814246.3814329>)
- **Locating and editing factual associations in GPT** [[Paper]](<https://dl.acm.org/doi/10.5555/3600270.3601532>)
- **Explaining Fine Tuned LLMs via Counterfactuals A Knowledge Graph Driven Framework** [[Paper]](<https://openreview.net/forum?id=JpmVfZR3la>)
- **Multi-component Causal Tracing in Large Language Models** [[Paper]](<https://arxiv.org/abs/2606.03085v2>)
- **Causal Differentiating Concepts: Interpreting LM Behavior via Causal Representation Learning** [[Paper]](<https://proceedings.neurips.cc/paper_files/paper/2025/hash/5faf0f518f39e4d6b2b595e3ca2fe0c4-Abstract-Conference.html>)
- **Causal Agent Replay: Counterfactual Attribution for LLM-Agent Failures** [[Paper]](<https://arxiv.org/pdf/2606.08275>)
- **LLMs as Counterfactual Explanation Modules: Can ChatGPT Explain Black-box Text Classifiers?** [[Paper]](<https://arxiv.org/html/2309.13340v1>)

### 3.4 Robustness

#### 3.4.1 Output

- **Boosting Resilience of Large Language Models through Causality-Driven Robust Optimization** [[Paper]](<https://proceedings.neurips.cc/paper_files/paper/2025/hash/50d277e84b2bcbaadcd84548a87e8cc4-Abstract-Conference.html>)
- **Causal Fine-Tuning under Latent Confounded Shift** [[Paper]](<https://openreview.net/forum?id=NDPvfDxsz4>)

#### 3.4.2 Reasoning

- **Teaching Small Language Models Reasoning through Counterfactual Distillation** [[Paper]](<https://aclanthology.org/2024.emnlp-main.333/>)
- **Can Large Language Models Learn Independent Causal Mechanisms?** [[Paper]](<https://aclanthology.org/2024.emnlp-main.381/>)
- **Towards Generalizable Reasoning: Group Causal Counterfactual Policy Optimization for LLM Reasoning** [[Paper]](<https://openreview.net/forum?id=w7zWxdLHWD>)
- **CDF-RAG: Causal Dynamic Feedback for Adaptive Retrieval-Augmented Generation** [[Paper]](<https://arxiv.org/abs/2504.12560v1>)
- **CARE: Causally-Aligned Reasoning Exploration for Medical Large Language Models** [[Paper]](<https://arxiv.org/abs/2608.26147v1>)

### 3.5 Unlearning

#### 3.5.1 Modeling

- **Revisiting Who's Harry Potter: Towards Targeted Unlearning from a Causal Intervention Perspective** [[Paper]](<https://arxiv.org/abs/2407.16997>)
- **CiPO: Counterfactual Unlearning for Large Reasoning Models through Iterative Preference Optimization** [[Paper]](<https://arxiv.org/abs/2604.15847>)

#### 3.5.2 Editing

- **CausalDetox: Causal Head Selection and Intervention for Language Model Detoxification** [[Paper]](<https://arxiv.org/abs/2604.14602>)
- **KUDA: Knowledge Unlearning by Deviating Representation for Large Language Models** [[Paper]](<https://arxiv.org/abs/2602.19275>)

### 3.6 Security and Alignment

#### 3.6.1 Attacks

- **Causal Front-Door Adjustment for Robust Jailbreak Attacks on LLMs** [[Paper]](<https://arxiv.org/abs/2602.05444v2>)

#### 3.6.2 Detection

- **Counterfactual Evaluation for Blind Attack Detection in LLM-based Evaluation Systems** [[Paper]](<https://aclanthology.org/2025.ijcnlp-long.33/>)
- **Enhancing LLM Agent Safety via Causal Influence Prompting** [[Paper]](<https://aclanthology.org/2025.findings-acl.784/>)
- **Ghost in the Agent: Redefining Information Flow Tracking for LLM Agents** [[Paper]](<https://arxiv.org/abs/2604.23374v1>)
- **LLMScan: Causal Scan for LLM Misbehavior Detection** [[Paper]](<https://proceedings.mlr.press/v267/zhang25al.html>)

#### 3.6.3 Defense

- **Causality Based Front-door Defense Against Backdoor Attack on Language Models** [[Paper]](<https://openreview.net/forum?id=dmHHVcHFdM>)
- **AgentSentry: Mitigating Indirect Prompt Injection in LLM Agents via Temporal Causal Diagnostics and Context Purification** [[Paper]](<https://arxiv.org/abs/2602.22724>)
- **AttriGuard: Defeating Indirect Prompt Injection in LLM Agents via Causal Attribution of Tool Invocations** [[Paper]](<https://arxiv.org/abs/2603.10749>)

#### 3.6.4 Alignment (Human Values)

- **Counterfactual Reasoning for Steerable Pluralistic Value Alignment of Large Language Models** [[Paper]](<https://proceedings.neurips.cc/paper_files/paper/2025/hash/b0916c29bc32d57e2c86a63e8f2df9f2-Abstract-Conference.html>)
- **Preference Learning for AI Alignment: a Causal Perspective** [[Paper]](<https://proceedings.mlr.press/v267/kobalczyk25a.html>)
- **Optimizing Language Models for Human Preferences is a Causal Inference Problem** [[Paper]](<https://openreview.net/forum?id=VmI8qE0UK6>)

## 4. Applications

### 4.1 Traditional Causal Analysis

- **Discovery of the Hidden World with Large Language Models** [[Paper]](<https://papers.nips.cc/paper_files/paper/2024/hash/b99a07486702417d3b1bd64ec2cf74ad-Abstract-Conference.html>)
- **Causal Modelling Agents: Causal Graph Discovery through Synergising Metadata- and Data-Driven Reasoning** [[Paper]](<https://openreview.net/forum?id=pAoqRlTBtY>)
- **LLM4Causal: Democratized Causal Tools for Everyone via Large Language Model** [[Paper]](<https://openreview.net/forum?id=H1Edd5d2JP>)
- **Cause and Effect: Can Large Language Models Truly Understand Causality?** [[Paper]](<https://ojs.aaai.org/index.php/AAAI-SS/article/view/31764>)
- **On Incorporating Prior Knowledge Extracted from Pre-trained Language Models into Causal Discovery** [[Paper]](<https://openreview.net/forum?id=lZLwoWXVWy>)
- **LLM-initialized Differentiable Causal Discovery** [[Paper]](<https://openreview.net/forum?id=2gENrLD5nn>)
- **End-To-End Causal Effect Estimation from Unstructured Natural Language Data** [[Paper]](<https://proceedings.neurips.cc/paper_files/paper/2024/hash/8d2aad53fa148791ffd004a7c9cce5ad-Abstract-Conference.html>)
- **LLM-Driven Causal Discovery via Harmonized Prior** [[Paper]](<https://ieeexplore.ieee.org/abstract/document/10839116>)
- **LLM-GC: Advancing Granger Causal Discovery from Time Series with Multimodel Language Modeling** [[Paper]](<https://dl.acm.org/doi/abs/10.1145/3773966.3777994>)
- **Integrating Large Language Model for Improved Causal Discovery** [[Paper]](<https://ieeexplore.ieee.org/abstract/document/10966043?casa_token=qZPioYUR9NYAAAAA:IxJC-l6s7us8ksejJIWMDBNrzvL8Jm4tT-iBTjjX6OdlDWtxJigvZtt8oIv6dA3HrtqOVpgcJg>)
- **ALCM: Autonomous LLM-Augmented Causal Discovery Framework** [[Paper]](<https://arxiv.org/abs/2405.01744>)
- **Causal-Copilot: An Autonomous Causal Analysis Agent with Large Language Models** [[Paper]](<https://arxiv.org/abs/2504.13263>)
- **Integrating Large Language Models in Causal Discovery: A Statistical Causal Approach** [[Paper]](<https://openreview.net/forum?id=Reh1S8rxfh>)
- **Causal Discovery through Synergizing Large Language Model and Data-Driven Reasoning** [[Paper]](<https://dl.acm.org/doi/abs/10.1145/3711896.3736874>)
- **LLM-Augmented Causal Discovery with Order Conflict Resolution** [[Paper]](<https://ieeexplore.ieee.org/abstract/document/11320707>)
- **CARE: Turning LLMs Into Causal Reasoning Expert** [[Paper]](<https://openreview.net/forum?id=EC7B1nlK9j>)
- **Leveraging Large Language Models for Causal Discovery: a Constraint-based, Argumentation-driven Approach** [[Paper]](<https://arxiv.org/abs/2602.16481>)
- **Causality by Abstraction: Symbolic Rule Learning in Multivariate Timeseries with Large Language Models** [[Paper]](<https://arxiv.org/abs/2602.17829>)
- **Retrieving Classes of Causal Orders with Inconsistent Knowledge Bases** [[Paper]](<https://arxiv.org/abs/2412.14019v4>)
- **Counterfactual Causal Inference in Natural Language with Large Language Models** [[Paper]](<https://openreview.net/forum?id=ldnKzNQ5l0>)
- **HOLOGRAPH: Active Causal Discovery via Sheaf-Theoretic Alignment of Large Language Model Priors** [[Paper]](<https://arxiv.org/abs/2512.24478v2>)
- **IRIS: An Iterative and Integrated Framework for Verifiable Causal Discovery in the Absence of Tabular Data** [[Paper]](<https://arxiv.org/abs/2510.09217v1>)
- **LLM-based Agents for Automated Confounder Discovery and Subgroup Analysis in Causal Inference** [[Paper]](<https://www.computer.org/csdl/proceedings-article/iri/2025/994400a265/29WVuKREtSE>)
- **Learning to Defer for Causal Discovery with Imperfect Experts** [[Paper]](<https://arxiv.org/abs/2502.13132v1>)
- **Technical Report: Facilitating the Adoption of Causal Inference Methods Through LLM-Empowered Co-Pilot** [[Paper]](<https://arxiv.org/abs/2508.10581v1>)
- **CauSim: Scaling Causal Reasoning with Increasingly Complex Causal Simulators** [[Paper]](<https://arxiv.org/abs/2605.09079v1>)
- **RealTCD: Temporal Causal Discovery from Interventional Data with Large Language Model** [[Paper]](<https://arxiv.org/abs/2404.14786v2>)

### 4.2 Data Analysis

- **Do LLMs Think Fast and Slow? A Causal Study on Sentiment Analysis** [[Paper]](<https://aclanthology.org/2024.findings-emnlp.547/>)
- **Are Large Language Models Capable of Causal Reasoning for Sensing Data Analysis?** [[Paper]](<https://dl.acm.org/doi/abs/10.1145/3662006.3662064>)
- **LoCal: Logical and Causal Fact-Checking with LLM-Based Multi-Agents** [[Paper]](<https://dl.acm.org/doi/abs/10.1145/3696410.3714748>)
- **Effective Use of LLMs via Counterfactual Reasoning for Transparent Recommendation Explanations** [[Paper]](<https://link.springer.com/chapter/10.1007/978-3-032-13562-9_20>)
- **ARCADIA: Scalable Causal Discovery for Corporate Bankruptcy Analysis Using Agentic AI** [[Paper]](<https://arxiv.org/abs/2512.00839v1>)
- **Augur: Modeling Covariate Causal Associations in Time Series via Large Language Models** [[Paper]](<https://arxiv.org/abs/2510.07858v2>)
- **Causal Inference based Transfer Learning with LLMs: An Efficient Framework for Industrial RUL Prediction** [[Paper]](<https://arxiv.org/abs/2503.17686v1>)
- **Causal Prompting for Implicit Sentiment Analysis with Large Language Models** [[Paper]](<https://arxiv.org/abs/2507.00389v1>)
- **Enhancing Temporal Sensitivity of Large Language Model for Recommendation with Counterfactual Tuning** [[Paper]](<https://arxiv.org/abs/2507.03047v2>)
- **Interpreting Public Sentiment in Diplomacy Events: A Counterfactual Analysis Framework Using Large Language Models** [[Paper]](<https://arxiv.org/abs/2509.20367v1>)
- **MedCoT-RAG: Causal Chain-of-Thought RAG for Medical Question Answering** [[Paper]](<https://arxiv.org/abs/2508.15849v1>)
- **Retrieval Augmented Generation based Large Language Models for Causality Mining** [[Paper]](<https://arxiv.org/abs/2505.23944v1>)
- **Large Language Models for Causal Relations Extraction in Social Media: A Validation Framework for Disaster Intelligence** [[Paper]](<https://arxiv.org/abs/2605.11348v1>)
- **CausalTAD: Injecting Causal Knowledge into Large Language Models for Tabular Anomaly Detection** [[Paper]](<https://arxiv.org/abs/2602.07798v1>)
- **Causal Evidence Extraction and Triangulation in Crisis Reports using Large Language Models: A ReliefWeb-based Study** [[Paper]](<https://arxiv.org/abs/2608.04576v1>)
- **CAMO: An Agentic Framework for Automated Causal Discovery from Micro Behaviors to Macro Emergence in LLM Agent Simulations** [[Paper]](<https://aclanthology.org/2026.findings-acl.1224>)

### 4.3 Scientific Discovery

- **Can Large Language Models Help Experimental Design for Causal Discovery?** [[Paper]](<https://openreview.net/forum?id=72I1ln3Ee3>)
- **Causal AI Scientist: Facilitating Causal Data Science with Large Language Models** [[Paper]](<https://openreview.net/forum?id=EDWTHMVOCj>)
- **CauScientist: Teaching LLMs to Respect Data for Causal Discovery** [[Paper]](<https://arxiv.org/abs/2601.13614>)
- **IV Co-Scientist: Multi-Agent LLM Framework for Causal Instrumental Variable Discovery** [[Paper]](<https://openreview.net/forum?id=m4zveElZiD#discussion>)

### 4.4 Software Engineering

- **ECCO: Evidence-Driven Causal Reasoning for Compiler Optimization** [[Paper]](<https://openreview.net/forum?id=YvqOTT5S9Y>)
- **From Gameplay Traces to Game Mechanics: Causal Induction with Large Language Models** [[Paper]](<https://arxiv.org/abs/2602.00190>)
- **Enhancing Automated Grading in Science Education through LLM-Driven Causal Reasoning and Multimodal Analysis** [[Paper]](<https://www.ijcai.org/proceedings/2025/1150>)
- **CausalTrace: A Neurosymbolic Causal Analysis Agent for Smart Manufacturing** [[Paper]](<https://ojs.aaai.org/index.php/AAAI/article/view/41486>)
- **CausalRepair: Bridging the Causality Gap in Large Language Model-Based Automated Program Repair via Dual-Slicing** [[Paper]](<https://arxiv.org/abs/2608.10613v1>)

## 5. Evaluation and Benchmarking

### 5.1 System Design Evaluation

#### 5.1.1 Post Training

- **Can Post-Training Transform LLMs into Causal Reasoners?** [[Paper]](<https://aclanthology.org/2026.findings-acl.839/>)
- **Architecture-Dependent Causal Transfer of Activation States Across Large Language Models** [[Paper]](<https://arxiv.org/abs/2608.16347v1>)

#### 5.1.2 Architecture Design

- **ARCHITECT: Uncertainty-Aware Dynamic Tool Learning via Causal Intervention for Open-World Agents** [[Paper]](<https://aclanthology.org/2026.acl-long.1707>)

### 5.2 Capability Evaluation

#### 5.2.1 Generation

- **Prompting Large Language Models for Counterfactual Generation: An Empirical Study** [[Paper]](<https://aclanthology.org/2024.lrec-main.1156/>)
- **CLOMO: Counterfactual Logical Modification with Large Language Models** [[Paper]](<https://aclanthology.org/2024.acl-long.593/>)
- **LLMs for Generating and Evaluating Counterfactuals: A Comprehensive Study** [[Paper]](<https://aclanthology.org/2024.findings-emnlp.870/>)
- **On Causal and Anticausal LLM-based Data Synthesis** [[Paper]](<https://dl.acm.org/doi/abs/10.1145/3773966.3779380>)
- **CEval: A Benchmark for Evaluating Counterfactual Text Generation** [[Paper]](<https://aclanthology.org/2024.inlg-main.6/>)
- **Counterfactual Modeling with Fine-Tuned LLMs for Health Intervention Design and Sensor Data Augmentation** [[Paper]](<https://arxiv.org/abs/2601.14590v3>)
- **Zero-shot LLM-guided Counterfactual Generation: A Case Study on NLP Model Evaluation** [[Paper]](<https://ieeexplore.ieee.org/abstract/document/10825537>)

#### 5.2.2 Reasoning

- **The Magic of IF: Investigating Causal Reasoning Abilities in Large Language Models of Code** [[Paper]](<https://aclanthology.org/2023.findings-acl.574/>)
- **Counterfactual reasoning: Testing language models’ understanding of hypothetical scenarios** [[Paper]](<https://aclanthology.org/2023.acl-short.70/>)
- **CRAB: Assessing the Strength of Causal Relationships Between Real-world Events** [[Paper]](<https://aclanthology.org/2023.emnlp-main.940/>)
- **CLadder: Assessing Causal Reasoning in Language Models** [[Paper]](<https://neurips.cc/virtual/2023/poster/70983>)
- **Can Large Language Models Infer Causation from Correlation?** [[Paper]](<https://openreview.net/pdf?id=vqIH0ObdqL>)
- **MalAlgoQA: Pedagogical Evaluation of Counterfactual Reasoning in Large Language Models and Implications for AI in Education** [[Paper]](<https://aclanthology.org/2024.findings-emnlp.913/>)
- **Are LLMs Capable of Data-based Statistical and Causal Reasoning? Benchmarking Advanced Quantitative Reasoning with Data** [[Paper]](<https://aclanthology.org/2024.findings-acl.548/>)
- **CausalBench: A Comprehensive Benchmark for Evaluating Causal Reasoning Capabilities of Large Language Models** [[Paper]](<https://aclanthology.org/2024.sighan-1.17/>)
- **COLD: Causal reasOning in cLosed Daily activities** [[Paper]](<https://proceedings.neurips.cc/paper_files/paper/2024/hash/09265e2568cf7a6ff47b506acbc2c6eb-Abstract-Conference.html>)
- **Evaluating Interventional Reasoning Capabilities of Large Language Models** [[Paper]](<https://openreview.net/forum?id=n4AvrD8kl5>)
- **LLMs Are Prone to Fallacies in Causal Inference** [[Paper]](<https://aclanthology.org/2024.emnlp-main.590/>)
- **CLEAR: Can Language Models Really Understand Causal Graphs?** [[Paper]](<https://aclanthology.org/2024.findings-emnlp.363/>)
- **Unveiling Causal Reasoning in Large Language Models: Reality or Mirage?** [[Paper]](<https://proceedings.neurips.cc/paper_files/paper/2024/hash/af2bb2b2280d36f8842e440b4e275152-Abstract-Conference.html>)
- **Does Reasoning Emerge? Examining the Probabilities of Causation in Large Language Models** [[Paper]](<https://proceedings.neurips.cc/paper_files/paper/2024/hash/d5a1f97d2b922da92e880d13b7d2bf02-Abstract-Conference.html>)
- **CausalGraph2LLM: Evaluating LLMs for Causal Queries** [[Paper]](<https://aclanthology.org/2025.findings-naacl.110/>)
- **From Causal Parrots to Causal Prophets? Towards Sound Causal Reasoning with Large Language Models** [[Paper]](<https://aclanthology.org/2025.nlp4dh-1.29/>)
- **On the Reliability of Large Language Models for Causal Discovery** [[Paper]](<https://aclanthology.org/2025.acl-long.471/>)
- **Eliciting and Improving the Causal Reasoning Abilities of Large Language Models with Conditional Statements** [[Paper]](<https://aclanthology.org/2025.cl-2.3/>)
- **ExpliCa: Evaluating Explicit Causal Reasoning in Large Language Models** [[Paper]](<https://aclanthology.org/2025.findings-acl.891/>)
- **Failure Modes of LLMs for Causal Reasoning on Narratives** [[Paper]](<https://icml.cc/virtual/2025/47391>)
- **Automated classification of causal relations. Evaluating different LLM performances.** [[Paper]](<https://aclanthology.org/2025.ranlp-stud.4/>)
- **Causal Understanding by LLMs: The Role of Uncertainty** [[Paper]](<https://aclanthology.org/2025.uncertainlp-main.19/>)
- **Counterfactual reasoning: an analysis of in-context emergence** [[Paper]](<https://neurips.cc/virtual/2025/loc/san-diego/poster/116021>)
- **Structure-Aware Causal Reasoning: A Neurosymbolic Framework for Counterfactual Inference in Large Language Models** [[Paper]](<https://papers.ssrn.com/sol3/papers.cfm?abstract_id=6110187>)
- **On the Eligibility of LLMs for Counterfactual Reasoning: A Decompositional Study** [[Paper]](<https://openreview.net/forum?id=qVFbnfVmuu>)
- **Do LLMs Share Human-Like Biases? Causal Reasoning Under Prior Knowledge, Irrelevant Context, and Varying Compute Budgets** [[Paper]](<https://openreview.net/forum?id=qlO26A1OpU>)
- **CausalFlip: A Benchmark for LLM Causal Judgment Beyond Semantic Matching** [[Paper]](<https://arxiv.org/abs/2602.20094>)
- **CausalReasoningBenchmark: A Real-World Benchmark for Disentangled Evaluation of Causal Identification and Estimation** [[Paper]](<https://openreview.net/forum?id=xqpDucFOZT>)
- **CounterBench: Evaluating and Improving Counterfactual Reasoning in Large Language Models** [[Paper]](<https://arxiv.org/abs/2502.11008>)
- **Can Large Language Models Infer Causal Relationships from Real-World Text?** [[Paper]](<https://arxiv.org/abs/2505.18931>)
- **A Causal Framework to Quantify the Robustness of Mathematical Reasoning with Language Models** [[Paper]](<https://aclanthology.org/2023.acl-long.32/>)
- **CofCA: A STEP-WISE Counterfactual Multi-hop QA benchmark** [[Paper]](<https://proceedings.iclr.cc/paper_files/paper/2025/hash/2628d4d3b054c2d7ad33ab03435204f4-Abstract-Conference.html>)
- **LLMs Struggle to Perform Counterfactual Reasoning with Parametric Knowledge** [[Paper]](<https://openreview.net/forum?id=EU9qCcKMv1>)
- **Can LLMs Leverage Observational Data? Towards Data-Driven Causal Discovery with LLMs** [[Paper]](<https://arxiv.org/abs/2504.10936v1>)
- **Causal Reasoning in Pieces: Modular In-Context Learning for Causal Discovery** [[Paper]](<https://arxiv.org/abs/2507.23488v1>)
- **Compositional Causal Reasoning Evaluation in Language Models** [[Paper]](<https://openreview.net/forum?id=OJ3dQNRnsx>)
- **Flying Pigs, FaR and Beyond: Evaluating LLM Reasoning in Counterfactual Worlds** [[Paper]](<https://arxiv.org/abs/2505.22318v2>)
- **HCR-Reasoner: Synergizing Large Language Models and Theory for Human-like Causal Reasoning** [[Paper]](<https://neurips.cc/virtual/2025/loc/mexico-city/129961>)
- **Ice Cream Doesn't Cause Drowning: Benchmarking LLMs Against Statistical Pitfalls in Causal Inference** [[Paper]](<https://arxiv.org/abs/2505.13770v3>)
- **CommonWhy: A Dataset for Evaluating Entity-Based Causal Commonsense Reasoning in Large Language Models** [[Paper]](<https://arxiv.org/abs/2605.12918v1>)
- **From Causal Plausibility to Causal Reliability: Evaluating LLMs as Calibrated Direct Causal-Edge Classifiers** [[Paper]](<https://arxiv.org/abs/2608.23660v1>)
- **METER: Evaluating Multi-Level Contextual Causal Reasoning in Large Language Models** [[Paper]](<https://aclanthology.org/2026.acl-long.1668/>)
- **NoisyCausal: A Benchmark for Evaluating Causal Reasoning Under Structured Noise** [[Paper]](<https://openreview.net/forum?id=PO4enmM9wT#discussion>)
- **How Likely Do LLMs with CoT Mimic Human Reasoning?** [[Paper]](<https://aclanthology.org/2025.coling-main.524/>)
- **FACT-E: Causality-Inspired Evaluation for Trustworthy Chain-of-Thought Reasoning** [[Paper]](<https://aclanthology.org/2026.findings-acl.1014/>)
- **On Emergent Social World Models — Evidence for Functional Integration of Theory of Mind and Pragmatic Reasoning in Language Models** [[Paper]](<https://aclanthology.org/2026.acl-long.1735/>)
- **CausalityCheck: A Framework for Evaluating Causal Reasoning in Large Language Models** [[Paper]](<https://aclanthology.org/2026.findings-acl.808/>)
- **LLMs with Chain-of-Thought Are Non-Causal Reasoners** [[Paper]](<https://arxiv.org/pdf/2402.16048v1>)
- **Causal Abstraction for Chain-of-Thought Reasoning in Arithmetic Word Problems** [[Paper]](<https://aclanthology.org/2023.blackboxnlp-1.12.pdf>)
- **KisMATH: DoLLMsHaveKnowledge of Implicit Structures in Mathematical Reasoning?** [[Paper]](<https://aclanthology.org/2026.tacl-1.59.pdf>)

#### 5.2.3 Planning and Decision Making

*No papers listed yet.*

### 5.3 Trustworthiness Evaluation

#### 5.3.1 Fairness

- **BiasCause: Evaluate Socially Biased Causal Reasoning of Large Language Models** [[Paper]](<https://arxiv.org/abs/2504.07997v2>)
- **Do Large Language Models Show Biases in Causal Learning? Insights from Contingency Judgment** [[Paper]](<https://arxiv.org/abs/2510.13985v1>)
- **Exploring Causal Effect of Social Bias on Faithfulness Hallucinations in Large Language Models** [[Paper]](<https://dl.acm.org/doi/10.1145/3746252.3761298>)
- **Causally Testing Gender Bias in LLMs: A Case Study on Occupational Bias** [[Paper]](<https://aclanthology.org/2025.findings-naacl.281/>)
- **Counterfactual Fairness Evaluation of LLM-Based Contact Center Agent Quality Assurance System** [[Paper]](<https://aclanthology.org/2026.findings-acl.1890/>)
- **SCOPE: A Dataset of Stereotyped Prompts for Counterfactual Fairness Assessment of LLMs** [[Paper]](<https://arxiv.org/abs/2604.05555v1>)

#### 5.3.2 Faithfulness

- **Can LLMs Explain Themselves Counterfactually?** [[Paper]](<https://aclanthology.org/2025.emnlp-main.396/>)
- **A Causal Lens for Evaluating Faithfulness Metrics** [[Paper]](<https://aclanthology.org/2025.emnlp-main.1496/>)
- **LIBERTy: A Causal Framework for Benchmarking Concept-Based Explanations of LLMs with Structural Counterfactuals** [[Paper]](<https://aclanthology.org/2026.findings-acl.399/>)
- **Uncovering Hidden Correctness in LLM Causal Reasoning via Symbolic Verification** [[Paper]](<https://aclanthology.org/2026.eacl-long.56/>)
- **C2-Faith: Benchmarking LLM Judges for Causal and Coverage Faithfulness in Chain-of-Thought Reasoning** [[Paper]](<https://aclanthology.org/2026.gem-main.62/>)
- **The Table Says Otherwise: Testing LLMs with Counterfactual Relational Data** [[Paper]](<https://arxiv.org/abs/2606.23667v2>)
- **RFEval: Benchmarking Reasoning Faithfulness under Counterfactual Reasoning Intervention in Large Reasoning Models** [[Paper]](<https://openreview.net/forum?id=2Gc8aj0afg>)
- **Do LLMs Make More Mistakes If They Do Not Believe the Input Data?** [[Paper]](<https://arxiv.org/abs/2609.09363>)
- **Towards Faithful Natural Language Explanations: A Study Using Activation Patching in Large Language Models** [[Paper]](<https://aclanthology.org/2025.emnlp-main.529/>)
- **The Probabilities Also Matter: A More Faithful Metric for Faithfulness of Free-Text Explanations in Large Language Models** [[Paper]](<https://aclanthology.org/2024.acl-short.49/>)
- **On Measuring Faithfulness or Self-consistency of Natural Language Explanations** [[Paper]](<https://aclanthology.org/2024.acl-long.329/>)

#### 5.3.3 Interpretability

- **Do LLM Self-Explanations Help Users Predict Model Behavior? Evaluating Counterfactual Simulatability with Pragmatic Perturbations** [[Paper]](<https://arxiv.org/abs/2601.03775>)
- **CausalGym: Benchmarking causal interpretability methods on linguistic tasks** [[Paper]](<https://aclanthology.org/2024.acl-long.785/>)
- **RAVEL: Evaluating Interpretability Methods on Disentangling Language Model Representations** [[Paper]](<https://aclanthology.org/2024.acl-long.470/>)
- **MIB: A Mechanistic Interpretability Benchmark** [[Paper]](<https://proceedings.mlr.press/v267/mueller25a.html>)
- **How does Chain of Thought Think? Mechanistic Interpretability of Chain-of-Thought Reasoning with Sparse Autoencoding** [[Paper]](<https://arxiv.org/abs/2507.22928>)

#### 5.3.4 Robustness

- **How Robust are Large Language Models Against Word-Level Spurious Correlations? A Causal Discovery Approach** [[Paper]](<https://link.springer.com/article/10.1007/s10994-026-07011-3>)
- **RECALL: A Benchmark for LLMs Robustness against External Counterfactual Knowledge** [[Paper]](<https://arxiv.org/abs/2311.08147>)
- **Faithfulness vs. Safety: Evaluating LLM Behavior Under Counterfactual Medical Evidence** [[Paper]](<https://arxiv.org/abs/2601.11886v2>)
- **MamaBench: Benchmarking LLM Robustness in Maternal and Child Health Diagnosis through Counterfactual Clinical Perturbation** [[Paper]](<https://arxiv.org/abs/2607.14385v2>)
- **MedEinst: Benchmarking the Einstellung Effect in Medical LLMs through Counterfactual Differential Diagnosis** [[Paper]](<https://arxiv.org/abs/2601.06636v1>)

#### 5.3.5 Unlearning

- **Intrinsic Test of Unlearning Using Parametric Knowledge Traces** [[Paper]](<https://aclanthology.org/2025.emnlp-main.985/>)
- **Measuring the Depth of LLM Unlearning via Activation Patching** [[Paper]](<http://arxiv.org/abs/2605.24614>)

#### 5.3.6 Security and Alignment

- **On the Hidden Costs of Counterfactual Knowledge Training in LLM Unlearning** [[Paper]](<https://arxiv.org/abs/2605.27083>)

### 5.4 Application Evaluation

#### 5.4.1 Traditional Causal Analysis

*No papers listed yet.*

#### 5.4.2 Data Analysis

- **Deriving Strategic Market Insights with Large Language Models: A Benchmark for Forward Counterfactual Generation** [[Paper]](<https://aclanthology.org/2025.emnlp-main.575/>)
- **Can LLMs Simulate Personas with Reversed Performance? A Systematic Investigation for Counterfactual Instruction Following in Math Reasoning Context** [[Paper]](<https://openreview.net/forum?id=kPv29Z83gU>)
- **Enhancing Causal Relationship Detection Using Prompt Engineering and Large Language Models** [[Paper]](<https://aclanthology.org/2025.finnlp-1.26/>)

#### 5.4.3 Scientific Discovery

- **Hypothesizing Missing Causal Variables with LLMs** [[Paper]](<https://openreview.net/forum?id=lXVVpoW2CJ>)
- **CauSciBench: Assessing LLM Causal Reasoning for Scientific Research** [[Paper]](<https://openreview.net/forum?id=EO8mTLqDuT>)
- **CausalGame: Benchmarking Causal Thinking of LLM Agents in Games** [[Paper]](<https://openreview.net/forum?id=SEFSkn4l6d>)
- **CausalDS: Benchmarking Causal Reasoning in Data-Science Agents** [[Paper]](<https://arxiv.org/abs/2607.08093v1>)

#### 5.4.4 Software Engineering

- **OpenRCA: Can Large Language Models Locate the Root Cause of Software Failures?** [[Paper]](<https://openreview.net/forum?id=M4qNIzQYpd>)
- **OpenRCA 2.0: From Outcome Labels to Causal Process Supervision** [[Paper]](<https://arxiv.org/abs/2606.27154>)

## Additional Papers

Papers retained from the bibliography that do not yet have a complete taxonomy assignment.

- **Consistency evaluation of benchmarks used for causal discovery** [[Paper]](<https://arxiv.org/abs/2606.01789v1>)
- **Repair or Resample? Rethinking Failure Debugging in LLM Multi-Agent Systems** *(paper link unavailable)*
- **Learning a Structural Causal Model for Intuition Reasoning in Conversation** [[Paper]](<https://arxiv.org/abs/2305.17727>)
- **Causal-structure Driven Augmentations for Text OOD Generalization** [[Paper]](<https://openreview.net/pdf?id=XmTRYK1uN2>)
- **Image Content Generation with Causal Reasoning** [[Paper]](<https://arxiv.org/abs/2312.07132>)
- **Causal Interpretation of Self-Attention in Pre-Trained Transformers** [[Paper]](<https://arxiv.org/abs/2310.20307>)
- **Interpretability at Scale: Identifying Causal Mechanisms in Alpaca** [[Paper]](<https://arxiv.org/abs/2305.08809>)

## Contributing

Contributions are welcome. Please open an issue or pull request with:

- the paper title and public URL;
- the most appropriate taxonomy section; and
- a short note if the paper belongs in more than one section.

Please keep entries alphabetically or chronologically consistent with their surrounding section and avoid duplicate links within the same category.
