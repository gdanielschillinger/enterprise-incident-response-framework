# Enterprise Incident Response Framework & Strategic Policy

### 🛡️ Governance | Risk | Compliance (GRC)

**Project Status:** v3 (Portfolio-Ready)
**Standards:** NIST SP 800-61 Rev. 2, NIST SP 800-83, SANS Institute, CISA Playbooks (2025)

---

## 📖 Executive Summary
This repository houses a **strategic analysis and policy framework** designed to operationalize Incident Response (IR) for cloud-native and hybrid enterprise environments.

The project addresses the critical tension between **strategic governance** (NIST) and **tactical execution** (SANS). It delivers a legally defensible **Security Response Plan (SRP)** that prioritizes forensic integrity, chain of custody, and regulatory compliance (GDPR, SOC 2) without sacrificing speed of remediation.

---

## 📊 Strategic Analysis: NIST vs. SANS
A comparative analysis was conducted to determine the optimal framework for a high-velocity Cloud Service Provider (CSP). The resulting "Hybrid Model" utilizes **NIST for Board-level reporting** and **SANS for SOC-level execution**.

| Feature | **NIST SP 800-61 Rev. 2** | **SANS Institute Framework** | **Strategic Decision** |
| :--- | :--- | :--- | :--- |
| **Phases** | 4 Phases (Preparation, Detection/Analysis, Containment/Eradication/Recovery, Post-Incident) | 6 Phases (Preparation, Identification, Containment, Eradication, Recovery, Lessons Learned) | **Hybrid Approach:** We utilize SANS steps for the technical SOPs to ensure granular tracking, mapped to NIST phases for executive reporting. |
| **Focus** | Governance, Policy, & Coordination | Technical Execution & "Boots on the Ground" | Use SANS for the SOC team; use NIST for the Board of Directors. |
| **Vocabulary** | "Detection & Analysis" combined | "Identification" separate from "Investigation" | SANS methodology was selected to enforce the distinction between *finding* an alert and *verifying* the threat. |
| **Recovery** | Grouped with Containment | Distinct Phase | **Critical:** SANS forces verification that the threat is gone *before* restoring backups, preventing reinfection loops. |

---

## 🛠️ Policy Architecture & Forensic Modernization
This framework modernizes legacy Incident Handling forms (circa 2003) to meet 2025 forensic standards.

### 1. Incident Contact & Escalation Protocol
* **Gap:** Static contact lists fail during the "Golden Hour" of a breach.
* **Solution:** Integration of CISA (2025) guidelines to automate contact retrieval via API (e.g., PagerDuty), ensuring Legal, PR, and Executive stakeholders are engaged within SLAs.

### 2. Identification & Severity Scoring
* **Standard:** NIST SP 800-61r2
* **Enhancement:** Implemented a **Severity Impact Matrix** (Critical/High/Medium/Low) based on business continuity impact rather than just technical indicators.
* **Forensic Trigger:** Captures "Method of Detection" (IDS vs. User Report) to guide initial evidence gathering.

### 3. Containment & Chain of Custody
* **Legal Requirement:** Preserving evidence for potential litigation or insurance claims.
* **Cloud Adaptation:** "Physical Location" fields were deprecated in favor of **Snapshot IDs**, **Container Hashes**, and **VPC Flow Log** pointers.
* **Dwell Time Tracking:** Explicit fields to measure *Time of Detection* vs. *Time of Containment* to track SOC performance KPIs.

### 4. Eradication & Vulnerability Management
* **Process:** Linkage of incidents to specific **CVE Numbers**.
* **Goal:** Ensures that the "Lessons Learned" phase feeds directly into the Vulnerability Management lifecycle to patch the root cause.

---

## 🚀 Project Outcome
* **Deliverable:** A comprehensive Security Response Plan (SRP) and Incident Handling SOP.
* **Compliance:** Achieved 100% alignment with rubric requirements for regulatory adherence.
* **Impact:** Created a reusable template for organizations seeking to mature their SOC from "ad-hoc" firefighting to "defined" processes (CMMI Level 3).

---

## 📂 Repository Contents
* `README.md` - Executive Summary and Strategic Analysis.
* `SANS_vs_NIST_Strategic_Analysis.md` - The Strategic Policy Analysis.
* `Incident_Handling_Forms_Template.md` - Modernized templates for SOC analysts.

---
