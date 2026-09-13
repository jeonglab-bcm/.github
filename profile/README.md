# Jeong Lab @ Baylor College of Medicine

Welcome to the GitHub home of the **Jeong Lab** (PI: Dr. Hyun-Hwan Jeong) at Baylor College of Medicine.

We build computational and AI methods for biomedicine: agentic AI systems for genetic disease discovery and research reproducibility, vision-language models for medical imaging, and statistical tools for CRISPR screens and transcriptomics. Most of our work lives in this organization; published tools are public, and active projects are private to lab members.

> 🔒 marks a private repository (visible to lab members only). 🌐 marks a public repository.

---

## 🚀 Start here

New to the lab? Two repositories hold everything you need in your first week.

### 📘 Onboarding — [`jeonglab-bcm/onboarding`](https://github.com/jeonglab-bcm/onboarding) 🔒

The onboarding repository is the lab handbook. It explains what you can expect from Dr. Jeong, what is expected of you, and the policies that help us do good science in a supportive environment. Read it once during your first week, starting with **Expectations**, and bring questions to Dr. Jeong.

| Document | What it covers |
| --- | --- |
| [Definition of Lab Membership](https://github.com/jeonglab-bcm/onboarding/blob/HEAD/lab-membership.md) | Who counts as a Jeong Lab member |
| [Expectations](https://github.com/jeonglab-bcm/onboarding/blob/HEAD/expectations.md) | Initial alignment, Dr. Jeong's responsibilities, goals by training level, authorship (COPE guidelines) |
| [Communication & Work Style](https://github.com/jeonglab-bcm/onboarding/blob/HEAD/communication.md) | Working hours, responsiveness, planned absences |
| [Lab Meetings & Journal Club](https://github.com/jeonglab-bcm/onboarding/blob/HEAD/lab-meetings.md) | Meeting schedules, formats, presentation rotation |
| [GitHub Workflow](https://github.com/jeonglab-bcm/onboarding/blob/HEAD/github-workflow.md) | How we use issues, branches, and pull requests |
| [Technical Support](https://github.com/jeonglab-bcm/onboarding/blob/HEAD/technical-support.md) | Accounts, compute, software, who to ask |
| [Using the bioinfolder Portal](https://github.com/jeonglab-bcm/onboarding/blob/HEAD/bioinfolder-portal.md) | Signing in to the lab portal and what each tool is for |
| [Conflict Resolution](https://github.com/jeonglab-bcm/onboarding/blob/HEAD/conflict-resolution.md) | How to raise and resolve disagreements |
| [Mental Health & Wellness](https://github.com/jeonglab-bcm/onboarding/blob/HEAD/mental-health.md) | BCM resources and how to ask for support |
| [Acknowledgment & Signatures](https://github.com/jeonglab-bcm/onboarding/blob/HEAD/signatures/README.md) | Sign off that you have read and agree to the expectations |

The documents are revised as the lab evolves. If something is unclear, open an issue or a pull request there.

### 🗓️ Lab Meeting — [`jeonglab-bcm/labmeeting`](https://github.com/jeonglab-bcm/labmeeting) 🔒

The lab meeting repository holds the **presentation rotation** and the **slides** from every past talk.

- **Lab meeting:** every **Tuesday at 2 PM**. A rotating presenter gives a project update or work-in-progress talk. Recent topics have ranged from VLM benchmarks for lung ultrasound and lncRNA essentiality prediction to single-cell RNA-seq of mouse tumor models, RL prefix pruning, and running local coding agents.
- **Journal club:** every **Friday at 10 AM**. No rotating presenter. Dr. Jeong posts the week's paper to the `#things-to-read` Slack channel and everyone joins the discussion.
- **Your turn:** check the schedule table in the README for your date, then add your slides as a PDF under `slides/` and link them from the table. The very first entry in the rotation is a talk on how to prepare a lab meeting, so start there.

Participation in both is expected of all lab members. Full details are in the onboarding [Lab Meetings & Journal Club](https://github.com/jeonglab-bcm/onboarding/blob/HEAD/lab-meetings.md) page.

---

## 🔬 Ongoing projects

Grouped by theme. Each line summarizes the repository's own README.

### Agentic AI for genetic disease discovery and reproducible science

| Repository | Summary |
| --- | --- |
| [`MARRVEL-Evo`](https://github.com/jeonglab-bcm/MARRVEL-Evo) 🔒 | A self-optimizing agentic system for Mendelian disease discovery, the successor to MARRVEL-MCP. Pydantic AI agent loop over 35+ FastMCP biomedical tools, typed evidence and candidate-gene outputs, a Pydantic Evals scorer (MRR, top-1, top-5), and a roadmap toward GEPA and TextGrad prompt/policy evolution. |
| [`MARRVEL_MCP_manuscript`](https://github.com/jeonglab-bcm/MARRVEL_MCP_manuscript) 🔒 | Benchmark results and figure-generation workflows for the MARRVEL-MCP paper: vanilla vs. MCP-augmented LLM runs, reviewer questionnaire spreadsheets, and model-comparison figures. |
| [`AURORA`](https://github.com/jeonglab-bcm/AURORA) 🔒 | Automated Understanding and Reproduction of Research Artifacts. A multi-agent pipeline that searches PubMed Central for autism spectrum disorder papers, extracts data from tables and figures, and independently re-implements the figures without touching the authors' code. Ships `aurora-figdiff` for side-by-side figure comparison. |
| [`dejavu`](https://github.com/jeonglab-bcm/dejavu) 🔒 | DEjaVu asks whether an auditable AI agent can reproduce published bulk RNA-seq differential-expression findings starting from the lowest public data level (FASTQ, alignments, or counts). Defines a small benchmark of 8–15 studies, a four-way reproduction classification, and strict guardrails and provenance requirements. |
| [`consol`](https://github.com/jeonglab-bcm/consol) 🌐 | ConSol (Confident Solver): a PyPI package that wraps LLM calls in sequential probability ratio tests to get consistent answers at lower token cost. Improved o3-mini accuracy on AIME24 by 10–17 points while cutting output tokens by 64–85%. |

### Vision-language models for medical imaging

| Repository | Summary |
| --- | --- |
| [`POCUS_RESEARCH`](https://github.com/jeonglab-bcm/POCUS_RESEARCH) 🔒 | Research platform for LLM interpretation of point-of-care lung ultrasound clips. Nextflow pipelines extract frames, query Claude via AWS Bedrock, and score three subtasks: pleural sliding, anterior-zone B-lines and consolidation, and posterior PLAPS with effusion type. |
| [`pocus-atlas-bench`](https://github.com/jeonglab-bcm/pocus-atlas-bench) 🌐 | Reproducibility release for the medRxiv preprint *"Morphology, Not Motion: Benchmarking Vision-Language Models on Multi-Sign Lung Ultrasound Interpretation."* Regenerates every figure and CSV byte-identically from frozen outputs of 8 models (8,010 predictions). Dataset on Hugging Face as `bcm-liuzlab/pocus-atlas-bench`. |
| [`EndoVLM`](https://github.com/jeonglab-bcm/EndoVLM) 🔒 | Using vision-language models to annotate anatomical landmarks in GI endoscopy images, later video. Currently in Phase 0: ML evaluation and CV fundamentals, a public-dataset rubric and comparison (HyperKvasir, GastroVision, and others), and a zero-shot VLM feasibility experiment ending in a GO / NO-GO call. Public data only. |
| [`GIM_Detection`](https://github.com/jeonglab-bcm/GIM_Detection) 🔒 | Gastro CV: a config-driven PyTorch pipeline for classifying and detecting GI pathologies (atrophy, GIM, polyp, tumor, ulcer) and landmarks across white-light and narrow-band endoscopy. One `ModelAdapter` registry covers timm classifiers, YOLO, U-Net, and DETR/ViT, with patient-level splits, GradCAM-to-mask explainability, and a center-bias audit. Handles PHI; read its CLAUDE.md before touching data. |

### CRISPR screen statistics and functional genomics

| Repository | Summary |
| --- | --- |
| [`BARCS`](https://github.com/jeonglab-bcm/BARCS) 🌐 | Beta-binomial Analysis and Regression for CRISPR pooled Screens. An R package that fits guide-level beta-binomial regression on any full-rank design matrix (dose, time, batch, donor, interactions) and tests coefficients with degrees of freedom from independent libraries, not read depth. Covers FASTQ quantification through gene-level summaries. |
| [`BARCS-manuscript`](https://github.com/jeonglab-bcm/BARCS-manuscript) 🌐 | Benchmarks, figures, and analysis scripts for the BARCS paper, pinning the package and CB² as submodules. Compares against MAGeCK and CRISPulator simulations. |
| [`BARCS-tex`](https://github.com/jeonglab-bcm/BARCS-tex) 🌐 | Public LaTeX mirror of the BARCS manuscript, kept in sync with Overleaf. |
| [`CB2`](https://github.com/jeonglab-bcm/CB2) 🌐 | CB² (CRISPRBetaBinomial): the lab's CRAN package for two-group CRISPR screen analysis with a beta-binomial model. Also powers CRISPRCloud. BARCS generalizes its two-group test. |
| [`lncFit`](https://github.com/jeonglab-bcm/lncFit) 🌐 | Foundation-model features and a trainable classifier pipeline for predicting lncRNA essentiality from CRISPR screens. Hosts a live leaderboard for the THP1 hold-out challenge: train on HAP1, K562, and MDA-MB-231, predict an unseen cell line, ranked by AUPRC in CI. |
| [`lncFit-groundtruth`](https://github.com/jeonglab-bcm/lncFit-groundtruth) 🔒 | Placeholder for genuinely blind hold-out labels for future lncFit challenges. Not currently in use. |
| [`SalmonTE`](https://github.com/jeonglab-bcm/SalmonTE) 🌐 | Fast, scalable quantification of transposable element abundance from RNA-seq built on Salmon, with built-in differential expression and regression (PSB 2018). Applied in a Cell Reports study of TEs in Alzheimer's disease. |

### Single-cell and organism-level transcriptomics

| Repository | Summary |
| --- | --- |
| [`mouse_brain_spleen_scRNA`](https://github.com/jeonglab-bcm/mouse_brain_spleen_scRNA) 🔒 | scRNA-seq pipeline for a CT2A glioma immunology study: a 2x2 design (pre-immunization x CT2A-gD vs. control) across brain tumor and splenocyte samples. CellRanger, DecontX, scDblFinder, Harmony, Leiden clustering into 19 annotated clusters. |
| [`scAnalytics`](https://github.com/jeonglab-bcm/scAnalytics) 🔒 | A learning-driven, agent-assisted pipeline for automated single-cell analysis: DEG (single-cell and pseudobulk), functional enrichment, cell-cell communication, pseudotime, RNA velocity, and optionally co-expression and metabolomics. |
| [`fly-spy`](https://github.com/jeonglab-bcm/fly-spy) 🔒 | Early-stage Drosophila machine-learning analysis (PyTorch, XGBoost, Optuna, marimo notebooks). No README yet. |

### Literature mining and clinical phenotyping

| Repository | Summary |
| --- | --- |
| [`exposome-ehr-review`](https://github.com/jeonglab-bcm/exposome-ehr-review) 🌐 | Reproducible pipeline that searches PubMed Central for pediatric exposome / EWAS and vaccine-exposure studies using EHR or claims data, summarizes each paper with Gemma 4 12B into a structured checklist, extracts data-availability statements, and publishes a browsable static site. 185 full-text papers so far. |
| [`POTS-phenotyping`](https://github.com/jeonglab-bcm/POTS-phenotyping) 🔒 | Harvests and structures the PubMed literature on deep phenotyping of Postural Orthostatic Tachycardia Syndrome (POTS). Early stage. |

### Lab infrastructure

| Repository | Summary |
| --- | --- |
| [`jeonglab-bcm.github.io`](https://github.com/jeonglab-bcm/jeonglab-bcm.github.io) 🌐 | Source for the lab website. |
| [`.github`](https://github.com/jeonglab-bcm/.github) 🌐 | This landing page and organization-wide GitHub defaults. |

---

## 🤝 Contributing

We work through issues, feature branches, and pull requests in every repository. See the onboarding [GitHub Workflow](https://github.com/jeonglab-bcm/onboarding/blob/HEAD/github-workflow.md) guide for conventions, and open an issue in the relevant repository if you spot a problem. To update this page, edit `profile/README.md` in the [`.github`](https://github.com/jeonglab-bcm/.github) repository.
