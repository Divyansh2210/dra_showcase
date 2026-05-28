# DRA Management Consulting — Showcase

A deep-research-agent evaluation set in management consulting. Each prompt is a real business case with a single deterministic problem buried under CFO-grade prose, decoy data, and ambiguous formatting.

→ **[Live showcase](#)** _(set this link after enabling GitHub Pages — see below)_

---

## What this is

13 hand-authored evaluation tasks spanning cost optimization, operations research, operations optimization, market strategy, and service ops. Each task ships with:

- A real-world business prompt written in CFO-grade language, with embedded ambiguity
- Expert-authored solution logic with a published golden answer range (not shown to agents)
- Atomic verifiers — each one a single independently-checkable fact
- A sanity-check rationale demonstrating the problem is deterministically solvable

The samples in this repository are a slice of the full dataset. **The full dataset is delivered upon request** — talk to Deccan AI about volume, domain spread, annotator profile, and delivery format.

## Models tested

| Model       | Configuration                                        | ACCEPT count |
|-------------|------------------------------------------------------|--------------|
| OpenAI o3   | `o3-deep-research`, OpenAI API, single rollout       | 3 / 13       |
| Claude Opus | `claude-opus-4-6`, Anthropic API + file explorer     | 3 / 13       |
| Gemini      | `gemini-pro-3-1-deep-research`, Deep Research mode   | 5 / 13       |

> Note: Claude was run with a file-explorer tool; o3 and Gemini used their respective built-in tooling. Tool configurations are not identical across the three models — see each task page's badge popover for the exact setup.

**ACCEPT criterion:** Verifier Pass Rate ≥ 80% **AND** rubric average ≥ 2.5 **AND** no rubric criterion scored 0. Rubric uses five criteria (DI · AR · RF · EP · FD), each scored 0–3.

## Difficulty calibration

Bands are **measured, not asserted** — defined by frontier-model acceptance, not author intuition:

- **Hard** (5 tasks) — 0 / 3 agents accept
- **Medium** (5 tasks) — 1 / 3 agents accept
- **Easy** (3 tasks) — 2+ / 3 agents accept

If frontier models start accepting Hards, the bands re-bind.

## Annotator profile

Ex-MBB & Tier-1 consulting strategists, cross-audited by research-trained reviewers.

> _Repo maintainer: replace this with concrete annotator credentials or a pseudonymous track record before sharing externally. Vague credential claims are a trust risk for the audience this is built for._

## Local viewing

Open `index.html` in any modern browser. No build step required.

## Repository structure

```
index.html               Catalog / landing page
task_01.html .. task_13.html   Per-task detail pages
```

## Publish via GitHub Pages

1. Push this repo to a public GitHub repository.
2. Repo **Settings → Pages**.
3. Source: **Deploy from a branch**, Branch: `main` (root). Save.
4. After a minute, GitHub serves `https://<user>.github.io/<repo>/index.html`.
5. Update the **Live showcase** link at the top of this README.

---

Built by [Deccan AI](https://deccan.ai). Contact for full dataset access and custom evaluation builds.
