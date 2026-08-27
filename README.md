# Solstice Governance Repository
## 1.1 Purpose

This repository is the operational layer of the governance defined in the Solstice FIP. The FIP fixes what is enforced: the two governance tiers and their powers, the change lifecycle, and the invariants the threat model relies on. This repository holds how those tiers operate: addresses for each governance Safe, the procedures for verification, rotation, disputes, and the parameters designed to iterate without a FIP.

## 1.2 What lives here
### How this document maps to the repository

Each section below is a separate page, ordered by its number, so a reader interested in only one topic can open that page alone. File names carry the section number so they sort in reading order.

| Section | Repository file | Covers |
| :-- | :-- | :-- |
| 1. README | [`README.md`](README.md) | Purpose, references, section map |
| 2. Solstice Program Governance | [`docs/02-solstice-program-governance.md`](docs/02-solstice-program-governance.md) | Governance tiers & Safes · SWA tier · SRA tier (+ Orchestrator Registry) · Parameters · Safety and rotation playbook |
| 3. Orchestrator Operational Guidelines | [`docs/03-orchestrator-operational-guidelines.md`](docs/03-orchestrator-operational-guidelines.md) | Orchestrator guidelines · policies · tasks · monitoring |
| 3.01 Orchestrator Task Checklist | [`docs/03.01-orchestrator-task-checklist.md`](/docs/03.01-orchestrator-task-checklist.md) | Orchestrator checklist · tasks · guidance |
| 4. Quarterly Review and Runbook | [`docs/04-quarterly-review-and-runbook.md`](docs/04-quarterly-review-and-runbook.md) | Quarterly community reporting duty · report template · example · declaration, verification & escalation |
| 5. Quarterly Reports | [`docs/05-quarterly-reports.md`](docs/05-quarterly-reports.md) | Archive/history of filed quarterly reports (one page per report) |
| 6. Program Change Log | [`docs/06-changelog.md`](docs/06-changelog.md) | Rule-change history with community issues & FIP links |

### Contains key documentation including:
- Tasks and actions for each ecosystem actor, inclusive of the operational guidelines for each role, and admission and removal criteria for Orchestrators.
- Measurement-rule declarations for each orchestrator.
- The registry of admitted Orchestrators and the change log of program-rule updates.
- The dispute procedure for contested bindings, and the verification playbook.
- The versioned reference indexer that recomputes FPV from public settlement events.
- The durations of `POST_PERIOD` and `VERIFICATION_WINDOW`.
- The wallet addresses for each tier's Safes.
- Future issue templates, application forms, and workflow automation.

## 1.3 Changing this repository

Changes happen by pull request with public review — covering, but not limited to, merge rights, review windows, and whether any section requires sign-off from both tiers. Every change to the program rules is recorded in the [Program Change Log](docs/06-changelog.md), which links the originating community issue and, where applicable, the resulting FIP.

## 1.4 Reference Links

- FIP text: [FIP-0118](https://github.com/filecoin-project/FIPs/blob/master/FIPS/fip-0118.md)
- Reference indexer: TBD
- Settlement data and dashboards: TBD

---

*Solstice Governance Repository — operational layer of [FIP-0118](https://github.com/filecoin-project/FIPs/blob/master/FIPS/fip-0118.md).*
