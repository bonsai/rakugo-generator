# Rakugo Generator

This repository is the **Implementation Engine** that transforms academic Rakugo structures into actual scripts.

## 🎯 Purpose
While `research-rakugo` focuses on the **discovery** of patterns (Inductive), `rakugo-generator` focuses on the **application** of those patterns to generate new content (Deductive).

## 🔄 Relationship with `research-rakugo`
This project depends on the `STOCK` defined in the research repository.

**The Pipeline:**
`research-rakugo (STOCK)` $\xrightarrow{\text{Import}}$ `rakugo-generator (Seeds)` $\xrightarrow{\text{Generate}}$ `Outputs (Scripts)`

## 🏗️ Workflow: Concept $\rightarrow$ Script
1. **Concept (seeds/)**: Define a theme and select a target structure (e.g., `STRUC-001`) from the research STOCK.
2. **Generation (gen-pipelines/)**: Apply the a-priori structural laout to a generative LLM prompt.
3. **Verification**: The generated script is cross-referenced with the original theory to ensure structural fidelity.

## 📂 Directory Structure
- `seeds/`: Concept YAMLs specifying the target theme and structural components.
- `gen-pipelines/`: Workflow definitions and prompt engineering logic.
- `outputs/`: The generated Rakugo scripts.
