# 🌟 SITF-HCL Protocol: The Social Impact Tokenization Framework - Human Capital Ledger

![GitHub Repo Size](https://img.shields.io/github/repo-size/ChathuraMalinga/sitf-hcl-Protocol?style=for-the-badge)
![GitHub Last Commit](https://img.shields.io/github/last-commit/ChathuraMalinga/sitf-hcl-Protocol?style=for-the-badge)
![GitHub Contributors](https://img.shields.io/github/contributors/ChathuraMalinga/sitf-hcl-Protocol?style=for-the-badge)
![GitHub Open Issues](https://img.shields.io/github/issues/ChathuraMalinga/sitf-hcl-Protocol?style=for-the-badge)
![License](https://img.shields.io/github/license/ChathuraMalinga/sitf-hcl-Protocol?style=for-the-badge)

---

## 🚀 I. Project Overview: The Crisis of Trust

The **SITF-HCL Protocol** solves the global crisis of trust in social impact reporting. Currently, verifiable proof of skill and long-term job commitment is non-existent, reliant on easily falsified paper or fragmented databases.

### The Solution: Digital Trust Stamp

We are building a free, open-source **DLT (Distributed Ledger Technology)** protocol to provide an **unbreakable, verifiable digital fingerprint** for human capital achievements. This is the **Commitment-Proof Voucher (CPV)**.

* **Core Principle:** We provide the free, open-source tool for **verification**. Our commercial entity (Vetted AI) monetizes the **prediction** and **scale** built on this trusted data.

### 🎯 Global Alignment (SDGs)

The protocol is a direct technical solution to these global goals:
* **SDG 8 (Decent Work):** Providing verifiable proof of stable job retention.
* **SDG 4 (Quality Education):** Standardizing and certifying auditable skills acquisition.
* **SDG 5/10 (Equality):** Ensuring the digital proof is portable and worker-owned.

---

## II. Architecture & Core Components

The SITF-HCL is an efficient, non-cryptocurrency DLT designed for speed and data assurance.

### 1. The Core DLT Components

| Component | Analogy (Simple Explanation) | Technical Function |
| :--- | :--- | :--- |
| **Commitment-Proof Voucher (CPV)** | **The Digital Fingerprint** | A secure, irreversible cryptographic hash (SHA-256) of a worker's milestone record. **No PII is stored on the ledger.** |
| **Micro-Audit Protocol (MAP)** | **The Global Truth Check** | The core function that instantly verifies a CPV's integrity against the decentralized ledger. |
| **API Endpoints** | **The Integration Toolkit** | RESTful access points for enterprises and NGOs to issue and verify CPVs. |

### 2. API Access and Standards

The protocol is consumed via a production-grade API.

**API Base URL:** `https://api.fairdigit.org/v1/`

| Action | API Endpoint Example | Purpose |
| :--- | :--- | :--- |
| **Issue Proof** | `POST /issue/cpv` | Records the immutable hash (fingerprint) onto the ledger. |
| **Verify Proof** | `GET /verify/cpv/{voucher_id}` | Instantly checks the hash integrity against the global ledger. |

---

## III. 🔑 How to Use the Protocol (Quickstart Guide)

This guide is for developers and architects who want to integrate the SITF-HCL verification into their existing systems.

### A. Prerequisites

* Python 3.8+ (for core code review and local testing)
* API Key (will be required for production use of `api.fairdigit.org`)

### B. Local Setup and Testing

To test the core verification logic (the MAP) locally:

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/ChathuraMalinga/sitf-hcl-Protocol.git](https://github.com/ChathuraMalinga/sitf-hcl-Protocol.git)
    cd sitf-hcl-Protocol
    ```
2.  **Install Dependencies:** (Ensure required hashing and utility libraries are installed)
    ```bash
    pip install -r requirements.txt
    ```
3.  **Run Local MAP Test:** The `map_protocol_core.py` script simulates CPV creation and hash verification.
    ```bash
    python map_protocol_core.py
    ```
    *Expected Output: `[SUCCESS] Micro-Audit Protocol (MAP) Result: DATA INTEGRITY VALID`*

### C. Enterprise Integration Steps

1.  **Standardize Data:** Ensure your system's data for a verified milestone aligns exactly with the **CPV JSON Schema** defined in the [Wiki].
2.  **Generate Hash (Local/API):** Use the core hashing function (or the `POST /issue/cpv` API) to generate the cryptographic fingerprint.
3.  **Store and Link:** Record the returned `voucher_id` and `transaction_hash` in your internal database, linking it to the worker record.
4.  **Verify:** Call the `GET /verify/cpv/{voucher_id}` API endpoint from your partner system (e.g., HR/Auditor) to prove the integrity of the data.

---

## IV. 📊 Kaggle & AI Strategy: Fueling Future Vetted AI

The **SITF-HCL Protocol** is being built to be backed by AI. We leverage the entire Kaggle ecosystem to test, optimize, and validate the protocol's data structure for machine learning compatibility.

| Kaggle Option | SITF-HCL Application | Contribution Focus |
| :--- | :--- | :--- |
| **Competitions** | **Trust Score Optimization Challenge:** Focus on security, DLT efficiency, and latency reduction in the MAP. | Optimization Algorithms and Cryptographic Review. |
| **Datasets & Models** | Publishing **Synthetic Ledger Data** (CPV Schema) on Kaggle. | Data analysis to confirm the *predictive signal* in the CPV data for future AI development. |
| **Code Collections** | Sharing SDKs, benchmark models, and EDA Notebooks. | Building integration tools to accelerate adoption and research. |


## 🤖 AI & Machine Learning Integration
The SITF-HCL Protocol is backed by a cloud-integrated AI engine hosted on Kaggle.

### Current Capabilities:
* **Institutional Trust Index:** Automates the calculation of organizational reliability using a proprietary hashing-to-score algorithm.
* **Turnover Prediction (Vetted AI Alpha):** Uses Random Forest Classifiers to identify workforce stability risks with high precision.
* **Decentralized Analytics:** Analyzes impact across `did:hcl` identifiers without compromising individual worker privacy.

### Key Metrics (Latest Simulation):
| Metric | Result |
| :--- | :--- |
| **Top Organization Trust** | 71.26 (Issuer: `did:hcl:60c4694e26d3`) |
| **Prediction Accuracy** | [Insert F1-Score from your Kaggle Report]% |
| **Ledger Volume** | 5,000+ Verified Vouchers |


$T_i$ (Trust Index): $T_i = B + (\frac{D}{365} \times W_t) + (M \times W_m) + (I \times 100)$, where $B$ is baseline, $D$ is tenure days, $M$ is milestone weight, and $I$ is issuer impact.Risk Threshold: $R < 68$. Any entity falling below this threshold is flagged for "Retention Intervention."Data Schema v1.1: Added hcl_trust_index and is_at_risk as synthetic feature labels for ML training.
---

## V. Community Hub and Links

We welcome all developers, data scientists, researchers, and technical writers. Please utilize the official GitHub tools below to contribute and communicate.

### 1. Essential Documentation

* **[Wiki]** (Tab Link): The central handbook for architecture, design principles, and comprehensive standards. **(Required Reading for Architects)**
* **[CONTRIBUTING.md]**: **REQUIRED READING** for the developer workflow, legal boundaries, and AI/DLT firewall rules.
* **[CODE_OF_CONDUCT.md]**: Our ethical guidelines for maintaining a respectful community.
* **[LICENSE]**: The official MIT License text.
* **[SECURITY.md]**: Our policy on reporting vulnerabilities privately.

### 2. Communication & Development Workflow

| GitHub Feature | Purpose | Action for Contributors |
| :--- | :--- | :--- |
| **[Issues]** (Tab Link) | Reporting bugs, security flaws, and defining new feature requests. | **Use this to claim a task or report a problem.** |
| **[Pull requests]** (Tab Link) | Submitting final code for review and integration into the `main` branch. | **Use this to submit your completed work.** |
| **[Discussions]** (Tab Link) | Conceptual conversations, ethical questions, and roadmap input. | **Use this for non-code, high-level strategy.** |
| **[Actions]** (Tab Link) | Viewing CI/CD (Continuous Integration/Continuous Delivery) pipeline status and automated testing results. | **Check this before submitting a PR to ensure your changes pass tests.** |
| **[Projects]** (Tab Link) | Tracking the overall roadmap, milestones, and high-priority work streams. | **Review this to understand project priorities.** |

---

### 3. Legal and Attribution

* **Repository Owner:** ChathuraMalinga
* **License:** MIT License

**Join us in building the digital standard for verifiable global impact.**
