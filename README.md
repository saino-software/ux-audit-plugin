# UX Audit Plugin

UX heuristic evaluation agent for mobile apps. Evaluates user flows against Nielsen's 10 usability heuristics with structured, actionable findings.

## Installation

```bash
/plugin marketplace add ingrodelvalle/ux-audit-marketplace
/plugin install ux-audit@ux-audit-marketplace
```

## Usage

```bash
/ux-audit budget-flow
/ux-audit create-transaction
```

Or invoke the agent directly in conversation:

> "audit the UX of the transaction creation flow"

## What You Get

- `ux-auditor` agent — conducts structured heuristic evaluations
- `ux-heuristic-audit` skill — reference for the 10 heuristics
- `/ux-audit` command — quick invocation

## Scoring

Each flow gets scored 1-5 per heuristic (50 max), with findings classified as Critical/Major/Minor/Suggestion.
