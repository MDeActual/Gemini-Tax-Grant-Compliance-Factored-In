# READ THIS FIRST

## Objective

Ship a credible MVP in the next few hours for:

- tax and grant compliance intake
- secure-score telemetry review
- compliance penalty and security-gap surfacing
- executive-level operating ownership after launch

## Constraint

The repository snapshot did not include the referenced attachment, so this package uses the canonical source text preserved in `SOURCE_BRIEF.md` as the working source of truth.

## Assumption-Dependent Sections

Revisit these sections once the missing attachment is available, because they are the most assumption-sensitive parts of this package:

- the exact MVP scope in `Recommended MVP`
- executive role coverage in `AI Swarm Structure`
- release criteria in `Non-Negotiable Rules`
- launch sequencing in `Production-in-Hours Launch Sequence`

## Recommended MVP

Build only the shortest production path:

1. Intake business, grant, tax, and telemetry inputs
2. Normalize them into a single `case_record`
3. Run parallel executive-agent analysis
4. Aggregate findings through one orchestrator
5. Produce:
   - compliance risk summary
   - security-gap summary
   - likely penalty exposure
   - grant-readiness checklist
   - executive action plan

## DevOS Operating Model

Use DevOS as the control plane for:

- workflow routing
- role isolation
- approval gates
- task retries
- artifact logging
- production runbooks

The orchestrator is the only component allowed to:

- open or close workstreams
- assign work to executive agents
- merge parallel outputs
- trigger escalation
- mark deliverables production-ready

## AI Swarm Structure

The swarm should run in parallel under one orchestrator with these minimum executive roles:

Use the matrix below as the primary role contract for the MVP startup package.

Role | Department | Build Responsibility | Operating Responsibility
--- | --- | --- | ---
CEO / Chief of Staff Orchestrator | Executive Office | sets priorities, sequencing, and approvals | runs cadence, decisions, and escalations
CTO | Product + Engineering | builds MVP architecture, integrations, and delivery plan | owns engineering backlog and uptime
COO | Operations | defines workflows, SLAs, and execution lanes | manages operations and service quality
CFO | Finance | models cost, unit economics, and grant-use controls | owns budgets, burn, and financial controls
Chief Compliance Officer | Compliance | defines rules, evidence, and filing controls | manages audits, exceptions, and policy upkeep
CISO | Security | defines telemetry review, control checks, and risk thresholds | manages risk register and security incidents
CLO / General Counsel | Legal | reviews regulatory language, disclaimers, and exposure | manages legal review and policy changes
CRO / Revenue Lead | Growth | defines ICP, pipeline, and offer packaging | manages go-to-market execution

Role checklist fallback:

- CEO / Chief of Staff Orchestrator — Executive Office — builds priorities and approvals; manages cadence and escalations
- CTO — Product + Engineering — builds architecture and integrations; manages uptime and backlog
- COO — Operations — builds workflows and SLAs; manages service quality
- CFO — Finance — builds cost controls and budget guardrails; manages burn and reporting
- Chief Compliance Officer — Compliance — builds evidence and filing controls; manages audits and exceptions
- CISO — Security — builds telemetry mapping and severity thresholds; manages incidents and the risk register
- CLO / General Counsel — Legal — builds legal language and review checklists; manages policy change workflow
- CRO / Revenue Lead — Growth — builds offer packaging and onboarding flow; manages pipeline and adoption

## Parallel Work Pattern

### Wave 1 — Foundations

Run in parallel:

- CTO: system design and delivery architecture
- COO: operating workflow and handoff design
- CFO: MVP budget and deployment cost guardrails
- Chief Compliance Officer: compliance evidence checklist
- CISO: telemetry-to-risk mapping

### Wave 2 — Market + Risk

Run in parallel:

- CLO: legal disclaimers, terms, and exposure review
- CRO: offer framing, onboarding flow, and first-customer path
- CTO + CISO: production hardening checklist

### Wave 3 — Launch Gate

The orchestrator merges all outputs and blocks launch unless:

- MVP scope is frozen
- minimum compliance evidence exists
- telemetry ingestion is working
- risk severity thresholds are defined
- executive ownership is assigned by department

## Non-Negotiable Rules

1. Every department owner must both build and later manage their department lane.
2. No agent may overwrite another agent's approved artifact without orchestrator approval.
3. Compliance, legal, and security findings must be attached to every launch decision.
4. The CFO and COO must approve production budget and operating capacity before go-live.
5. The CISO and Chief Compliance Officer must sign off on critical-risk handling rules.
6. The orchestrator must maintain a single decision log and action queue.
7. Any missing evidence defaults to "not ready" rather than assumed compliance.

## Production-in-Hours Launch Sequence

### Hour 0-1

- finalize MVP scope
- confirm data inputs
- define risk severity bands
- assign executive agent owners

### Hour 1-2

- stand up DevOS orchestrator
- connect telemetry and intake sources
- create shared artifact store
- run first parallel executive pass

### Hour 2-3

- reconcile conflicts across finance, compliance, legal, and security
- freeze report template
- verify alert thresholds and escalation flow

### Hour 3-4

- perform smoke run with one real customer scenario
- fix blocker-level issues only
- launch with human approval gates still enabled

## First Production Deliverables

- intake checklist
- risk-scoring rubric
- grant-readiness report template
- compliance evidence checklist
- executive action dashboard
- incident and escalation runbook

## What To Do Next

1. Use `devos.yaml` as the initial operating template.
2. Use `agents.md` as the role contract for the swarm.
3. Keep the first release human-in-the-loop for legal, compliance, and security approvals.
4. Replace assumptions with the missing attachment details as soon as that file is available.
