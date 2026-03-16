---
name: ux-heuristic-audit
description: Use when evaluating app usability, identifying UX friction, or auditing user flows against established heuristics. Triggers on words like "UX audit", "usability", "friction", "user experience", "heuristic evaluation".
---

# UX Heuristic Audit

## Overview

Structured UX evaluation using Nielsen's 10 Usability Heuristics, adapted for mobile finance apps. Produces actionable findings with severity, location, and fix recommendations.

## When to Use

- User asks to "audit UX" or "check usability"
- User reports friction ("something feels off", "this is confusing")
- After implementing a new feature — validate the UX before shipping
- Periodic quality check on existing flows

## The 10 Heuristics (Quick Reference)

| # | Heuristic | Key Question |
|---|-----------|-------------|
| H1 | Visibility of System Status | Does the user always know what's happening? |
| H2 | Match System ↔ Real World | Does the app speak the user's language? |
| H3 | User Control & Freedom | Can the user undo and escape easily? |
| H4 | Consistency & Standards | Do similar things work the same way? |
| H5 | Error Prevention | Does the app prevent mistakes before they happen? |
| H6 | Recognition > Recall | Are options visible, not memorized? |
| H7 | Flexibility & Efficiency | Can power users be faster? |
| H8 | Aesthetic & Minimalist | Is every element necessary? |
| H9 | Error Recovery | Are error messages specific and helpful? |
| H10 | Help & Documentation | Can users learn without a manual? |

## Severity Scale

- **Critical**: Blocks the user or risks data loss
- **Major**: Significant friction or confusion
- **Minor**: Cosmetic or minor annoyance
- **Suggestion**: Opportunity, not a problem

## Audit Process

1. Identify the flow to audit
2. Read ALL source code involved (screens, ViewModels, navigation)
3. Trace the user journey step by step
4. Evaluate each step against all 10 heuristics
5. Classify findings by severity
6. Produce structured report with scores

## Invoking the Agent

Use the `ux-auditor` agent for comprehensive evaluations:

```
Dispatch ux-auditor agent with the flow name and relevant file paths
```

## Sources

- [Nielsen's 10 Usability Heuristics (NN/G)](https://www.nngroup.com/articles/ten-usability-heuristics/)
- [How to Conduct a Heuristic Evaluation (NN/G)](https://www.nngroup.com/articles/how-to-conduct-a-heuristic-evaluation/)
- [Heuristic Evaluation on Mobile Interfaces (PMC)](https://pmc.ncbi.nlm.nih.gov/articles/PMC4177852/)
