# Boundary Governance — Why AI Governance Fails to Function  
**Not a Gap, but a Missing Intermediate Layer**

Author: Dosanko | AI and Human Decision Design | Boundary Governance  
Note: This article is the official technical note for Boundary Governance and Decision‑space Rationale Identifiers.  
For context about sources referenced during research, see the References section below.

---

## Abstract
AI governance does not fail because organizations lack discipline or process maturity.  
It fails because the prevailing two‑layer model — principles above, operations below — is structurally incapable of producing governance‑grade rationale under conditions of regulatory pressure and asynchronous governance rhythms.

This article formalizes **Boundary Governance**, an architectural intermediate layer that defines decision spaces, structures rationale, synchronizes governance rhythms, and enables the exercise of accountability.

The argument is architectural, not procedural:  
governance must be designed as a system of constraints, interfaces, and decision coordinates, not as a sequence of steps.

---

## 1. Why AI Governance Fails (Reframed)
Organizations often misdiagnose AI governance failure as an “implementation gap.”  
They assume that more checklists, more oversight, or more maturity will close the distance between principles and practice.

**This is incorrect.**

The real issue is structural: **the architecture lacks an intermediate layer.**

### Governance‑grade rationale（formal definition）
Rationale sufficient to satisfy regulatory accountability requirements, including:

- traceability to predefined value criteria  
- decision boundaries  
- escalation conditions  
- organizational authority under which the decision was made  

Explainability techniques (SHAP, LIME, counterfactuals) provide partial interpretability,  
but **they do not produce governance‑grade rationale** without the intermediate layer.

### Why traditional IT governance worked
Because:

- system speeds matched governance rhythms  
- humans remained the decision‑makers  
- regulators demanded process evidence, not decision justification  

AI breaks all three simultaneously.

---

## 2. Governance Rhythms, Not Speed
Governance operates on asynchronous rhythms:

- Principles layer: **years**  
- Operational governance: **months–weeks**  
- AI decision outputs: **milliseconds**

Other high‑speed domains succeed because rhythms are synchronized through architecture.

Procedural refinement cannot compensate;  
when procedural controls are automated, they become **architectural**.

---

## 3. The Missing Intermediate Layer (Boundary Governance)
Boundary Governance transforms principles into operational constraints and enables accountability.

It has **design‑time**, **runtime**, and **interface** responsibilities.

---

### 3.1 Design‑Time Responsibilities

#### (1) Decision‑Space Definition
Defines:

- value criteria  
- trade‑off boundaries  
- permissible decision regions  
- fairness thresholds  
- escalation triggers  

#### (2) Rationale Identifier Schema
Each AI output is tagged with:

- fairness‑space ID  
- risk‑space ID  
- trade‑off configuration ID  
- escalation‑condition ID  
- decision‑owner ID  

This schema is the **minimal evidential unit** for governance‑grade rationale.

---

### 3.2 Runtime Responsibilities

#### (3) Drift and Distribution‑Shift Monitoring
Detects divergence from the predefined decision space.

#### (4) Exception and Boundary Routing
When a boundary is crossed:

- system halts or re‑routes  
- identifies responsible human  
- records rationale identifier  
- triggers escalation  

Drift monitoring is one of the triggers for exception routing.

---

### 3.3 Interfaces and Change Propagation

#### Upstream Inputs
- Regulatory requirements  
- Organizational values  
- Risk appetite  
- Fairness constraints  
- Sustainability expectations  

#### Downstream Outputs
- Decision‑space configurations  
- Rationale identifiers  
- Escalation rules  
- Monitoring parameters  
- Audit‑ready evidence structures  

#### Change‑Propagation Protocol
When upstream inputs change, the layer:

- records the change  
- evaluates affected artifacts  
- issues updated configurations or deprecation notices  

Change events are auditable.

#### Integration with Model Pipeline
The layer prescribes interface requirements, not API contracts.  
It can operate:

- pre‑inference（feature gating）  
- post‑inference（rationale tagging）  
- inline wrapper  

Robust deployments combine pre‑ and post‑inference roles.

---

## 4. Worked Example 1: Credit Scoring
(EU AI Act Articles 9, 11, 14; Article 43; CSRD; ESRS‑S1, ESRS‑G1)

### Without the intermediate layer
- Risk management becomes checklist‑driven  
- Documentation lacks rationale  
- Oversight cannot be justified  
- Conformity assessment fails  
- Double materiality cannot be demonstrated  

### With the intermediate layer
**Decision Space**

- Disparity ratio ≤ 1.25  
- Approval‑rate delta ≤ 8%  
- PD ≤ 0.12  
- Escalation when disparity > 1.25  

**Identifier Schema**  
fairness‑space ID / risk‑space ID / trade‑off config ID / escalation‑condition ID / decision‑owner ID

**Double Materiality Path**

- Impact on individuals: fairness constraints  
- Impact from external constraints: regulatory boundaries  

---

## 5. Worked Example 2: HR Recommendation Systems
(Equality Directives; ESRS‑S1)

### Without the intermediate layer
- Bias mitigation is ad‑hoc  
- Protected‑attribute correlations discovered post‑hoc  
- Oversight inconsistent  
- ESRS‑S1 disclosures lack structure  

### With the intermediate layer
**Decision Space**

- Adverse impact ratio ≤ 1.10  
- Protected‑attribute correlation ≤ 0.15  
- Escalation when correlation > 0.15 and performance delta < 5%  

**Identifier Schema**  
fairness‑space ID / correlation‑monitor ID / trade‑off config ID / escalation‑case ID / decision‑owner ID

---

## 6. Worked Example 3: Generative AI Advisory Chatbot
**Decision‑Space Parameters**

- Intent envelopes: product info, billing support  
- Safety constraints: no unverified financial projections  
- Provenance: every claim must carry a source token  

**Runtime Behavior**  
If chatbot attempts legal advice → safety‑constraint ID triggers suppression and routes to human.

---

## 7. Positioning Within Scholarship
Boundary Governance aligns with and extends:

- **Floridi** — Levels of Abstraction, Ethical Infrastructure  
- **Mittelstadt** — Principles fail structurally  
- **Morley** — Operationalization typology  
- **NIST AI RMF** — Complementary  
- **IEEE 7000** — Runtime persistence  
- **Selbst** — Abstraction traps  
- **OECD AI Principles** — Accountability & transparency  

---

## 8. Architectural vs Procedural Governance
Procedural governance = sequences  
Architectural governance = constraints・interfaces・structural guarantees

Mapping to TOGAF:

- Architecture building blocks → decision spaces  
- Data entities → rationale schemas  
- Architecture continuum → intermediate layer  
- ADM lifecycle → evolution of decision‑space artifacts  

---

## 9. Organizational Ownership and Failure Modes
Three models:

1. **AI Governance Architecture Office**  
   - Failure: bottlenecks  

2. **Risk Architecture Function**  
   - Failure: insufficient technical integration  

3. **Hybrid Model**  
   - Failure: coordination overhead  

---

## 10. Implementation Prerequisites
Technical:

- metadata tagging  
- semantic drift detection  
- evidence store  

Organizational:

- architectural authority  
- cross‑functional alignment  

Boundary Governance is additive to model risk management (e.g., SR 11‑7).

---

## 11. Limitations and Theoretical Assumptions
Limitations:

- emergent decision contexts  
- agentic/self‑modifying systems  
- organizations lacking architectural authority  

Assumption:  
value criteria and trade‑off boundaries can be formalized ex ante.

---

## 12. Methodology Note
Conceptual design contribution grounded in:

- comparative policy analysis  
- design‑science reasoning  

Future work: empirical pilots and evaluation.

---

## 13. Conclusion and Next Steps
AI governance fails because the architecture is incomplete.  
Boundary Governance formalizes the missing layer.

Next steps:

- implementation pilots  
- standardization of identifier schemas  
- empirical evaluation  

---

## References
(Your reference list here — unchanged)
