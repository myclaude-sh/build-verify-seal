---
name: build-verify-seal
display_name: Build-Verify-Seal
description: "Anti-hallucination engineering framework for Claude Code. 3-phase pipeline: Architecture (6 Questions) > Engineering (Build-Verify-Seal) > Verification (XP Scorecard). Enforces contracts, bottom-up bu"
version: 1.0.0
author: cognittusai
license: Proprietary
tags:
  - "engineering"
  - "anti-hallucination"
  - "methodology"
  - "architecture"
  - "quality"
  - "build-system"
  - "contracts"
  - "verification"
  - "scorecard"
marketplace_url: "https://myclaude.sh/p/build-verify-seal"
user-invocable: true
---

# Build-Verify-Seal

**Engineering framework that prevents AI drift in complex projects.**

If you've ever lost time because Claude invented an API that doesn't exist, rewrote a module that was already done, or forgot what it built two sessions ago — this fixes that.

## The Problem

AI assistants hallucinate. They invent flags, forget contracts, skip layers, and drift from what was agreed. The longer the session, the worse it gets. On complex projects with 3+ modules, this becomes a real engineering risk.

## The Solution: 3-Phase Pipeline

### Phase 1: Architecture — 6 Questions Before Coding

No code until these are answered:

1. What is the problem?
2. Who uses it?
3. What data goes in and out?
4. Where will it run?
5. What can go wrong?
6. How to safeguard it?

Output: ARCHITECTURE.md with contracts for every module.

### Phase 2: Engineering — Build-Verify-Seal

- **Module Contracts** — Every module defines Input, Output, success criteria, and idempotency
- **Bottom-up Build Order** — Utils first, then base modules, then composites, then orchestrator. Never skip a layer
- **1 Module Per Session** — Focus prevents drift
- **Objective Seal Criteria** — A module is SEALED only when: reproducible test passes, user approves, output matches contract
- **Drift Prevention** — If code diverged from contract, update docs in the same session. Never "fix later"

### Phase 3: Verification — XP Scorecard

5 pillars checked at every milestone:

| Pillar | What it verifies |
|--------|-----------------|
| Docs | Architecture and project docs reflect current code |
| Tests | Every sealed module has a reproducible test |
| CI | Automated verification on push (or documented smoke test) |
| Protection | Config files in .gitignore, sensitive data out of code |
| Commits | Conventional format, atomic, 1 commit per module |

Minimum 3/5 per layer. 5/5 before release.

## When to Use

- Projects with 3+ modules
- 2+ external API integrations
- Media/content pipelines
- Any project where AI drift has cost you time

## How to Use

After installing, invoke the skill in Claude Code. It will guide you through all 3 phases, enforce contracts, and prevent drift automatically.

---

*By @cognittusai — Built from real-world experience shipping AI-assisted projects.*

