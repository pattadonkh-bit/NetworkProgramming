---
name: qnet
description: >
  Use this skill for ANY task related to the Q-Net quantum networking project
  (CP352005, Khon Kaen University). Triggers include: writing or updating
  Research.md files for any sprint, updating Sprint_Plan.md, writing or editing
  README/CITATION/CONTRIBUTING files, answering questions about experimental
  results or fidelity numbers, explaining the Q-Net architecture, summarizing
  peer review comments or rebuttal responses, generating Colab summary cells,
  or any documentation/code task that references Q-Net, IBM Quantum, quantum
  teleportation fidelity, or the team members. Always use this skill when the
  user mentions sprint alpha/beta/gamma/delta, ibm_torino/fez/marrakesh, or
  any Q-Net component such as Collapse Modulation, Q-CAST, QTCP, or Phononic Memory.
---

# Q-Net Project Skill

Complete knowledge base for the Q-Net quantum entanglement networking project.
Use this skill to answer questions, write documentation, generate code, or
assist with any task related to the project.

---

## Project Identity

| Field | Value |
|-------|-------|
| Project | Q-Net: Quantum Entanglement-Based Post-Internet Architecture |
| Course | CP352005 Computer Networks |
| Institution | College of Computing, Khon Kaen University |
| DOI | `10.5281/zenodo.19065067` |
| GitHub | `https://github.com/ms584/Q-Net` |
| Colab | `https://colab.research.google.com/drive/1zXrPBkwNGIn2XLGjwUW_jj5L3ldmKCGr` |
| Submission | March 17, 2026 |

### Team

| Role | Name | Nickname | Student ID |
|------|------|---------|-----------|
| Product Owner / Strategist ⭐ | Sitthichok Moknak | บูบู้ | 673380428-6 |
| Quantum Architect | Pattadon Khumnan | โบร์ท | 673380416-3 |
| Software Engineer | Nattaphat Chamtakhu | อ้น | 673380583-4 |
| Network Analyst | Sorawit Sukongchareun | โอ่ง | 673380606-8 |
| Research & Ethics Analyst | Amonwan Phimphichai | เนย | 673380608-4 |

---

## Experimental Results (Ground Truth)

**Always use these exact numbers — never approximate differently.**

### Sprint Summary

| Sprint | Version | Mean Fidelity | Key Innovation | Outcome |
|--------|---------|-------------|---------------|---------|
| Alpha (S1) | v1 | ~49.1% | Real-time feed-forward | ❌ NISQ incompatible |
| Beta (S2) | v2 | ~93.0% | Post-processing correction | ✅ +44 pp |
| Gamma (S3) | v2b | ~49.6% | Readout error mitigation | ❌ FAILED |
| Gamma (S3) | v3 | ~96.6% | Hardware-aware transpilation | ✅ +3.6 pp |
| Delta (S4) | v3 | ~98.0% | ibm_marrakesh + v3 | ✅ Peak 99.09% |

### Peak Result
- **Attempt 29, ibm_marrakesh, v3: 99.09%**
- 95% CI: [98.96%, 99.22%]

### Key Statistical Tests
- Sprint 1 vs Sprint 4: z > 100, p < 0.0001
- Sprint 2 vs Sprint 4: z ≈ 29.8, p < 0.0001

### Backend Comparison (v3 only — version controlled)
| Backend | Qubits | Processor | Mean (v3) | Peak |
|---------|--------|-----------|----------|------|
| ibm_marrakesh | 156 | Heron r1 | ~98.00% | 99.09% |
| ibm_fez | 156 | Heron r1 | ~96.60% | 97.90% |
| ibm_torino | 133 | Heron r1 | 92.83% | 92.83% |

### Sprint 3 Failure (v2b) — Scientific Finding
- **κ(M) ≈ 47.3** — shot noise amplified 47× under matrix inversion
- **Drift: ~8–12%** over 2.1-hour calibration-to-experiment window
- **Recommendation:** Use Probabilistic Error Cancellation (PEC) instead

---

## Experimental Environment

| Parameter | Value |
|-----------|-------|
| Qiskit | 1.0.2 |
| qiskit-ibm-runtime | 0.20.0 |
| Shots | up to 20,000 |
| optimization_level | 3 (v3 experiments) |
| ibm_fez layout | [q0→0, q1→1, q2→2] |
| ibm_marrakesh layout | [q0→0, q1→3, q2→4] |

---

## Q-Net Architecture

### 5-Layer Protocol Stack
| Layer | Name | Function | Technology |
|-------|------|---------|-----------|
| L5 | Application | Reality API | Neural-Qubit Interface |
| L4 | Transport | State Consistency | QTCP |
| L3 | Network | Cognitive Routing | Q-CAST |
| L2 | Link | Reality Link / Collapse Modulation | Bell State Measurement |
| L1 | Physical | Entanglement Fabric | Phononic Memory / Satellites |

### Key Definitions
- **Collapse Modulation:** Layer-2 protocol abstraction — NOT a novel quantum effect.
  Defines: (1) timing protocol, (2) metadata encoding, (3) L1/L3 interface spec
- **Q-CAST:** Fidelity-aware routing using entanglement freshness metric
- **QTCP:** Guarantees fidelity (not data integrity) — no ACK/NACK
- **Phononic Memory:** Crystalline acoustic storage for entangled qubits (speculative)

---

## Critical Scientific Facts

### No-Communication Theorem (ALWAYS enforce this)
> Q-Net does NOT achieve faster-than-light communication.
> Both entanglement pre-distribution and classical correction channels are bounded by c.
> Q-Net's advantage = elimination of connection-establishment overhead (SYN/SYN-ACK/ACK)
> = saving 6–44 minutes per session in Earth–Mars scenarios.

If any document says "zero-latency" or implies FTL → correct it immediately.

### DTN/Bundle Protocol
Q-Net complements (not replaces) NASA's DTN/RFC 9171:
1. Security via no-cloning theorem
2. Reduced per-session setup latency

### Known Limitations (always include in documentation)
- 3-qubit scale only — not production-ready
- Single-hop only — multi-hop fidelity degrades as F₁ × F₂
- No planetary-scale entanglement distribution demonstrated
- Phononic Memory speculative

---

## Peer Review Summary

### Decision: Major Revision Required (3 reviewers)

| Comment | Severity | Status | Resolution |
|---------|---------|--------|-----------|
| R1.M1 — FTL/No-Comm Theorem | Critical | ✅ | Removed all "zero-latency" |
| R1.M2 — Collapse Modulation undefined | Major | ✅ | Added formal protocol spec |
| R1.M3 — No statistical analysis | Major | ✅ | Added 95% CI + z-test |
| R1.m1 — Kardashev informal | Minor | ✅ | Reframed as speculative |
| R1.m2 — Ref [3] unverifiable | Minor | ✅ | Replaced with 2 verified refs |
| R1.m3 — No circuit diagrams | Minor | ✅ | Added Figures 1–3 |
| R2.M1 — Sprint 3 analysis thin | Critical | ✅ | Added κ(M), drift, PEC rec |
| R2.M2 — Backend comparison confounded | Major | ✅ | Separated by code version |
| R2.M3 — Reproducibility missing | Major | ✅ | Added Appendix A |
| R3.M1 — Layer model ≈ Wehner et al. | Major | ✅ | Added Table 1b comparison |
| R3.M2 — Ignores DTN/Bundle Protocol | Major | ✅ | Added to Sec 2.1 |
| R3.m2 — No Limitations section | Minor | ✅ | Added Section 7 |

---

## Writing Guidelines

### Research.md Structure (per sprint)
Each Research.md should contain:
1. Previous sprint review (results table + root cause)
2. Current sprint objectives + checklist
3. Technical approach (code snippets)
4. Expected results
5. References (10 papers, categorized)
6. Failure mode documentation (if applicable)
7. Next sprint plan

### Language
- Bilingual (EN + TH) for all Research.md and Sprint_Plan.md
- English only for README, CITATION.cff, CONTRIBUTING.md
- Thai comments acceptable in Python code

### Tone
- Academic but accessible
- Honest about failures (Sprint 3 v2b is a feature, not a bug)
- Always cite specific numbers (not "high fidelity" — say "97–99%")

---

## Repository Files

| File | Location | Description |
|------|---------|-------------|
| README.md | root | Full project overview with all 34 attempts |
| LICENSE | root | MIT License |
| CITATION.cff | root | Zenodo DOI + authors |
| CONTRIBUTING.md | root | How to contribute + new backend template |
| Sprint_Plan.md | docs/ | All 4 sprints — backlog, results, lessons |
| Research.md | sprint-alpha/ | Sprint 1 notes |
| Research.md | sprint-beta/ | Sprint 2 notes |
| Research.md | sprint-gamma/ | Sprint 3 notes (incl. v2b failure) |
| Research.md | sprint-delta/ | Sprint 4 notes + paper plan |

---

## Zenodo Record

| Field | Value |
|-------|-------|
| DOI | `10.5281/zenodo.19065067` |
| License | CC BY 4.0 (Zenodo) / MIT (GitHub) |
| Version | 1.0.0 |
| Date | 2026-03-17 |
| Status | Published (permanent, cannot delete) |

---

## Quick Reference: 95% CI Formula

```python
import numpy as np
p = success_rate / 100
se = np.sqrt(p * (1 - p) / shots)
ci_low  = (p - 1.96 * se) * 100
ci_high = (p + 1.96 * se) * 100
# Example: p=0.9909, n=20000 → CI=[98.96%, 99.22%]
```

## Quick Reference: Post-Processing Correction

```python
# v2/v3 correction logic
b_corr = b ^ a1 ^ a2   # XOR of bob's bit and alice's two measurement bits
# if payload was |1⟩, b_corr == 1 means success
```