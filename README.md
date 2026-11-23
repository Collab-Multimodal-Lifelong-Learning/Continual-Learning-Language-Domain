# Continual Learning in the Language Domain

**Research on continual learning methods and benchmarks for language-based tasks.**

This repository is part of the [Collab-Multimodal-Lifelong-Learning](https://github.com/Collab-Multimodal-Lifelong-Learning) project, **Developing a Sustainable Collaborative Multi-modal Lifelong Learning Framework**. It brings together research on how large language models (LLMs) acquire, retain, update, and reason over knowledge as information and learning conditions evolve.

## Research list

### Prompting and instruction learning

- **Fixed Input Parameterization for Efficient Prompting** (Findings of ACL 2023) — Eunbi Choi et al.
  - Encodes fixed prompts in model parameters so they need not be appended to every input.
  - [Paper](https://aclanthology.org/2023.findings-acl.533/) · [Project code](https://github.com/Collab-Multimodal-Lifelong-Learning/Fixed-Input-Parameterization/blob/bb46c78fcf52f7922e9fe9a9783d3341d6ab632d/README.md) · [Fork](https://github.com/Collab-Multimodal-Lifelong-Learning/Fixed-Input-Parameterization) · [Upstream](https://github.com/unbiarirang/Fixed-Input-Parameterization)

- **Gradient Ascent Post-training Enhances Language Model Generalization (GAP)** (ACL 2023) — Dongkeun Yoon et al.
  - Gradient-ascent post-training for language-model generalization.
  - [Paper](https://arxiv.org/abs/2306.07052) · [Project code](https://github.com/Collab-Multimodal-Lifelong-Learning/GAP/blob/4f0b3890536cbac5f708a1eddb4abf9cdc3c4159/README.md) · [Fork](https://github.com/Collab-Multimodal-Lifelong-Learning/GAP) · [Upstream](https://github.com/kaistAI/GAP)

- **Guess the Instruction! Flipped Learning Makes Language Models Stronger Zero-Shot Learners** (ICLR 2023) — Seonghyeon Ye et al.
  - Learning to infer instructions for zero-shot generalization.
  - [Paper](https://arxiv.org/abs/2210.02969) · [Project code](https://github.com/Collab-Multimodal-Lifelong-Learning/Flipped-Learning/blob/ad7d6ea590bc087b01a82bfc9ed02d97fccca977/README.md) · [Fork](https://github.com/Collab-Multimodal-Lifelong-Learning/Flipped-Learning) · [Upstream](https://github.com/seonghyeonye/Flipped-Learning)

- **Exploring the Benefits of Training Expert Language Models over Instruction Tuning** (ICML 2023) — Joel Jang et al.
  - Training and evaluation of expert language models.
  - [Paper](https://arxiv.org/abs/2302.03202) · [Project code](https://github.com/Collab-Multimodal-Lifelong-Learning/ELM/blob/7edc2660049f16c13a1bf67471c663bcbe6c504f/README.md) · [Fork](https://github.com/Collab-Multimodal-Lifelong-Learning/ELM) · [Upstream](https://github.com/joeljang/ELM)

- **Investigating the Effectiveness of Task-Agnostic Prefix Prompt for Instruction Following (TAPP)** — Seonghyeon Ye et al.
  - Studies whether prepending the same prefix across tasks improves zero-shot instruction following.
  - [Paper](https://arxiv.org/abs/2302.14691) · [Project code](https://github.com/Collab-Multimodal-Lifelong-Learning/TAPP/blob/fa9b19cd1dca32d924e43e0257018cc03ad0a80e/README.md) · [Fork](https://github.com/Collab-Multimodal-Lifelong-Learning/TAPP) · [Upstream](https://github.com/seonghyeonye/TAPP)

### Knowledge, grounding, and reasoning

- **Knowledge Unlearning for Mitigating Privacy Risks in Language Models** — Joel Jang et al.
  - Language-model knowledge unlearning for privacy.
  - [Paper](https://arxiv.org/abs/2210.01504) · [Project code](https://github.com/Collab-Multimodal-Lifelong-Learning/knowledge-unlearning/blob/53b118ea2f91029e79ab7832b8626f8c1cc617d0/README.md) · [Fork](https://github.com/Collab-Multimodal-Lifelong-Learning/knowledge-unlearning) · [Upstream](https://github.com/joeljang/knowledge-unlearning)

- **How Well Do LLMs Truly Ground?** — Hyunji Lee et al.
  - Evaluation of grounding in large language models.
  - [Paper](https://arxiv.org/abs/2311.09069) · [Project code](https://github.com/Collab-Multimodal-Lifelong-Learning/How-Well-Do-LLMs-Truly-Ground/blob/52115d43d0b7194ae255cb1381e426a919c96b5d/README.md) · [Fork](https://github.com/Collab-Multimodal-Lifelong-Learning/How-Well-Do-LLMs-Truly-Ground) · [Upstream](https://github.com/kaistAI/How-Well-Do-LLMs-Truly-Ground)

- **LangBridge: Multilingual Reasoning Without Multilingual Supervision** (ACL 2024) — Dongkeun Yoon et al.
  - Multilingual reasoning without multilingual supervision.
  - [Paper](https://aclanthology.org/2024.acl-long.405/) · [Project code](https://github.com/Collab-Multimodal-Lifelong-Learning/LangBridge/blob/373e789603e2b8cb11967126c3b194c1f735727b/README.md) · [Fork](https://github.com/Collab-Multimodal-Lifelong-Learning/LangBridge) · [Upstream](https://github.com/kaistAI/LangBridge)

- **Reasoning Models Better Express Their Confidence** (NeurIPS 2025) — Dongkeun Yoon et al.
  - Studies how extended reasoning and deliberative behaviors can improve confidence calibration and allow confidence to be refined over a reasoning trace.
  - [Paper](https://proceedings.neurips.cc/paper_files/paper/2025/hash/95ee7181fe256439dca74ec794b33bb6-Abstract-Conference.html) · [Project code](https://github.com/Collab-Multimodal-Lifelong-Learning/reasoning-models-confidence/blob/255e1777f46d37069392efb643f669e329fd223a/README.md) · [Fork](https://github.com/Collab-Multimodal-Lifelong-Learning/reasoning-models-confidence) · [Upstream](https://github.com/MattYoon/reasoning-models-confidence)

- **Can Large Language Models Keep Up? Benchmarking Online Adaptation to Continual Knowledge Streams (OAKS)** (ACL 2026) — Jiyeon Kim et al.
  - Introduces **OAKS**, a benchmark for tracking facts that evolve across a stream of context chunks, and examines limitations in current online adaptation methods.
  - [Paper](https://aclanthology.org/2026.acl-long.1956/) · [Project code](https://github.com/Collab-Multimodal-Lifelong-Learning/OAKS/blob/679445b674c075345787a6ee7fb1bfaba9b78632/README.md) · [Fork](https://github.com/Collab-Multimodal-Lifelong-Learning/OAKS) · [Upstream](https://github.com/kaistAI/OAKS)

### State-space language models

- **Mitigating Over-Smoothing in Mamba2 via Spectral Domain Analysis** — Seojin Kim, Yehjin Shin, and Noseong Park
  - High-frequency enhancement to reduce over-smoothing in Mamba2.
  - [Paper](https://openreview.net/forum?id=r08kqzrito) · [Project code](https://github.com/Collab-Multimodal-Lifelong-Learning/mamba2-high-freq-enhance/blob/b44332b9ce3c0a661bd36438e225a993161dae21/README.md) · [Fork](https://github.com/Collab-Multimodal-Lifelong-Learning/mamba2-high-freq-enhance) · [Upstream](https://github.com/sjiinkim/mamba2-high-freq-enhance)

- **Graph Signal Processing Meets Mamba2: Adaptive Filter Bank via Delta Modulation** (ICLR 2026) — Yehjin Shin, Seojin Kim, and Noseong Park
  - Adaptive graph filter banks for Mamba2 sequence modeling.
  - [Paper](https://openreview.net/forum?id=w0XhHcXfKv) · [Project code](https://github.com/Collab-Multimodal-Lifelong-Learning/HADES/blob/545d23bcb2d2c90f0e51800c9447fd662579031b/README.md) · [Fork](https://github.com/Collab-Multimodal-Lifelong-Learning/HADES) · [Upstream](https://github.com/yehjin-shin/HADES)

### Additional project research

The following publications are highlighted in the project's July 15, 2026 progress evaluation.

#### Knowledge Acquisition and Continual Adaptation

- **[Knowledge Entropy Decay during Language Model Pretraining Hinders New Knowledge Acquisition](https://proceedings.iclr.cc/paper_files/paper/2025/hash/f8f3250f3f31387906e49aec41602f36-Abstract-Conference.html)** — *ICLR 2025 (Oral)*.
  - Investigates how declining diversity in the use of internal knowledge sources is associated with weaker acquisition and retention of new knowledge.

#### Reasoning Analysis and Confidence

- **[The CoT Encyclopedia: Analyzing, Predicting, and Controlling how a Reasoning Model will Think](https://proceedings.iclr.cc/paper_files/paper/2026/hash/e560202b6e779a82478edb46c6f8f4dd-Abstract-Conference.html)** — *ICLR 2026*.
  - Introduces a bottom-up framework for extracting, clustering, interpreting, and steering reasoning strategies from model-generated chains of thought.

#### Structured Reasoning

- **[TSLM: Tree-Structured Language Modeling for Divergent Thinking](https://arxiv.org/abs/2601.22688)** — *ICLR 2026*.
  - Explores tree-structured language generation that branches and expands multiple reasoning paths within a single process.

## Research Overview

Language models deployed in changing environments must accommodate new facts, revise outdated knowledge, and maintain useful previously learned information. Continual language learning studies the balance between **knowledge acquisition**, **knowledge retention**, and **adaptation to evolving information**. It also investigates how models assess and refine their own reasoning as they process new evidence.

The principal research directions are:

1. **Continual Knowledge Acquisition and Retention:** Understanding why learning new knowledge becomes harder during language-model pretraining and how to mitigate forgetting.
2. **Online Knowledge Adaptation and Evaluation:** Measuring a model's ability to follow continuously changing facts and update its knowledge efficiently.
3. **Reasoning Behavior and Confidence:** Analyzing reasoning strategies and the evolution of confidence during inference.
4. **Structured Reasoning and Exploration:** Learning to explore multiple reasoning paths systematically rather than relying solely on a linear chain of thought.

## Research Directions

### 1. Continual Knowledge Acquisition and Retention

**Research focus:** Knowledge acquisition, forgetting, and the evolution of internal memory usage during language-model pretraining.

- Analyze how the diversity of parametric knowledge sources used by a language model changes as pretraining progresses.
- Study **knowledge entropy decay** and its association with reduced ability to acquire and retain knowledge.
- Investigate approaches that encourage the use of underutilized knowledge sources to improve subsequent learning.
- Support continual updates while reducing interference with previously acquired knowledge.

**Research team:** Prof. Minjoon Seo, KAIST.

### 2. Online Knowledge Adaptation and Evaluation

**Research focus:** Adapting to emerging or changing facts in a stream of textual information.

- Evaluate the ability to distinguish **newly acquired**, **updated**, and **forgotten** knowledge.
- Investigate parameter-efficient adaptation, including LoRA-based approaches, for learning from new corpora while limiting forgetting.
- Study **online adaptation to continual knowledge streams**, including facts that change repeatedly over time.
- Build benchmarks that measure whether models accurately track changing information rather than relying on outdated states.

**Evaluation resources:** EvolvingQA (NAACL 2024) is used in the project's continual-knowledge-learning evaluation; OAKS (ACL 2026) is a distinct benchmark for online adaptation to continually changing contextual facts.

**Research team:** Prof. Minjoon Seo, KAIST.

### 3. Reasoning Behavior and Confidence

**Research focus:** Understanding and measuring how reasoning models express and revise their confidence.

- Analyze how confidence changes during extended **chain-of-thought (CoT)** reasoning.
- Examine the contribution of deliberative behaviors, including verification, exploration of alternatives, and backtracking.
- Study confidence calibration as a component of reliable language-model reasoning.
- Identify and organize recurring reasoning strategies through bottom-up analysis of model-generated reasoning traces.

**Research team:** Prof. Minjoon Seo, KAIST.

### 4. Structured Reasoning and Exploration

**Research focus:** Moving beyond purely sequential reasoning toward structured, branching exploration.

- Represent multiple candidate reasoning paths within a **tree-structured generation** process.
- Train models on branching reasoning traces, including both successful and unsuccessful paths.
- Study more systematic exploration while avoiding redundant computation on shared reasoning prefixes.
- Connect reasoning-process analysis with methods for predicting and guiding model behavior.

**Research team:** Prof. Minjoon Seo, KAIST.

## Evaluation Highlights

The following figures are **project-reported results** from the **July 15, 2026** progress evaluation. They are not independently reproduced results from the code in this repository.

### Continual Knowledge Learning

The project evaluates continual updating of LLM knowledge using **FUAR** (*Forgotten / (Updated + Acquired)*). A **lower** FUAR indicates less forgetting relative to successfully updated and newly acquired knowledge.

| Evaluation item | Reported value |
| --- | ---: |
| Pre-project reference FUAR | 0.50 |
| Project target FUAR | **< 0.30** |
| Reported 2024 result | 0.20 |
| Reported 2025 result | 0.15 |
| Reported 2026 result | **0.13** |

**Evaluation context:** The project materials identify **EvolvingQA** as a benchmark for continual knowledge learning and describe approaches based on LoRA and related methods. The FUAR figures above refer to the project's continual-knowledge-learning assessment; they should **not** be interpreted as scores on OAKS.

### Related Benchmarks

| Benchmark | What it evaluates | Resource |
| --- | --- | --- |
| **EvolvingQA** | Acquisition and updating of temporally evolving world knowledge | [NAACL 2024 paper](https://aclanthology.org/2024.naacl-long.302/) |
| **OAKS** | Online adaptation to continuously changing facts in streamed context | [ACL 2026 paper](https://aclanthology.org/2026.acl-long.1956/) |

## Code and Resources

Each Project code link opens the README at the pinned commit in the organization fork. The corresponding submodule uses the same revision. Open the upstream repository for the original source.

Clone this repository and its project folders with:

```bash
git clone --recurse-submodules --shallow-submodules https://github.com/Collab-Multimodal-Lifelong-Learning/Continual-Learning-Language-Domain.git
```

In an existing checkout, run `git submodule update --init --recursive --depth 1`.

## Related Repositories

Other research areas within [Collab-Multimodal-Lifelong-Learning](https://github.com/Collab-Multimodal-Lifelong-Learning):

- [Continual-Learning-Vision-Domain](https://github.com/Collab-Multimodal-Lifelong-Learning/Continual-Learning-Vision-Domain) — Continual learning for vision-based tasks.
- [Continual-Learning-Time-Series-Domain](https://github.com/Collab-Multimodal-Lifelong-Learning/Continual-Learning-Time-Series-Domain) — Continual learning for time-series data.
- [Continual-Learning-and-Multimodal-Integration](https://github.com/Collab-Multimodal-Lifelong-Learning/Continual-Learning-and-Multimodal-Integration) — Continual learning methods and multimodal integration.
- [PDM-Framework](https://github.com/Collab-Multimodal-Lifelong-Learning/PDM-Framework) — Integrated framework for sustainable collaborative multimodal continual learning.

## Acknowledgment

This research is associated with the Korean national R&D project **“Developing a Sustainable Collaborative Multi-modal Lifelong Learning Framework” (Project No. 2022-0-00113)**, conducted within the *Human-Centered AI Core Technology Development* program, supported by the Ministry of Science and ICT (MSIT) and administered by the Institute of Information & Communications Technology Planning & Evaluation (IITP).
