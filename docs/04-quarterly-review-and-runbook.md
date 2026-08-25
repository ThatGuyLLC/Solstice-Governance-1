# 4. Quarterly Review and Runbook

> Part of the [Solstice Governance Repository](../README.md). Protocol rules are fixed by [**FIP-0118**](https://github.com/filecoin-project/FIPs/blob/master/FIPS/fip-0118.md) and referenced throughout.

This section is the runbook for the quarterly review: the community reporting and disclosure duty every Orchestrator must complete each quarter ([§4.1](#41-community-reporting-and-disclosure)), the report **template** to fill ([§4.2](#42-quarterly-report-template)), a worked **example** ([§4.3](#43-example)), and the declaration, verification and escalation process ([§4.4](#44-declaration-verification-and-escalation)). Completed reports are archived in [Section 5, Quarterly Reports](05-quarterly-reports.md).

**Contents**

- [4.1 Community Reporting and Disclosure](#41-community-reporting-and-disclosure)
- [4.2 Quarterly report template](#42-quarterly-report-template)
- [4.3 Example](#43-example)
- [4.4 Declaration, verification and escalation](#44-declaration-verification-and-escalation)

## 4.1 Community Reporting and Disclosure

**Quarterly Community disclosure must be disclosed as per the template in [§4.2](#42-quarterly-report-template); failure to disclose on a quarterly basis may result in Orchestrator Removal.**

Per [§3.1, Policy 9](03-orchestrator-operational-guidelines.md#31-policies): a Quarterly Community Report on claims and reward reception is required; failure to disclose is a removal trigger and forfeits the next quarter's re-admission.

**Procedure (recap):**

1. Public issue in this repository.
2. Response window (7 days).
3. Governance decision (if needed) and archival.

## 4.2 Quarterly report template

> _Placeholder — currently being drafted._ The agreed template will live here. A copy is kept at [`quarterly-reports/_TEMPLATE.md`](quarterly-reports/_TEMPLATE.md) so each quarter's report can be created from it and archived in [Section 5](05-quarterly-reports.md).

## 4.3 Example

> _Placeholder — currently being drafted._ A worked example of a filled quarterly report will go here.

## 4.4 Declaration, verification and escalation

### 4.4.1 Binding declarations and verification

Declarations are accepted by default, and rely upon a mix of on-chain verifiable metrics and other KPIs/SLAs. Verification is dispute-driven: it is triggered only based upon provable gaps highlighted by community members. A false claim surfaces when the legitimate orchestrator's registration and performance cannot be proven via either on-chain transactions or credible probing documentation for off-chain transactions. Verification methods per our integrity guidelines are set out below.

FIP-0118 fixes the consequence of a misreport discovered after binding:

> "There is no retroactive clawback: a misreport discovered after binding is grounds for audit or removal."

### 4.4.2 Dispute resolution for contested bindings

1. The contesting party opens an issue in this repository identifying the pair and its claim.
2. SRA Governance requests evidence of the client relationship from both parties. Acceptable evidence, in increasing strength: business records showing the engagement; client confirmation through a verifiable channel; a signed client attestation (a message signed by the payer wallet naming the orchestrator).
3. Resolution target timeline: 7 days. The outcome (reassignment, removal, or no action) executes on-chain, subject to the hold, and is recorded in the issue.

A contested `CorrectVolume` follows the same evidence process. Per the FIP, bound values are final, so the appeal outcome can only affect later quarters:

> "Binding: whatever each value is when the window closes binds, and bound values are final for the quarter."

### 4.4.3 Verification and removal

Orchestrator verifications are exception-based, per the FIP, and are never pre-clearance. A scheduled audit cycle would rebuild the review pipeline Solstice deprecates. A verification begins only when a trigger fires: a public-data anomaly, a community report filed as an issue, or a contested binding escalated from the dispute process ([4.4.2](#442-dispute-resolution-for-contested-bindings)).

**Grounds for removal:** wash trading, self-dealing (settling volume between parties under common control), misreported FPV (mechanically detectable, since FPV is recomputable from public events), and binding fraud.

### 4.4.4 What triggers a verification

- A public-data anomaly surfaced by the quarterly FPV recomputation or by monitoring (volume spikes at quarter/gate boundaries, figures that clear the target by a hair, volume with no matching storage activity).
- A community report filed as an issue in this repository.
- A contested binding escalated from the dispute process.

### 4.4.5 Escalation

1. **Trigger** → run the relevant on-chain checks (see [§3.2](03-orchestrator-operational-guidelines.md#32-orchestrators-tasks-and-actions)); the recomputation is deterministic and public.
2. **Request evidence** if an anomaly holds: open a public issue and request on- and off-chain evidence; the orchestrator answers within the response window (7 days).
3. **Decide:** reassign a binding, or `Remove(orch)`.
4. All on-chain actions run through the standard registry-change flow under ChangeLogs (see [§2.3](02-solstice-program-governance.md#23-sra-governance-tier--tasks-and-actions)) and are recorded, with rationale, in the issue.

### 4.4.6 Cross-cutting verification measures

- **Reproducibility:** every verification conclusion must be reproducible from public data via the versioned reference indexer; findings cite the events and blocks used.
- **Sanctions cadence:** re-screen registered addresses on a fixed cadence and at each admission, not only on trigger.
- **Conflict attestations:** collect a conflict-of-interest / no-common-control attestation at admission and on any roster or binding change.
- **Verification trail:** triggers, evidence, decisions, and on-chain actions are all logged in this repository.

---

← Previous: [3. Orchestrator Operational Guidelines](03-orchestrator-operational-guidelines.md) · [Back to README](../README.md) · Next: [5. Quarterly Reports](05-quarterly-reports.md) →
