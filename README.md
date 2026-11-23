# Continual Learning in the Language Domain

**Research on continual learning methods and benchmarks for language-based tasks.**

This repository is part of the [Collab-Multimodal-Lifelong-Learning](https://github.com/Collab-Multimodal-Lifelong-Learning) project, **Developing a Sustainable Collaborative Multi-modal Lifelong Learning Framework**. It brings together research on how large language models (LLMs) acquire, retain, update, and reason over knowledge as information and learning conditions evolve.

Browse the [12 research projects](#code-and-resources) for source code and documentation.

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

## Representative Research and Publications

The following publications are highlighted in the project's July 15, 2026 progress evaluation.

### Knowledge Acquisition and Continual Adaptation

- **[Knowledge Entropy Decay during Language Model Pretraining Hinders New Knowledge Acquisition](https://proceedings.iclr.cc/paper_files/paper/2025/hash/f8f3250f3f31387906e49aec41602f36-Abstract-Conference.html)** — *ICLR 2025 (Oral)*.
  - Investigates how declining diversity in the use of internal knowledge sources is associated with weaker acquisition and retention of new knowledge.

- **[Can Large Language Models Keep Up? Benchmarking Online Adaptation to Continual Knowledge Streams](https://aclanthology.org/2026.acl-long.1956/)** — *ACL 2026*.
  - Introduces **OAKS**, a benchmark for tracking facts that evolve across a stream of context chunks, and examines limitations in current online adaptation methods.
  - [OAKS code and benchmark](https://github.com/Collab-Multimodal-Lifelong-Learning/OAKS/blob/c1a76e66b5b2276973ee8ee3de7063721e22a88f/README.md)

### Reasoning Analysis and Confidence

- **[Reasoning Models Better Express Their Confidence](https://proceedings.neurips.cc/paper_files/paper/2025/hash/95ee7181fe256439dca74ec794b33bb6-Abstract-Conference.html)** — *NeurIPS 2025*.
  - Studies how extended reasoning and deliberative behaviors can improve confidence calibration and allow confidence to be refined over a reasoning trace.
  - [Project code and setup](https://github.com/Collab-Multimodal-Lifelong-Learning/reasoning-models-confidence/blob/1bb950d60b4556e1d02560fd55e5bd866354afec/README.md)

- **[The CoT Encyclopedia: Analyzing, Predicting, and Controlling how a Reasoning Model will Think](https://proceedings.iclr.cc/paper_files/paper/2026/hash/e560202b6e779a82478edb46c6f8f4dd-Abstract-Conference.html)** — *ICLR 2026*.
  - Introduces a bottom-up framework for extracting, clustering, interpreting, and steering reasoning strategies from model-generated chains of thought.

### Structured Reasoning

- **[TSLM: Tree-Structured Language Modeling for Divergent Thinking](https://arxiv.org/abs/2601.22688)** — *ICLR 2026*.
  - Explores tree-structured language generation that branches and expands multiple reasoning paths within a single process.

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

Each project is a Git submodule pinned to a commit in its organization fork. The table links to that revision's README and lists both the fork and its upstream repository.

Clone this repository and its project folders with:

```bash
git clone --recurse-submodules --shallow-submodules https://github.com/Collab-Multimodal-Lifelong-Learning/Continual-Learning-Language-Domain.git
```

In an existing checkout, run `git submodule update --init --recursive --depth 1`.

| Project README | Research focus | Repositories |
| --- | --- | --- |
| [Fixed-Input-Parameterization](https://github.com/Collab-Multimodal-Lifelong-Learning/Fixed-Input-Parameterization/blob/97639ee4c0f9d8034830346268e0401c475037d8/README.md) | Efficient prompting through fixed input parameterization. | [Fork](https://github.com/Collab-Multimodal-Lifelong-Learning/Fixed-Input-Parameterization) · [Upstream](https://github.com/unbiarirang/Fixed-Input-Parameterization) |
| [knowledge-unlearning](https://github.com/Collab-Multimodal-Lifelong-Learning/knowledge-unlearning/blob/732876dc19a782c4440c3565cf9821df0a4c7ca0/README.md) | Language-model knowledge unlearning for privacy. | [Fork](https://github.com/Collab-Multimodal-Lifelong-Learning/knowledge-unlearning) · [Upstream](https://github.com/joeljang/knowledge-unlearning) |
| [GAP](https://github.com/Collab-Multimodal-Lifelong-Learning/GAP/blob/fe89b0ad6c5c13f7f4e848ad3058a7df1fc3b5c6/README.md) | Gradient-ascent post-training for language-model generalization. | [Fork](https://github.com/Collab-Multimodal-Lifelong-Learning/GAP) · [Upstream](https://github.com/kaistAI/GAP) |
| [Flipped-Learning](https://github.com/Collab-Multimodal-Lifelong-Learning/Flipped-Learning/blob/9d2404eb87ed3d5099e09d1af2e89f2852da4afc/README.md) | Learning to infer instructions for zero-shot generalization. | [Fork](https://github.com/Collab-Multimodal-Lifelong-Learning/Flipped-Learning) · [Upstream](https://github.com/seonghyeonye/Flipped-Learning) |
| [How-Well-Do-LLMs-Truly-Ground](https://github.com/Collab-Multimodal-Lifelong-Learning/How-Well-Do-LLMs-Truly-Ground/blob/df3602b07e3e365f0903768a101306bacc1f8fd6/README.md) | Evaluation of grounding in large language models. | [Fork](https://github.com/Collab-Multimodal-Lifelong-Learning/How-Well-Do-LLMs-Truly-Ground) · [Upstream](https://github.com/kaistAI/How-Well-Do-LLMs-Truly-Ground) |
| [ELM](https://github.com/Collab-Multimodal-Lifelong-Learning/ELM/blob/27fc2a326cd8846717a022db1cbd94d393420bce/README.md) | Training and evaluation of expert language models. | [Fork](https://github.com/Collab-Multimodal-Lifelong-Learning/ELM) · [Upstream](https://github.com/joeljang/ELM) |
| [TAPP](https://github.com/Collab-Multimodal-Lifelong-Learning/TAPP/blob/f1e7c0bb894f192f71b9554e8a8ff3b0be01cc3a/README.md) | Task-agnostic prefix prompts for instruction following. | [Fork](https://github.com/Collab-Multimodal-Lifelong-Learning/TAPP) · [Upstream](https://github.com/seonghyeonye/TAPP) |
| [LangBridge](https://github.com/Collab-Multimodal-Lifelong-Learning/LangBridge/blob/4f43fb27cbed0b7d879f709831cc89738fac1039/README.md) | Multilingual reasoning without multilingual supervision. | [Fork](https://github.com/Collab-Multimodal-Lifelong-Learning/LangBridge) · [Upstream](https://github.com/kaistAI/LangBridge) |
| [reasoning-models-confidence](https://github.com/Collab-Multimodal-Lifelong-Learning/reasoning-models-confidence/blob/1bb950d60b4556e1d02560fd55e5bd866354afec/README.md) | Measurement and calibration of confidence in reasoning models. | [Fork](https://github.com/Collab-Multimodal-Lifelong-Learning/reasoning-models-confidence) · [Upstream](https://github.com/MattYoon/reasoning-models-confidence) |
| [mamba2-high-freq-enhance](https://github.com/Collab-Multimodal-Lifelong-Learning/mamba2-high-freq-enhance/blob/2932bf9d5460e2339af10607d1184c24f7ff78d8/README.md) | High-frequency enhancement to reduce over-smoothing in Mamba2. | [Fork](https://github.com/Collab-Multimodal-Lifelong-Learning/mamba2-high-freq-enhance) · [Upstream](https://github.com/sjiinkim/mamba2-high-freq-enhance) |
| [HADES](https://github.com/Collab-Multimodal-Lifelong-Learning/HADES/blob/56816a942f16809dbcfd4662c06d25e24d74b561/README.md) | Adaptive graph filter banks for Mamba2 sequence modeling. | [Fork](https://github.com/Collab-Multimodal-Lifelong-Learning/HADES) · [Upstream](https://github.com/yehjin-shin/HADES) |
| [OAKS](https://github.com/Collab-Multimodal-Lifelong-Learning/OAKS/blob/c1a76e66b5b2276973ee8ee3de7063721e22a88f/README.md) | Benchmark and code for online adaptation to changing facts in a knowledge stream. | [Fork](https://github.com/Collab-Multimodal-Lifelong-Learning/OAKS) · [Upstream](https://github.com/kaistAI/OAKS) |

## Related Repositories

Other research areas within [Collab-Multimodal-Lifelong-Learning](https://github.com/Collab-Multimodal-Lifelong-Learning):

- [Continual-Learning-Vision-Domain](https://github.com/Collab-Multimodal-Lifelong-Learning/Continual-Learning-Vision-Domain) — Continual learning for vision-based tasks.
- [Continual-Learning-Time-Series-Domain](https://github.com/Collab-Multimodal-Lifelong-Learning/Continual-Learning-Time-Series-Domain) — Continual learning for time-series data.
- [Continual-Learning-and-Multimodal-Integration](https://github.com/Collab-Multimodal-Lifelong-Learning/Continual-Learning-and-Multimodal-Integration) — Continual learning methods and multimodal integration.
- [PDM-Framework](https://github.com/Collab-Multimodal-Lifelong-Learning/PDM-Framework) — Integrated framework for sustainable collaborative multimodal continual learning.

## Acknowledgment

This research is associated with the Korean national R&D project **“Developing a Sustainable Collaborative Multi-modal Lifelong Learning Framework” (Project No. 2022-0-00113)**, within the *Human-Centered AI Core Technology Development* program, supported by the Ministry of Science and ICT (MSIT) and administered by the Institute of Information & Communications Technology Planning & Evaluation (IITP).
