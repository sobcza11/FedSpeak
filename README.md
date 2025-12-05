# <p align="center">*FedSpeak* • 🗣️ • Policy Signals → Structured Intelligence</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10%2B-blue" />
  <img src="https://img.shields.io/badge/PMI--CPMAI-Aligned-D4AF37" />
  <img src="https://img.shields.io/badge/NLP-PoliSci-4B0082" />
  <img src="https://img.shields.io/badge/Topic_Modeling-LDA_%7C_RBL-6A5ACD" />
  <img src="https://img.shields.io/badge/Sentiment-Targeted_Tone-2E8B57" />
  <img src="https://img.shields.io/badge/MLOps-R2_Mirroring_%7C_Lineage-2F4F4F" />
  <img src="https://img.shields.io/badge/Creative_Commons-CC_BY_4.0-2F4F4F" />
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/sobcza11/FedSpeak/main/_assets/FedSpeak.png" width="720">
</p>

---

**FedSpeak** is a domain-specific *Policy Language Intelligence Engine* that transforms Federal Reserve communication into:

- **Policy-risk signals** — `inflation_risk`, `growth_risk`, `policy_bias`
- **Regime labels** — `hawkish`, `neutral`, `dovish`, `unknown`
- **Drift diagnostics** — governed z-score deviations against a baseline
- **Stability summaries** — quarter-over-quarter tone consistency

FedSpeak serves as the *policy backbone* for:

- **the_Spine** — macro fusion engine  
- **the_OracleChambers** — interpretive + narrative layer  

FedSpeak supports academic research, RegTech workflows, and supervisory-aligned analysis through **governed, transparent, CPMAI-aligned NLP pipelines**.

---

# 🗣️ Integration Snapshot (Truth-Aligned)

| Component | Status | Notes |
|----------|--------|-------|
| **Beige Book** | ✅ **Complete** | Canonical sentences → LDA/RBL topics → sentiment → fused into `combined_policy_leaf` |
| **Fed Statements** | 🟡 **Partial** | Parsing complete; tone-weighting + hawk/dove logic planned |
| **FOMC Minutes** | 🟥 **Pending** | Needs ingestion → canonicalization → paragraph segmentation |
| **SEP (Dot Plot)** | 🟡 **Partial** | Sentiment template + schema drafted; not yet populated |
| **Fed Speeches** | 🟡 **Partial** | Speaker-ID mapping staged; canonical leaf not yet built |
| **Fusion into `p_Sentiment_US`** | 🟡 **In Progress** | Beige fully fused; multi-channel fusion ready once remaining leaves exist |

**TRANCHE 1 Universities:**  
FedSpeak is delivery-ready with full Beige Book pipelines, metadata governance, drift/stability diagnostics, and a validated fusion interface.

---

# 🧠 What FedSpeak Extracts

### **Beige Book**
Structured tone on:
- Business conditions  
- Labor markets  
- Wages & compensation  
- Prices & supply chain pressure  

### **FOMC Minutes** *(future tranche)*
- Committee disagreement  
- Risk balance (inflation vs. growth)  
- Uncertainty structure  

### **FOMC Statement**
- Hawkish/dovish posture  
- Forward-guidance shifts  
- Paragraph-level emphasis  

### **SEP (Dot Plot)** *(future tranche)*
- Rate-path sentiment  
- Neutral-rate drift detection  

### **Fed Speeches** *(future tranche)*
- Governor-specific tone  
- Conviction & uncertainty  
- Drift over time  

Outputs integrate into:
- `p_FedSpeak_US`
- `p_Sentiment_US`
- the_Spine (macro fusion)
- the_OracleChambers (interpretation layer)

---

# 📦 Repository Structure
```text
fed_speak/
├── inputs/                   # Scraping / ingestion
├── preprocess/               # Canonical sentences
├── sentiment/                # VADER + FedLex adjustments
├── topic/                    # LDA + RBL (top-slice)
├── leaves/                   # Policy leaf fusion (final signal)
├── utils/                    # R2 upload + general utilities
└── run_tranche1_pipeline.py  # Full BeigeBook → Policy Leaf pipeline
```
---

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
