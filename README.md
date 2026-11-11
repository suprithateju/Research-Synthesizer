# 📑 Academic Paper / Research Brief Synthesizer Skill

> An AI Agent Skill specification, local heuristic execution engine, and interactive dashboard that ingests unstructured research papers and deterministically synthesizes them into standardized 5-pillar markdown dossiers with formatted metric tables.

---

## 📌 Executive Summary

* **Objective:** Standard LLM summaries often omit exact numbers, dataset scales, or computational bottlenecks. This project builds a dedicated, schema-validated Agent Skill (`academic-research-synthesizer`) that deterministically extracts five critical research pillars without paid APIs or cloud dependencies.
* **Methodology:**
  * Created an offline-first single-page studio combining an agent skill specification package (`skill.json` OpenAPI schema, `prompt_system.md` persona rules, `rules.yaml` heuristic definitions) with a client-side execution engine.
  * Implemented a local regex and heuristic text segmenter to identify paper objectives, dataset counts, architectural mechanics, comparative evaluation metrics, and hardware/complexity limitations.
  * Embedded real-time RFC 7159 JSON schema validation, interactive Markdown dossier rendering, and vector print PDF export.
* **Expected Outcome:** A fast, 100% offline-ready application allowing researchers and students to paste any paper, view live pipeline extraction steps, inspect the underlying tool schema, and export publication-ready research briefs.

---

## 🚀 Key Features

### 1. ⚙️ Complete Agent Skill Specification Bundle
* **`skill.json`:** Standardized OpenAPI v3 / JSON-Schema Draft-07 specification defining function signatures, mandatory parameters, and nested object constraints.
* **`prompt_system.md`:** Rigid persona instructions that enforce factual extraction and suppress academic marketing fluff.
* **`rules.yaml`:** Heuristic regex patterns and marker keywords for deterministic section segmentation (abstracts, methodologies, datasets, benchmarks, limitations).

### 2. 🏛️ The 5-Pillar Scientific Extraction
1. **Core Objective & Problem Formulation:** Primary goal, baseline problem statement, and scientific hypothesis.
2. **Datasets & Evaluation Benchmarks:** Dataset titles, task domains, and training/testing scale metrics.
3. **Architecture & Methodological Novelty:** Core algorithmic mechanism, key innovations, and asymptotic time/space complexity.
4. **Empirical Evaluation Metrics Table:** Structured comparative tables detailing benchmark tasks, target metrics, baseline scores, achieved scores, and performance deltas.
5. **Stated Limitations & Computational Constraints:** Memory bounds, hardware bottlenecks, and scaling limits.

### 3. 🧪 Pre-Loaded Benchmark Corpus
* Ships with pre-loaded seminal papers for instant verification:
  * **Sample 1:** *Attention Is All You Need* (Vaswani et al., Transformer)
  * **Sample 2:** *Deep Residual Learning for Image Recognition* (He et al., ResNet)
* Custom text ingestion mode to paste and analyze any research paper.

### 4. 📊 Real-Time Validation & Export
* Real-time confidence gauges across all 5 scientific deliverables.
* Instant toggle between formatted Markdown dossier view and raw JSON schema output.
* One-click clipboard copy, `.md` file download, and vector A4 PDF print stylesheet.

---

## 🖥️ System Architecture & Workflow

<img width="892" height="389" alt="image" src="https://github.com/user-attachments/assets/ffb288c5-43bf-4637-805b-d559a2939a9a" />
<img width="872" height="336" alt="image" src="https://github.com/user-attachments/assets/2f837d72-6a81-4e41-8398-c9d6be1486e8" />

+-----------------------------------------------------------------------------------------+
| RAW RESEARCH PAPER (Abstract, Methods, Experiments, Baselines, Limitations)             |
+-----------------------------------------------------------------------------------------+
                                             │
                                             ▼
                      [ HEURISTIC SEGMENTATION ENGINE ]
                      - Regex metric parsers (BLEU, Error %, mAP)
                      - Section keyword boundaries
                                             │
                                             ▼
                      [ RFC 7159 SCHEMA VALIDATOR ]
                      - Validates against skill.json Draft-07
                      - Checks 5 mandatory pillar parameters
                                             │
                                             ▼
+-----------------------------------------------------------------------------------------+
| STANDARDIZED 5-PILLAR DOSSIER                                                          |
| 1. Objective & Hypothesis      4. Empirical Comparative Table                           |
| 2. Benchmark Scales            5. Stated Bottlenecks & Complexity Bounds                |
| 3. Architecture & Innovations                                                           |
+-----------------------------------------------------------------------------------------+
| Output Formats: Live HTML Dashboard  |  Raw JSON  |  Markdown (.md)  |  A4 Print PDF    |
+-----------------------------------------------------------------------------------------+
