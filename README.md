# FedGuard-XAI

A Conceptual Framework for Federated, Adversarially-Aware, and Explainable
Deep Learning-Based Intrusion Detection in Multi-Tenant Cloud Environments

Cutoff 1 Research Proposal — Cloud Computing Security

---

## Overview

Cloud computing's multi-tenant, shared-infrastructure model creates security
risks that traditional and even many ML-based intrusion detection systems
(IDS) do not fully address, particularly around data privacy, adversarial
robustness, and explainability. A recent bibliometric review of the field
(Alzoubi et al., 2024) names federated learning as a promising but
under-developed direction for cloud security and stops there.

This project takes that stated gap as its starting point. It does not
implement or benchmark a full system. Instead, it proposes a conceptual
reference architecture combining:

1. Federated learning (FL) for privacy-preserving collaborative training
   across cloud tenants
2. Adversarially-aware training principles for robustness against evasion
   attacks
3. Explainable AI (XAI) for interpretable detection outputs

and reasons about expected performance, trade-offs, and feasibility using
evidence already reported in existing literature.

---

## Research Question

What would a federated, adversarially-aware, and explainable deep learning
framework for cloud intrusion detection look like, and, based on evidence
already reported in the literature, what performance characteristics,
trade-offs, and feasibility concerns can reasonably be anticipated?

## Objectives

- Synthesize existing literature on FL, adversarial robustness, and XAI as
  applied separately to cloud/network security, and identify why they have
  not yet been combined
- Propose a conceptual reference architecture integrating these three
  components for multi-tenant cloud intrusion detection
- Reason, using evidence from existing studies, about the expected
  performance profile, privacy benefits, and adversarial resilience of the
  proposed architecture
- Identify open feasibility questions and outline a roadmap for future
  empirical validation

---

## Scope

This is a conceptual/design-stage proposal, not an implementation. No model
training, attack simulation, or benchmarking is performed at this stage.
The deliverables are: a literature synthesis, a proposed architecture, a
reasoned discussion of expected behavior, and a list of open questions for
future empirical work.

---

## Repository Structure
FedGuard-XAI/
├── docs/
│ ├── proposal.tex # Cutoff 1 proposal (Overleaf source)
│ ├── proposal.pdf
│ └── slides.pdf
├── literature/
│ ├── synthesis.md # Structured notes per component (FL, adversarial, XAI)
│ └── references.bib
├── architecture/
│ └── reference_architecture.png # Proposed conceptual diagram
├── README.md
└── LICENSE


---

## Team

| Name | Roll Number | Role |
|---|---|---|
| Hadi Saleemi | 22i-1043 |
| Zainab Fatima | 22i-1064 |

Institution: FAST National University of Computer and Emerging Sciences (FAST-NUCES)


---

## Key References

1. Al Morsy, Grundy, and Muller, "An analysis of the cloud computing security problem," arXiv:1609.01107, 2016.
2. Arogundade, "Addressing cloud computing security and visibility issues," IARJSET, 2023.
3. Alzoubi, Mishra, and Topcu, "Research trends in deep learning and machine learning for cloud computing security," Artificial Intelligence Review, 2024.
4. Ahmadi, "Systematic literature review on cloud computing security: threats and mitigation strategies," Journal of Information Security, 2024.
5. Khan, Hussain, and Islam, "Optimizing content cache with vehicular edge computing: a deep federated learning based novel predictive study," 2024.
6. McMahan et al., "Communication-efficient learning of deep networks from decentralized data," AISTATS, 2017.
7. Goodfellow, Shlens, and Szegedy, "Explaining and harnessing adversarial examples," ICLR, 2015.

---
