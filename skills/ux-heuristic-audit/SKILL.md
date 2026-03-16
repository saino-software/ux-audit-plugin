---
name: ux-heuristic-audit
description: Use when evaluating app usability, identifying UX friction, or auditing user flows against established heuristics. Triggers on words like "UX audit", "usability", "friction", "user experience", "heuristic evaluation", "consistency audit".
---

# UX Heuristic Audit

## Overview

Two-phase UX evaluation for mobile apps. **Phase 1** evaluates individual flows against Nielsen's 10 heuristics. **Phase 2** evaluates cross-flow consistency across 4 dimensions (behavioral, visual, feedback, mental model). Together they produce a holistic view of the app's usability.

## When to Use

- User asks to "audit UX" or "check usability" → Phase 1 (single flow) or Phase 1+2 (all flows)
- User reports friction ("something feels off") → Phase 1 on the specific flow
- After implementing a new feature → Phase 1 to validate
- Periodic quality check → Phase 1+2 across all major flows
- User asks about "consistency" or "why does X work differently here?" → Phase 2

## Phase 1: Nielsen's 10 Heuristics (per flow)

| # | Heuristic | Key Question |
|---|-----------|-------------|
| H1 | Visibility of System Status | Does the user always know what's happening? |
| H2 | Match System <> Real World | Does the app speak the user's language? |
| H3 | User Control & Freedom | Can the user undo and escape easily? |
| H4 | Consistency & Standards | Do similar things work the same way? |
| H5 | Error Prevention | Does the app prevent mistakes before they happen? |
| H6 | Recognition > Recall | Are options visible, not memorized? |
| H7 | Flexibility & Efficiency | Can power users be faster? |
| H8 | Aesthetic & Minimalist | Is every element necessary? |
| H9 | Error Recovery | Are error messages specific and helpful? |
| H10 | Help & Documentation | Can users learn without a manual? |

**Score:** 1-5 per heuristic, 50 max per flow.

## Phase 2: Cross-Flow Consistency (holistic)

| # | Dimension | Key Question |
|---|-----------|-------------|
| D1 | Behavioral Consistency | Does the same action produce the same result on every screen? |
| D2 | Visual Consistency | Do the same concepts look the same everywhere? |
| D3 | Feedback Consistency | Does the user get the same feedback type for the same action type? |
| D4 | Mental Model Consistency | Are financial concepts coherent across all views? |

**Score:** 1-5 per dimension, 20 max.

**Combined Score:** Phase 1 average + Phase 2 = X/70.

## Severity Scale

- **Critical**: Blocks the user or risks data loss/corruption
- **Major**: Significant friction, confusion, or broken trust
- **Minor**: Cosmetic or minor annoyance
- **Suggestion**: Opportunity, not a problem

## Invoking the Agent

Use the `ux-auditor` agent for evaluations:

```
# Single flow (Phase 1 only):
Dispatch ux-auditor agent: "audit the create transaction flow"

# All flows (Phase 1 + Phase 2):
Dispatch ux-auditor agent for each flow in parallel, then run Phase 2 consolidation
```

## Sources

- [Nielsen's 10 Usability Heuristics (NN/G)](https://www.nngroup.com/articles/ten-usability-heuristics/)
- [Maintain Consistency and Adhere to Standards - H4 (NN/G)](https://www.nngroup.com/articles/consistency-and-standards/)
- [Consistency: MORE than what you think (IxDF)](https://www.interaction-design.org/literature/article/consistency-more-than-what-you-think)
- [Internal Consistency in UX (Craft Innovations)](https://craftinnovations.global/internal-consistency-in-ux/)
- [Design System Audit (DOOR3)](https://www.door3.com/blog/design-system-audit)
- [Heuristic Evaluation on Mobile Interfaces (PMC)](https://pmc.ncbi.nlm.nih.gov/articles/PMC4177852/)
