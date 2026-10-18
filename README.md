# Multi-Agent AI Review & Reconciliation System

**Independent Review Orchestrator (IRO)** is an ongoing multi-agent AI review system for coordinating independent reviewers, evidence-based reconciliation, durable review state, and protected human decision gates.

**Status:** Work in progress · September 2026–Present

## Why Multi-Agent

IRO is designed around a simple rule: independent reviewers should not influence one another before their work is complete.

A typical workflow is:

**artifact → isolated reviewers → frozen reviewer outputs → separate reconciler → human decision**

Different reviewer agents can receive different review focuses while evaluating the same artifact. Their outputs are preserved before a separate reconciler compares agreements, conflicts, omissions, severity, and supporting evidence.

## Operator Workspace

![IRO operator workspace](Screenshot%202026-10-17%20195441.png)

*Desktop workspace for review intake, document inspection, review modes, findings/progress, outputs, and persistent operator interaction.*

## Working Custom Review Mode

Custom mode is operational and still being expanded. It supports selectable reviewer roles, role-specific focus, reconciliation behavior, reconciler selection/focus, reporting options, reviewer limits, plan preview/validation, and real review dispatch.

![Custom multi-agent configuration](Screenshot%202026-10-17%20211025.png)

*Custom review configuration with separate reviewer roles and distinct evaluation focuses before reconciliation.*

![Validated Custom ReviewPlan](Screenshot%202026-10-17%20211122.png)

*Validated Custom plan preview before dispatch, including reviewer/reconciliation settings, review focus, reporting options, and bounded execution settings.*

## Real Multi-Agent Test

The current portfolio sample uses a deliberately flawed fictional internet-service notice.

![Completed multi-agent review with operator interaction](Screenshot%202026-10-17%20234634.png)

*Completed Custom-mode run showing independent reviewer reports side-by-side, all reviewer stages complete, reconciliation complete, the workflow stopped at the human decision gate, and Operator Chat being used to locate the reconciler output.*

In the completed run:

- three reviewer roles each recorded **7 findings**;
- reviewer outputs were preserved before reconciliation;
- the reconciler returned **Revision Required**;
- **7 reconciled findings** remained;
- **6 were blocking**;
- the workflow stopped for a human decision rather than approving or publishing automatically.

See the portfolio-safe sample: [sample/README.md](sample/README.md).

### Generated review outputs

![Reviewer and reconciliation output folder](Screenshot%202026-10-17%20234656.png)

*Generated output folder for the sample run, preserving separate reviewer reports and reconciliation artifacts rather than collapsing the review into one opaque response.*

## Operator Chat

IRO includes a persistent operator chat for general assistance and interaction with the application. The chat is intentionally separate from reviewer and reconciler execution so normal operator conversation does not silently contaminate isolated review sessions or mutate an active review.

The current implementation uses a provider-adapter seam rather than making the core workflow depend on one model/provider. Additional provider adapters remain part of the roadmap.

## Review Scope & Extensibility

The public sample demonstrates document review, but IRO is not limited to customer-facing prose. Existing project workflows also include **code-aware software review**, architecture/contract review, closure retesting, and evidence-based QA.

The core is being shaped around review artifacts/packages rather than one file format, which supports future reuse from other applications without copying the orchestration engine.

## QA, Provenance & Human Control

The system preserves review plans, reviewer outputs, reconciliation results, run state, hashes/provenance, recovery information, and human-readable reports.

Current design priorities include:

- reviewer independence and focus isolation;
- deterministic review-plan construction;
- fail-closed validation at policy/authority boundaries;
- reconciliation that can accept, merge, modify, downgrade, or reject reviewer findings;
- explicit PASS / FAIL / UNVERIFIED handling;
- preserved evidence and human-readable reports;
- human approval remaining separate from automated review.

## Sample Files

- [Fictional customer notice](sample/IRO_Custom_Review_Test_Internet_Notice.txt)
- [Sample workflow and reviewer comparison](sample/README.md)
- [Reconciled sample result](sample/Reconciled_Result.md)

## Skills Demonstrated

- Multi-agent orchestration
- AI evaluation and review design
- Quality Assurance / UAT
- Reviewer isolation and reconciliation
- Requirements and policy boundaries
- Python-based workflow design
- Provenance and evidence preservation
- State / lifecycle design
- Technical documentation
- Human-in-the-loop decision controls

## Portfolio Scope

This public repository is a portfolio presentation rather than the complete private IRO codebase or run archive. Screenshots and sample artifacts demonstrate the working system while internal execution records, private configuration, and machine-specific details remain outside the public repository.
