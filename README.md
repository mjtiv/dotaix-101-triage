# DotAIX §101 Triage Engine

A deterministic AI execution environment for patent law.

Run §101 eligibility analyses using a fixed evidentiary record and reproducible outputs instead of free-form prompting.

No installation required — drag and drop the `.aix` file directly into ChatGPT.  
The execution model is portable and model-agnostic.

This repo prioritizes correctness, auditability, and repeatability over doctrinal coverage.  
Additional cases and rules can be added incrementally without changing the core execution framework.

---

## Overview

This repository demonstrates a **structured, deterministic approach to 35 U.S.C. §101 patent eligibility analysis**.

Instead of free-form prompting, the system uses a **DotAIX-style closed evidentiary record** (`.aix` file) containing:

- Governing statute
- Core Supreme Court precedent (Mayo, Myriad, Alice)
- Representative Federal Circuit guidance (Enfish, etc.)
- Explicit reasoning instructions

Claims are analyzed **only within that fixed record**, producing:

- Step One (abstract idea / natural law / phenomenon)
- Step Two (inventive concept)
- Short conclusion: *Likely Eligible / Likely Ineligible*
- Concise reasoning bullets grounded in cited doctrine

The goal is **reproducibility and explainability**, not open-ended AI guessing.

---

## Why this exists

Modern LLM outputs drift and hallucinate.

Legal analysis — especially patent eligibility — requires:

- traceable reasoning
- consistent rules
- repeatable outputs

DotAIX introduces:

> deterministic AI execution for legal workflows

Each run:
- uses the same rule set
- the same evidentiary record
- the same reasoning steps

→ producing auditable, stable results.

---

## What this is

✓ A research prototype  
✓ A deterministic §101 triage tool  
✓ A structured memo generator  
✓ A demonstration of controllable AI reasoning  

---

## What this is NOT

✗ Not legal advice  
✗ Not a court outcome predictor  
✗ Not a substitute for attorney review  
✗ Not doctrinally complete  

This tool provides **initial triage only**.

---

## Repository Structure

This repo is intentionally minimal.

Each PDF is a full execution transcript showing:
input claim → DotAIX (.aix) rule file → structured eligibility memo.

Claim_101_Analysis_V2.aix.txt – deterministic execution script

-001_*.pdf – positive control (eligible)
-002_*.pdf – ineligible example (statistical analysis)
-003_*.pdf – ineligible example (data classification)
-004_*.pdf – complex edge case (beta limitation)

Together these act as a small regression suite demonstrating reproducible input → output behavior.

--

## Included Test Suite (Deterministic Regression Runs)

| ID  | Category | Expected Result | Purpose |
|-----|-----------|----------------|-----------|
| 001 | Structural / architecture improvement | Likely Eligible | Positive control – verifies Enfish-style computer functionality improvements pass |
| 002 | Statistical / financial analytics | Likely Ineligible | Math + generic computation should fail |
| 003 | Data classification / identifier matching | Likely Ineligible | Information processing without technical improvement should fail |
| 004 | Rule-based animation automation | Edge case (beta) | Complex software rules case used to expose doctrine gaps and guide future rule expansion |

Reference cases include: Enfish (eligible), SAP/InvestPic (ineligible), Intellectual Ventures v. Symantec (ineligible), and McRO (edge/complex rules automation).

---

## ⚠️ Beta Status

This project is **early-stage / beta**.

Important:

- Doctrine coverage is intentionally minimal
- Only a small set of controlling cases are encoded
- Some complex claims (e.g., McRO-style rule-based automation) may be classified conservatively
- Outputs use **“Likely”** language, not definitive determinations

Misclassifications are treated as:

> signals to extend the rule set

The system is designed to be **incrementally extensible**, not perfect on day one.

---

## Design Philosophy

DotAIX follows three principles:

### 1. Closed Record
No external browsing or hidden knowledge.
Only the provided legal materials may be used.

### 2. Deterministic Reasoning
Same input → same output.

### 3. Explainability
Every conclusion must cite specific doctrinal logic.

---

## How to Run (ChatGPT Workflow)

This project is designed to run directly inside ChatGPT using the DotAIX execution file.

### Steps

1. Drag and drop:
   aix/Claim_101_Analysis_V2.aix.txt
   into ChatGPT.

2. Type:
   read file as txt and prompt me for a claim to analyze when done

3. Wait for the model to confirm the file has been fully read.

4. Paste the full text of ONE patent claim.

5. The model will output a structured §101 eligibility memo:
   - Step One analysis
   - Step Two analysis
   - Conclusion (Likely Eligible / Likely Ineligible)
   - Short reasoning bullets grounded only in the included cases

6. Save the output into /outputs for reproducibility.

---

## License

MIT License — provided for research and demonstration purposes.

---

## Disclaimer

This repository is for educational and research purposes only.
It does not provide legal advice and should not be relied upon for legal decisions.

Consult qualified counsel for any real-world matters.

---

## Roadmap

- Add additional edge cases (McRO, DDR, Finjan)
- Add “Borderline / Needs Review” category
- Improve rule coverage
- Build packaged CLI runner
- Expand DotAIX execution framework

---

## DotAIX

This repo is an early demonstration of the broader **DotAIX concept**:
> structured, deterministic execution environments for AI systems

The same approach can be extended beyond law into:
- compliance
- auditing
- regulated workflows
- safety-critical AI

---

## Contact

Open an issue or reach out via GitHub.

Feedback and edge cases welcome.

M. Joseph Tomlinson IV
mjtiv@udel.edu























