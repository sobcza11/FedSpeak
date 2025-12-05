# <p align="center">*FedSpeak* • 🗣️ • Policy Signals → Structured Intelligence</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10%2B-blue" />
  <img src="https://img.shields.io/badge/PMI–CPMAI-Aligned-D4AF37" />
  <img src="https://img.shields.io/badge/NLP-PoliSci-4B0082" />
  <img src="https://img.shields.io/badge/Topic_Modeling-LDA_%7C_RBL-6A5ACD" />
  <img src="https://img.shields.io/badge/Sentiment-Targeted_Tone-2E8B57" />
  <img src="https://img.shields.io/badge/MLOps-R2_Mirroring_%7C_Lineage-2F4F4F" />
  <img src="https://img.shields.io/badge/Creative_Commons-CC_BY_4.0-2F4F4F" />
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/sobcza11/FedSpeak/main/_assets/FedSpeak.png" width="720">
</p>

## 🗣️ FedSpeak Status • *Integration Snapshot*

| Component | Status | Notes |
|----------|--------|-------|
| **Beige Book** | ✅ **Complete** | Canonical sentences → Topic leaves (LDA/RBL) → Sentiment → R2 |
| **Fed Statements** | 🟡 **Partial** | Parsing stable; awaiting tone-weight logic + hawk/dove scoring |
| **FOMC Minutes** | 🟥 **Pending** | Canonical extraction + paragraph segmentation pipeline next |
| **SEP (Dot Plot)** | 🟡 **Partial** | Template for sentiment + neutral-rate drift defined; not populated yet |
| **Fed Speeches** | 🟡 **Partial** | Multi-speaker canonical leaf planned; speaker-ID mapping staged |
| **Fusion into `p_Sentiment_US`** | 🟡 **In Progress** | All Beige outputs + policy leaves flowing to R2; fusion rules pending |


FedSpeak extracts structured meaning from every major policy-communication channel:
### Beige Book
District-level tone on:
- business conditions
- labor markets
- wages + compensation
- prices + supply chains

### FOMC Minutes
- disagreement
- uncertainty posture
- inflation vs. growth emphasis

### FOMC Statement
- hawkish/dovish shifts
- forward-guidance direction
- paragraph-level emphasis

### SEP (Dot Plot) (future tranche)
- rate-path expectations
- neutral-rate drift

### Fed Speeches (future tranche)
- speaker-specific tone
- drift across governors
- certainty vs. contingency language

Outputs feed downstream into `p_FedSpeak_US`, directly integrated into the_Spine and the_OracleChambers.

<p align="center">📦 Repository Structure</p>
fed_speak/
├── inputs/                   # Scraping / ingestion
├── preprocess/               # Canonical sentences
├── sentiment/                # VADER + FedLex adjustments
├── topic/                    # LDA + RBL (top-slice)
├── leaves/                   # Policy leaf fusion (final signal)
├── utils/                    # R2 upload + general utilities
└── run_tranche1_pipeline.py  # Full BeigeBook → Policy Leaf pipeline

<p align="center">🧠 Key Outputs</p>
File	Description
canonical_sentences.parquet	Cleaned, structured linguistic units
sentiment_scores.parquet	Targeted tone scoring
beige_topics.parquet	LDA topic distributions
beige_topics_rbl.parquet	RBL topic slices (high interpretability)
combined_policy_leaf.parquet	Final fused policy signal

These artifacts enable:

macro-state fusion

policy-drift narratives

scenario commentary

cross-asset interpretation

explainable macro pipelines

<p align="center">⚙️ Usage</p>
Run full Beige Book → Policy Leaf pipeline
python -m fed_speak.run_tranche1_pipeline

Upload all processed outputs to Cloudflare R2
python -m fed_speak.utils.backfill_r2

Prepare multi-channel leaf (future)
python -m fed_speak.leaves.fed_multichannel_leaf

<p align="center">🔒 R2 Configuration</p>

Set environment variables:

PowerShell

$env:R2_ACCESS_KEY_ID="YOUR_KEY"
$env:R2_SECRET_ACCESS_KEY="YOUR_SECRET"


Bash

export R2_ACCESS_KEY_ID="YOUR_KEY"
export R2_SECRET_ACCESS_KEY="YOUR_SECRET"


R2 mirroring ensures lineage, availability, and reproducibility across the entire macro stack.

<p align="center">🔮 CPMAI Alignment</p>

FedSpeak follows the CPMAI model used across your ecosystem:

Phase I — policy domain understanding

Phase II — data governance + exploration

Phase III — modeling (LDA, RBL, sentiment)

Phase IV — validation + lineage

Phase V — deployment (R2 mirroring)

Phase VI — monitoring + drift evaluation

<p align="center">🧭 Roadmap</p>
Tranche II

FOMC Minutes ingestion

Multi-speaker drift

SEP tone extraction

Tranche III

Hawk–Dove Index

Forward-guidance classification

Tranche IV

Real-time Fed drift monitor

Cross-asset reaction overlays

Expansion: ECB, BoE, BoJ
[Return](https://github.com/sobcza11/the_Spine/tree/main)

<p align="right">***🧠 the_Spine •*** [Return](https://github.com/sobcza11/the_Spine/tree/main)</p>
