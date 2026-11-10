# Healthcare Generative AI Use-Case Risk Assessment

## Overview

This project assesses the privacy, security and governance risks of a fictional Generative AI solution designed to summarize medical records for healthcare professionals.

The assessment examines whether the solution should be approved, approved with conditions, deferred or rejected.

> This project is based entirely on a fictional scenario and synthetic information. It does not contain real patient data or confidential company information.

## Business Context

A fictional healthcare organization plans to deploy a Generative AI assistant to summarize medical reports.

The proposed workflow is:

1. An authorized healthcare professional uploads a medical report.
2. The document is processed by a Generative AI service.
3. The AI generates a preliminary summary.
4. A qualified healthcare professional reviews and corrects the output.
5. The validated summary is added to the patient's medical record.

## Assessment Objectives

The project aims to:

- Identify the personal and sensitive data processed by the solution.
- Map the main data flows and third-party dependencies.
- Assess privacy, cybersecurity and operational risks.
- Analyze hallucination, prompt injection and data leakage risks.
- Evaluate human oversight and access-control requirements.
- Review relevant GDPR and EU AI Act considerations.
- Apply the NIST AI Risk Management Framework.
- Produce an executive risk-based deployment decision.

## Frameworks

- NIST AI Risk Management Framework
- NIST AI 600-1 Generative AI Profile
- General Data Protection Regulation
- European Union Artificial Intelligence Act
- Privacy by Design and Security by Design principles

## Key Risk Areas

The assessment covers:

- Sensitive health data exposure
- Unauthorized access
- Excessive data retention
- Third-party and supply-chain risks
- Hallucinations and inaccurate medical summaries
- Prompt injection
- Model and output manipulation
- Insufficient human oversight
- Bias and incomplete summaries
- Service availability
- Uncontrolled model updates
- Lack of traceability and auditability

## Planned Deliverables

- AI Use-Case Inventory
- Stakeholder and Responsibility Map
- Healthcare Data Inventory
- Data-Flow Diagram
- AI Risk Register
- Risk Matrix
- GDPR Assessment
- EU AI Act Screening
- NIST AI RMF Mapping
- Executive Decision Memo

## Preliminary Decision

The fictional use case will be evaluated against four possible decisions:

- Approve
- Approve with conditions
- Defer
- Reject

The final decision will be documented after the risk assessment and control evaluation are completed.

## Repository Structure

```text
healthcare-ai-use-case-risk-assessment/
├── README.md
├── use-case/
├── data-flow/
├── risk-assessment/
├── compliance/
├── decision-memo/
└── references/
