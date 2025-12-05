# <p align="center">🗣️ **FedSpeak** — Policy Signals → Structured Intelligence</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.13.3B-blue" />
  <img src="https://img.shields.io/badge/PMI--CPMAI-Governed_Workflow-DAA520" />
  <img src="https://img.shields.io/badge/NLP-Policy_Sensitive-4B0082" />
  <img src="https://img.shields.io/badge/Topic_Modeling-LDA_%7C_RBL-6A5ACD" />
  <img src="https://img.shields.io/badge/DataLineage-R2_Compliant-556B2F" />
  <img src="https://img.shields.io/badge/License-CC_BY_4.0-2F4F4F" />
</p>

---

## 📘 **Overview**

**FedSpeak** is a governed, CPMAI-aligned *Policy Language Intelligence Engine* that transforms  
**Federal Reserve communication**—Beige Book, FOMC Statements, Minutes—into structured signals suitable for:

- **Macro fusion systems** (e.g., the_Spine)  
- **Research workflows** across Cambridge, Oxford, MIT, Cornell, Imperial, NUS, UCL  
- **RegTech, FinTech, and supervisory analytics**  
- **Policy-drift and uncertainty diagnostics**  
- **Scenario-aware macro narrative engines**

FedSpeak canonically processes Federal Reserve text and outputs:

- **Policy-risk features:** `inflation_pressure`, `growth_concern`, `policy_uncertainty`, `policy_bias`  
- **Stability diagnostics:** rolling uncertainty, coherence drift  
- **Regime probabilities:** Disinflation Recovery, Soft-Landing Drift, Stagflation Variant, Illusory Wealth Regime  

It produces explainable, reproducible, research-grade features backed by strict metadata, schema enforcement, and deterministic computation models.

---

## ⭐ **Key Features**

### 🔹 **Policy Signal Extraction**
- Inflation, growth, uncertainty, and coherence metrics  
- Hawkish/dovish classification  
- Structured speech + statement parsing  

### 🔹 **Beige Book NLP Engine**
- Canonical sentence extraction  
- LDA + RBL topic modeling  
- Tone classification across business, labor, wages, and prices  

### 🔹 **Minutes & Statement Processing**
- Risk balance scoring  
- Tone-weighted paragraph inference  
- Policy-bias quantification  

### 🔹 **Drift & Stability Metrics**
- Uncertainty drift  
- Coherence drift  
- Rolling stability windows  

### 🔹 **Regime Scoring Engine**
Uses fused signals to generate regime probabilities:

- `Disinflation_Recovery`  
- `Soft_Landing_Risk_Drift`  
- `Stagflation_Variant`  
- `Illusory_Wealth_Regime`  
- `Unknown`  

### 🔹 **Fully CPMAI-Aligned**
- Deterministic logic  
- Audit-ready metadata  
- Schema version enforcement  
- No external APIs required  

---

## 📦 **Repository Structure**

```text
fed_speak/
├── data_ingest/                   # Download & ingest Fed texts
├── preprocess/                    # Canonicalization and segmentation
├── sentiment/                     # Fed-adjusted sentiment scoring
├── features/                      # Beige/Minutes/Statement feature builders
├── drift/                         # Drift + stability metrics
├── fusion_fed_speak.py            # Composite features + regime engine
├── scripts/
│   ├── run_minutes_to_signals.py
│   ├── run_statements_features_for_spine.py
│   ├── run_beige_features_for_spine.py
│   ├── build_fed_only_macro_state.py
│   └── build_fed_drift_metrics.py
└── utils/
    ├── metadata.py
    └── schema_checks.py


# 🧠 Key Outputs

| File | Description |
|------|-------------|
| `canonical_sentences.parquet` | Cleaned, structured policy-relevant units |
| `sentiment_scores.parquet` | Fed-adjusted sentiment values |
| `beige_topics.parquet` | LDA topic distributions |
| `beige_topics_rbl.parquet` | Top-slice RBL (interpretable topics) |
| `combined_policy_leaf.parquet` | Final policy-risk leaf (∈ [-1, 1]) |

These artifacts support:
- Macro-state fusion  
- Policy-drift narratives  
- Risk diagnostics  
- Scenario commentary  
- Cross-asset interpretation  

---

# ⚙️ Usage

### Run the full Beige Book → Policy Leaf pipeline
```bash
python -m fed_speak.run_tranche1_pipeline

<p align="right">🧠 the_Spine •</p>[Return](https://github.com/sobcza11/the_Spine/tree/main)
