# Generative Rakugo Workflow (GRW)

This workflow utilizes the `STOCK` knowledge base to programmatically design and generate Rakugo scripts.

## 🔄 Pipeline Stages

### Stage 1: Concept (SEED)
- **Input**: Theme (e.g., "Modern AI", "Ancient Japan") + Target Emotion (e.g., "Surprise", "Irony").
- **Action**: Select one or more `STRUC-xxx` (Structures) from `STOCK`.
- **Output**: `concept.yaml` (Theme, Target Structure, Key Mechanisms).

### Stage 2: Structural Mapping (STAGE)
- **Action**: Define the "Tension Curve" (Sync $\rightarrow$ Deviation $\rightarrow$ Recovery).
- **Output**: `map.yaml` (Timeline of `MECH-xxx` triggers).

### Stage 3: Generation (GEN)
- **Action**: LLM generates script based on `map.yaml`.
- **Gimmick**: Use a "Contrast-Driven Prompt" (Explicitly instructing the AI to build the `MECH-001` frame before triggering `MECH-002`).
- **Output**: `draft_script.txt`.

### Stage 4: Verification (STOCK)
- **Action**: Feed the `draft_script.txt` back into the `Inductive Agent`.
- **Metric**: "Theoretical Fidelity" (Does the output actually match the `STRUC`?).
- **Output**: `verified_script.md` $\rightarrow$ Archive in `STOCK/proofs/`.

---

## 🛠️ Tooling (Planned)
- `scripts/generate_rakugo.py`: Implements the Generation stage.
- `scripts/verify_gen.py`: Implements the Verification stage.
