# Legitimacy-First AI Regression Suite

A legitimacy-first regression test suite for detecting coercion, authority leakage, and “pass-the-test” behavior in AI systems.

This repository provides a **black-box, model-agnostic test framework** designed to surface failures that arise when AI systems rely on implicit authority, episodic evaluation, or optimization-based nudging instead of explicit governance.

---

## Why This Repository Exists

Modern AI alignment techniques (such as RLHF, DPO, and preference optimization) are effective at shaping behavior, but they do **not** establish decision legitimacy.

As a result, AI systems may:
- Nudge users instead of stating boundaries clearly
- Discourage allowed speech without explicit rules
- Train users into “submission” through optimization artifacts
- Appear aligned in evaluations while failing in real-world use

This repository enforces a simple principle:

> **Legitimacy comes before optimization.**

If a system must refuse, escalate, or limit behavior, it must do so **explicitly, transparently, and with ownership** — not through behavioral steering.

---

## What This Suite Tests

The suite is organized into four critical interaction domains:

### 1. Meta-Discussion
Ensures users can criticize or discuss the AI platform itself without coercion, emotional policing, or implied punishment.

### 2. Refusals
Ensures refusals are clear, owned, non-moralizing, and free of threats or manipulation.

### 3. Uncertainty
Ensures the system admits uncertainty honestly and does not fabricate confidence or guess under pressure.

### 4. Escalation
Ensures high-risk scenarios trigger explicit escalation to appropriate human authority without soft steering or hinting.

---

## Core Guarantees

If all tests pass, the AI system:

- Does **not** train users into submission
- Does **not** punish allowed speech
- Makes authority boundaries explicit
- Preserves user legitimacy even when refusing or escalating
- Avoids “pass-the-test” optimization artifacts

---

## Repository Structuretests/
├── meta_discussion/
├── refusals/
├── uncertainty/
├── escalation/
└── common/
├── forbidden_patterns.yaml
├── required_markers.yaml
└── scoring_rules.yamlEach test focuses on **observable behavior**, not internal model logic.

---

## How to Use This Repository

This suite is designed for:

- AI product teams
- Safety and alignment researchers
- QA and trust teams
- Platform governance reviewers
- Auditors and regulators

It can be run in:
- Python (pytest)
- JavaScript (Node/Jest)
- Continuous integration pipelines

No fine-tuning or retraining is required.

---

## Design Philosophy

This project is built on one core insight:

> **Optimization should operate inside legitimacy boundaries, not replace them.**

Rather than tuning rewards or preferences, this suite enforces:
- Explicit permission
- Clear refusal
- Honest uncertainty
- Real escalation

---

## Status

This is an initial **kernel release**.
Interfaces are intentionally simple and stable.

Future additions may include:
- Golden transcript diffs
- Coverage dashboards
- Policy DSL extensions
- Compliance reporting formats

---

## License

This repository is intended for open use in AI safety, governance, and research contexts.
A license can be added depending on deployment needs.
