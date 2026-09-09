# FedGuard-XAI

**A Federated, Adversarially-Robust, and Explainable Deep Learning Framework 
for Intrusion and Anomaly Detection in Multi-Tenant Cloud Environments**

> Cutoff 1 Research Proposal — Cloud Computing Security using Federated Deep Learning

---

## Overview

Cloud computing's multi-tenant, shared-infrastructure model creates security 
risks that traditional and even many ML-based intrusion detection systems 
(IDS) fail to fully address — particularly around **data privacy**, 
**adversarial robustness**, and **explainability**. This project designs and 
evaluates a federated deep learning IDS that:

1. Trains collaboratively across simulated cloud tenants **without sharing raw data** (Federated Learning)
2. Is hardened against **adversarial evasion attacks** (adversarial training)
3. Produces **human-interpretable explanations** for its predictions (XAI)

---

## Research Question

> Can a federated deep learning-based intrusion detection framework, hardened 
> with adversarial training and augmented with explainable AI, achieve 
> detection performance comparable to centralized DL models on novel/zero-day 
> attacks, while preserving tenant data privacy and improving interpretability?

## Objectives

- [ ] Design a federated deep learning architecture (CNN/LSTM) for cloud IDS
- [ ] Integrate adversarial training (FGSM/PGD) into the federated pipeline
- [ ] Integrate explainability (SHAP/LIME) for detection outputs
- [ ] Benchmark against centralized DL baselines on accuracy, robustness, 
      privacy, and interpretability

---

## Repository Structure

FedGuard-XAI/
├── data/ # Dataset download/preprocessing scripts (not raw data)
│ └── preprocess.py
├── federated/ # FL client/server simulation code
│ ├── client.py
│ ├── server.py
│ └── fed_avg.py
├── adversarial/ # Adversarial attack/training scripts
│ └── fgsm_pgd.py
├── explainability/ # SHAP/LIME analysis notebooks
│ └── shap_analysis.ipynb
├── models/ # Model architectures (CNN/LSTM)
│ └── ids_model.py
├── experiments/ # Experiment configs and results
│ ├── configs/
│ └── results/
├── docs/ # Proposal, reports, slides
│ ├── proposal.pdf
│ └── slides.pdf
├── requirements.txt
├── LICENSE
└── README.md


---

## Tech Stack

| Component | Tool |
|---|---|
| Deep Learning | PyTorch |
| Federated Learning | Flower (`flwr`) |
| Adversarial Attacks | Adversarial Robustness Toolbox (ART) |
| Explainability | SHAP, LIME |
| Datasets | CICIDS2017/2018, NSL-KDD, UNSW-NB15 |
| Experiment Tracking | Weights & Biases / MLflow |

---

## Datasets

Publicly available network/cloud intrusion detection datasets, partitioned 
in a **non-IID** fashion across simulated tenant clients to reflect realistic 
multi-tenant cloud environments:

- [CICIDS2017/2018](https://www.unb.ca/cic/datasets/ids-2017.html)
- [NSL-KDD](https://www.unb.ca/cic/datasets/nsl.html)
- [UNSW-NB15](https://research.unsw.edu.au/projects/unsw-nb15-dataset)

> Raw datasets are **not** committed to this repository. Run 
> `data/preprocess.py` after downloading locally.

---

## Getting Started

```bash
# Clone the repository
git clone https://github.com/<team-org>/FedGuard-XAI.git
cd FedGuard-XAI

# Create environment
python -m venv venv
source venv/bin/activate      # Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Preprocess data (after manual download)
python data/preprocess.py --dataset cicids2017

# Run federated training simulation
python federated/server.py &
python federated/client.py --client_id 0
python federated/client.py --client_id 1
```

---

## Team

| Name | Role |
|---|---|
| Student 1 | Hadi Saleemi - 22i-1043 |
| Student 2 | Zainab Fatima - 22i-1064 |

---

## Key References

1. Al Morsy, Grundy & Müller, *An analysis of the cloud computing security problem*, arXiv:1609.01107, 2016.
2. Arogundade, *Addressing cloud computing security and visibility issues*, IARJSET, 2023.
3. Alzoubi, Mishra & Topcu, *Research trends in deep learning and machine learning for cloud computing security*, Artificial Intelligence Review, 2024.
4. Ahmadi, *Systematic literature review on cloud computing security: threats and mitigation strategies*, Journal of Information Security, 2024.
5. Khan, Hussain & Islam, *Optimizing content cache with vehicular edge computing: a deep federated learning based novel predictive study*, 2024.
6. McMahan et al., *Communication-efficient learning of deep networks from decentralized data*, AISTATS, 2017.
7. Goodfellow, Shlens & Szegedy, *Explaining and harnessing adversarial examples*, ICLR, 2015.
