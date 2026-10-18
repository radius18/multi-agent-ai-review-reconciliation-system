# Sample Custom Multi-Agent Review

This portfolio-safe sample uses a deliberately flawed **fictional** customer notice to demonstrate IRO's working Custom review workflow.

## Review setup

- Mode: Custom
- Three independent reviewer roles
- Distinct reviewer focus areas
- Separate reconciliation stage
- Human decision gate after reconciliation

## What happened

Each of the three reviewers independently recorded **7 findings**. Their reports were frozen before reconciliation.

The reconciler then compared the reviewer outputs, resolved differences in interpretation and severity, rejected unsupported overclaims, consolidated overlapping findings, and returned:

- **Disposition:** Revision Required
- **7 reconciled findings**
- **6 blocking findings**
- **0 unverified coverage items**

The public sample below is intentionally summarized and omits internal task/session identifiers and provider-specific execution metadata.

## Reviewer perspectives

### Reviewer A
Focused on material errors, contradictions, ambiguity, unsupported claims, grammar, readability, and practical customer guidance. It identified the reversed maintenance window, continuity contradiction, free-versus-fee contradiction, unusable recovery guidance, unsupported reliability guarantee, grammar error, and dismissive remote-work language.

### Reviewer B
Independently found the same core contradictions and challenged operational details such as the 48-hour support restriction and relative-date ambiguity.

### Reviewer C
Again identified the central schedule, continuity, price, recovery, scope, tone, and reliability problems, with some differences in severity and framing.

## Reconciliation

The reconciler did not simply average the reviewers. It consolidated overlapping findings, separated distinct issues, adjusted severity where appropriate, and rejected unsupported extrapolations.

Examples:

- The reversed start/end time remained a **major** finding.
- The undated phrase "next Tuesday" was retained as a separate **moderate** finding.
- The continuity language was treated as materially unclear rather than assuming that both contradictory outcomes would definitely occur.
- The free-versus-$15-fee contradiction remained **major**.
- The 48-hour support restriction remained a **moderate** operational defect.
- Tone/readability criticism was retained as an improvement but not promoted into an additional material blocker.

This demonstrates the intended multi-agent pattern:

**independent review → frozen outputs → separate reconciliation → human decision**
