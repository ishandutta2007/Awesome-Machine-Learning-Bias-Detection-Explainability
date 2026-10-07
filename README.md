# Awesome-Machine-Learning-Bias-Detection-Explainability

## Top Machine Learning Bias Detection & Explainability Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Fairness Auditing, Model Interpretability & Self-Hosted XAI Libraries*  

**Last updated: October 2026**



This repository tracks notable **commercial bias detection and explainability platforms** and **open-source projects** that measure, monitor, and mitigate unfair treatment in machine learning models — from pre-training data audits and post-training fairness metrics to model-agnostic explainability libraries.



**Examples** include Amazon SageMaker Clarify, Fiddler AI, Arize AI, TruEra, WhyLabs, Credo AI, Arthur AI, Holistic AI, FairNow, and Monitaur (the category leaders).



**Open-source emphasis**: ML bias detection and explainability is one of the strongest open-source domains. **bias-scope** brings four families of bias metrics for language models under one consistent API . **LangFair** from CVS Health tests LLMs for bias and fairness with task-specific evaluation . **FairMind** provides an open-source platform for AI governance and bias testing . **Explainiverse** unifies 8 state-of-the-art XAI methods with a plugin registry . **PyXAI** brings formal explanations to tree-based models . **GovLLM** implements runtime LLM governance with small language model judges . This section is heavily expanded.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Amazon SageMaker Clarify](https://aws.amazon.com/sagemaker/clarify/)**  

  **AWS's purpose-built bias detection and explainability service** — 8 pre-training bias metrics (Class Imbalance, Difference in Proportions of Labels, KL Divergence, Jensen-Shannon Divergence, Conditional Demographic Disparity) and 13 post-training metrics (Accuracy Difference, Difference in Acceptance Rate, Recall Difference, Disparate Impact, Treatment Equality) . **SHAP-based explainability** shows which features drive each prediction. **Monitoring** detects bias drift in production alongside SageMaker Model Monitor . **Bias gates in pipelines** can block model deployment if disparate impact falls outside acceptable range . **Best for AWS-native ML workflows**.



- **[Fiddler AI](https://www.fiddler.ai/)**  

  **Model Performance Management (MPM) platform** with comprehensive explainability . **Artifact status tiers**: No Model (monitoring only), Surrogate (Fiddler-generated for basic explainability), and User Uploaded (full explainability with actual model) . **All-purpose explainable AI** for tabular ML to complex multimodal deep learning. **Pluggable deployment** on-premise and multi-cloud (AWS, GCP, Azure). **Enterprise security certifications** for financial services and healthcare . **Best for enterprises needing full model explainability**.



- **[Arize AI](https://arize.com/)**  

  **ML observability platform** for monitoring, troubleshooting, and explaining models . **Model fairness/bias metrics** surfaced alongside drift, data quality, and performance degradation. **OpenInference SDK** instruments traces to expose hallucinations, drift, and bias in the request path . **Deployed as SaaS or on-premise** — platform and model agnostic . **Best for production ML observability with fairness**.



- **[TruEra](https://truera.com/)**  

  **AI Quality Management platform** — test, evaluate, explain, monitor, and debug models . **Automated Test Harness** for systematic testing across performance, drift, bias/fairness, feature importance. **Segment analytics** automatically generate high-error segments. **Root cause analysis** informs directed retraining . **Best-in-class explainability** with SHAP and proprietary faster technology. **Best for retail and brands with systematic AI quality needs** .



- **[WhyLabs](https://whylabs.ai/)**  

  **AI Control Center** with Observe, Secure, and Optimize capabilities . **100% data observability** — no sampling, no false alarms from distorted distributions. **Privacy-preserving telemetry** via whylogs and LangKit. **Data cohorts** identify problematic segments that might indicate model bias. **Real-time guardrails** for LLM safety. **Best for healthcare and FinTech with high inference volumes** .



- **[Credo AI](https://www.credo.ai/)**  

  **AI governance platform** with agent registry, risk intelligence, and policy engine . **Policy packs** for EU AI Act, NIST AI RMF, ISO 42001 written by standards-body experts. **Continuous governance loop** — not point-in-time audits. **Agentic risk library** for tool misuse, scope drift, and inter-agent risk. **Integrates with Snowflake, Databricks, AWS, Azure, MLflow** . **Best for enterprises scaling AI governance**.



- **[Arthur AI](https://arthur.ai/)**  

  **Model monitoring and explainability** with inference deep dive, session filters for traces, and built-in evaluators . **Policy alert rule traceability** — trace alerts back to exact policy rule. **Dataset-to-trace back-linking** for curated examples. **Best for GenAI and traditional ML monitoring**.



- **[Holistic AI](https://www.holisticai.com/)**  

  **AI risk management and governance** platform for enterprise fairness and compliance.



- **[FairNow](https://fairnow.ai/)**  

  **AI governance and fairness** platform for regulatory compliance.



- **[Monitaur](https://www.monitaur.ai/)**  

  **AI assurance and governance** platform for regulated industries.



## Open-Source GitHub Projects



### Language Model Bias Detection



- **[bias-scope](https://github.com/RAINLabLAU/bias_scope)**  

  **A Python library for measuring bias in language models across four complementary families of metrics**, open-source . **Embedding-based metrics**: WEAT, SEAT, CEAT, SentenceBiasScore, and an `embed()` helper for built-in text embedding. **Probability-based metrics**: CrowS-Pairs, AUL, AULA, CAT, ICAT, LMB, LPBS, CBS, DisCoMetric, BertPLLScorer, TokenPredictionScorer. **Generated-text metrics**: ScoreParity and others. **Prompt-based benchmarks**: BBQ and more. **Consistent metric classes** with `.evaluate()` entrypoints, optional model adapters, and support for both raw-text convenience and precomputed inputs . **Best for comprehensive LLM bias evaluation**.



- **[LangFair](https://github.com/cvs-health/langfair)**  

  **Open-source Python library from CVS Health for testing LLMs for bias and fairness**, open-source with 262+ GitHub stars . **Designed around the idea that bias risk depends on how the LLM is actually used** — not one-size-fits-all benchmarks . **Metrics for toxicity, stereotyping, counterfactual fairness** (whether outputs change based on protected attributes), and **allocational harms** in classification or recommendation tasks. **Adversarial testing** surfaces worst-case model behaviour. **Decision framework** guides metric selection. **Works without internal model access** — relies only on model outputs, so developers, auditors, and governance bodies can apply it to models they don't control . **Methodology published in Journal of Open Source Software**. **Best for task-specific LLM fairness testing**.



### Explainable AI Frameworks



- **[Explainiverse](https://github.com/jemsbhai/explainiverse)**  

  **Unified, extensible Python framework for Explainable AI (XAI)**, open-source . **8 state-of-the-art XAI methods**: Local explainers (LIME, SHAP via KernelSHAP, Anchors, Counterfactual via DiCE-style) and Global explainers (Permutation Importance, Partial Dependence, ALE, SAGE). **Extensible plugin registry** — register custom explainers with rich metadata, filter by scope, model type, and data type, and get automatic recommendations . **Evaluation metrics**: AOPC (Area Over Perturbation Curve) and ROAR (Remove And Retrain). **Standardized interface** with `BaseExplainer` API and `UnifiedExplanation` output format. **Model adapters** for sklearn and more. **Best for model-agnostic explainability**.



- **[PyXAI](https://github.com/crillab/pyxai)**  

  **Python library for formal explanations suited to tree-based ML models** (Decision Trees, Random Forests, Boosted Trees), open-source with 41+ GitHub stars . **Formal explainability** — mathematically rigorous explanations rather than approximations. **Best for tree-based model explainability**.



### AI Governance & Compliance Platforms



- **[FairMind](https://github.com/adhit-r/fairmind)**  

  **Open-source platform for AI governance and assurance**, MIT licensed . **Evaluates AI systems for bias and safety** and collects reliable evidence for governance frameworks. **Fairness metrics** including demographic parity, equalised odds, and disparate impact. **Legacy features generate example code for reducing bias** — reweighting data, adjusting decision thresholds . **Results log to MLflow and Weights & Biases**. **New assurance foundation** records each evaluation evidence with exact scope, source, and review status — evidence can be signed, checked for authenticity, and expires when no longer current. **Planned mappings** to EU AI Act, ISO/IEC 42001, NIST AI RMF, and India's DPDP Act . **Best for AI governance with evidence recording**.



- **[VerifyWise](https://github.com/verifywise-ai/verifywise)**  

  **Open-source platform for AI governance, risk, and compliance**, open-source with 354+ GitHub stars . **Central repository for AI governance** — register AI systems, models, agents, applications, and suppliers in a structured inventory. **Risk assessments, governance decisions, evaluations, responsibilities, and mitigation tracking** through built-in workflows. **Maps governance activities across multiple frameworks simultaneously** — record evidence once and reuse across EU AI Act, ISO/IEC 42001, and NIST AI RMF obligations . **Continuous monitoring** of risk levels, controls, compliance status, and audit evidence over time. **Best for multi-framework AI compliance**.



- **[GovLLM](https://github.com/ai4gov/govllm)**  

  **Open-source runtime governance framework for LLM systems**, EUPL 1.2 licensed with 30+ GitHub stars . **Treats regulatory compliance as continuous signal from production observability** — not static audit verdict . **Panel of small language model judges** (1.7B-7B parameters) each assigned to a regulatory criterion (transparency, data privacy, non-manipulation, prompt injection resistance, human oversight). **Runs fully on-premise via Ollama** — no data leaves infrastructure. **Governance-driven routing** selects models based on accumulated compliance scores. **Four-zone model lifecycle** (test → human validation → production → quarantine) implements AI Act art. 9 continuous risk management . **Validated through 585 judge runs, 2340 individual assessments** — specialised panel outperforms best single judge by 10.9 percentage points. **Best for on-premise LLM compliance monitoring**.



### Additional Strong Open-Source Options



- **Opik** — Open-source LLM observability platform with guardrails, tracing, and evaluation. Self-hosted via Docker or Kubernetes with Helm .

- **LIME** — Local Interpretable Model-agnostic Explanations (foundational XAI method).

- **SHAP** — SHapley Additive exPlanations (foundational XAI method).

- **Fairlearn** — Microsoft's fairness assessment and mitigation toolkit.

- **AI Fairness 360** — IBM's comprehensive fairness metrics and algorithms.

- **What-If Tool** — Google's visual model analysis and fairness exploration.

- **InterpretML** — Microsoft's interpretable machine learning toolkit.

- **Captum** — PyTorch model interpretability library.

- **Alibi** — Python library for machine learning model inspection and interpretation.

- **DALEX** — Descriptive mAchine Learning EXplanations for R and Python.



**Frameworks for building custom bias detection and explainability solutions**: Combine **bias-scope** for comprehensive LLM bias evaluation across embedding, probability, generated-text, and prompt-based metrics . Use **LangFair** for task-specific LLM fairness testing that works without internal model access . Deploy **Explainiverse** for model-agnostic explainability with 8 XAI methods and plugin extensibility . Choose **FairMind** for AI governance with signed evidence recording and regulatory framework mapping . Integrate **VerifyWise** for multi-framework compliance management . Use **GovLLM** for on-premise LLM compliance monitoring with judge panels . Note that true enterprise bias detection and explainability with managed infrastructure, automatic scaling, and vendor-supported SLAs (SageMaker Clarify, Fiddler AI, TruEra) remains primarily commercial territory; open-source stacks provide strong bias measurement, XAI methods, and governance frameworks that require integration for complete responsible AI platforms.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Bias detection and explainability tools process sensitive model data and may involve protected attributes. Self-hosted solutions require proper security hardening, access controls, and compliance with data privacy regulations.

- **Bias metrics are diagnostic, not prescriptive** — a statistical disparity does not automatically mean discrimination. Context, domain expertise, and legal review are essential before drawing conclusions .

- **Explainability methods have trade-offs** — SHAP and LIME produce approximations; PyXAI provides formal explanations for tree-based models . No single method is universally best — choose based on model type, data, and stakeholder needs .

- **License considerations**: bias-scope is open-source , LangFair is open-source , FairMind uses MIT , Explainiverse is open-source , and GovLLM uses EUPL 1.2 . Verify licensing against your use case before committing.

- The open-source ecosystem provides strong bias measurement, XAI methods, and governance frameworks, but **managed infrastructure, automatic scaling, and vendor-supported SLAs** remain primarily commercial offerings.



---



**Made for ML engineers, responsible AI practitioners, and organizations seeking bias detection and explainability sovereignty.**

Let's make machine learning bias detection and explainability more open, transparent, and accountable.
