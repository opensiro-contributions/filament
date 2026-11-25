# Opt-in external-change adaptation for Filament task graphs

## Proposal in the project's own terms

### What you need

A developer could configure a watcher to assess a future external change and, within an explicitly approved scope, schedule a compatibility evaluation in a designated native chat's task graph. For example, a provider announces an API deprecation date; the watcher chooses whether to defer, do nothing or schedule an evaluation before that date. This is a hypothetical scenario, not a claim of an observed Filament failure.

**What exists today:** Filament's external script/webhook watchers can collect events and wake a run or notify a person. [Event packets](https://github.com/invertibleMatrix/filament/blob/90cf0c20f3fd2d55a73994963427f2fd2532b970/src/app/watchers/packet.js) fence outside data. [Routine validation](https://github.com/invertibleMatrix/filament/blob/90cf0c20f3fd2d55a73994963427f2fd2532b970/src/core/routines.js#L445-L460) currently limits guidance to chat-bound triggers.

**What may be missing:** an explicit opt-in path from an external-event watcher to a bounded future adaptation commitment and its actual disposition in an owner-designated chat graph, rather than merely a message.

**Closest existing project-native solution:** read a watcher's result and ask the graph planner to create a task; use existing guidance where its trigger allows it.

**Existing discussion:** [#2](https://github.com/invertibleMatrix/filament/issues/2) and [#3](https://github.com/invertibleMatrix/filament/issues/3) concern concrete provider compatibility; [#5](https://github.com/invertibleMatrix/filament/issues/5) concerns present worker budgets. Five original Issues open and no PRs at review time. No matching prospective adaptation proposal found within the bounded search, not proof of global novelty.

## How we reached this proposal — Opensiro VSM assessment

OpenSiro studies organizational functions and decision ownership, not product quality, safety or maturity.

**Historical assessment:** [accepted Index assessment](https://github.com/opensiro/vsm-harness-index/blob/7abafd36dd9216d94e795dac9e6030bc0e8e56a6/assessments/fi/filament.md); Index commit 7abafd36dd9216d94e795dac9e6030bc0e8e56a6; assessment blob 57cae90a39420244c4268dd4b64bf3af6648ed0c; reviewed 2026-11-24; original review_ref 90cf0c20f3fd2d55a73994963427f2fd2532b970; Profile 0.2.4; Skills Methodology 0.3.8.

**Boundary:** one native Filament coding chat, task graph and subordinate workers/beside-team; an optional Space watcher serving that chat. Not unrelated projects, external clients or business governance.

**Current original HEAD:** [90cf0c20f3fd2d55a73994963427f2fd2532b970](https://github.com/invertibleMatrix/filament/commit/90cf0c20f3fd2d55a73994963427f2fd2532b970), observed 2026-11-25.

| Key | Organizational function | Historical state | Evidence or limitation |
| --- | --- | --- | --- |
| **S1 · Operations** | Perform work | A | Native agent tool loop |
| **S2 · Coordination** | Prevent inter-worker interference | A | Task graph and overlap/merge feedback |
| **S3 · Current management** | Allocate current work | A(P) | Planner and owner graph controls |
| **S3* · Independent audit** | Check work independently | A | Beside-team findings |
| **S4 · Future adaptation** | Evaluate external/future changes | ? | Watcher composition unresolved |
| **S5 · Identity and policy** | Resolve ultimate policy | — | No local ultimate arbitration established |

States: `A` autonomous decision ownership; `C` supported function-specific construction of autonomous ownership; `P` supported parent-governed S3/S4/S5 mode; `A(P)` and `C(P)` additionally support parent ownership; `—` bounded absence of evidence for a material path after review; `?` unresolved evidence. These are ownership categories, not quality ranks or requirements to implement all six functions.

## Why this particular construction?

**Whole-repository prioritization:** S1, S2, S3 and S3* have established paths; no local S5 redesign is justified. S4 is a bounded hypothesis because external watcher input, owner authorization and the graph already exist but their prospective decision closure is unresolved. Maintainer interest in this S4 design is not established.

**Construction hypothesis:** S4=? -> S4=C. This is a proposed future construction path, not a new Index grade.

**Native building blocks:** [routine constraints](https://github.com/invertibleMatrix/filament/blob/90cf0c20f3fd2d55a73994963427f2fd2532b970/src/core/routines.js#L445-L460), [guidance authorization](https://github.com/invertibleMatrix/filament/blob/90cf0c20f3fd2d55a73994963427f2fd2532b970/src/app/watchers/guidance.js#L130-L145), and [graph apply/keep](https://github.com/invertibleMatrix/filament/blob/90cf0c20f3fd2d55a73994963427f2fd2532b970/src/app/agent/graph-runner.js#L1640-L1667).

**Minimal proposed addition:** optional owner-approved same-Space native-chat target and limited prospective choices, a revision-checked graph commitment or refusal, and durable feedback of its later result.

**Scope exclusions:** no automatic provider switch, secret access, arbitrary cross-chat guidance, policy edits or extra daemon. Preserve existing pause, privacy and permission boundaries. The graph planner still owns scheduling and integration.

## Proposed approach and validation

### How it could work

1. An owner explicitly binds an external-event routine to an eligible native chat and permits a bounded choice: defer, no change, or schedule a compatibility evaluation.
2. A developer-composed autonomous watcher evaluates the dated external evidence, chooses an allowed option and records the reason. The runtime applies the allowed future-work commitment through the native graph path or returns an explicit refusal; it must not silently replace the authorized decision. Link event, decision and graph task so the watcher can observe the receipt and terminal outcome.
3. Future tests should replay the same dated event with different permitted decisions; verify one graph commitment or no-change receipt and returned result. Reject wrong chat, revoked grant, stale revision, pause/archive and replay without unauthorized mutation. Existing watchers must remain unchanged. No tests have been run; use the native npm test/typecheck routes after implementation.

**Hypothesized benefit:** turn prospective external findings into visible, bounded future work without manually relaying each alert into the task graph.

**How to falsify:** if existing supported composition already chooses and commits the same lawful adaptation and returns its actual outcome, reuse it. A message alone, missing decision authority or absent feedback would not establish the proposed construction.

**Cost status:** NOT_MEASURED. Compare matched manual and constructed tasks, including integration, review, testing and maintenance.

## Feedback requested

Does this fit Filament's architecture? Is there an existing supported composition that already closes this path? Would a smaller native integration or no new mechanism be preferable? Corrections to our function mapping are welcome. Maintainers decide adoption; we are not asking Filament to adopt VSM.

## Three independent ways to participate

- Discuss the focused native integration if useful.
- Challenge the interpretation in the open Profile/Skills methodology.
- Explore a different operating boundary in a legally permitted experimental fork without asking Filament to adopt it.

## Research attribution and AI disclosure

[Opensiro Upstream](https://github.com/opensiro/upstream) · [VSM Profile](https://github.com/opensiro/vsm-harness-profile/blob/main/PROFILE.md) · [VSM Skills](https://github.com/opensiro/vsm-harness-skills) · [VSM Index](https://github.com/opensiro/vsm-harness-index)

**AI involvement:** Prepared with AI assistance. No independent human validation, maintainer endorsement, implemented constructor, new assessment grade or measured cost improvement is implied.
