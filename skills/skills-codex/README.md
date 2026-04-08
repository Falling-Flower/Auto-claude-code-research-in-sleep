# `skills-codex`

Codex-native mirror of the ARIS research skill pack.

## Overview

This package currently contains `39` skills adapted for OpenAI Codex-style agents, plus a small set of shared reference files used by writing workflows.

It is meant to be copied into `~/.codex/skills/` so the mirrored skills are available locally without depending on the original `skills/` tree.

## Included Skills

The current skill set is:

- `ablation-planner`
- `analyze-results`
- `arxiv`
- `auto-paper-improvement-loop`
- `auto-review-loop`
- `auto-review-loop-llm`
- `auto-review-loop-minimax`
- `comm-lit-review`
- `dse-loop`
- `experiment-bridge`
- `experiment-plan`
- `feishu-notify`
- `formula-derivation`
- `grant-proposal`
- `idea-creator`
- `idea-discovery`
- `idea-discovery-robot`
- `mermaid-diagram`
- `monitor-experiment`
- `novelty-check`
- `paper-compile`
- `paper-figure`
- `paper-illustration`
- `paper-plan`
- `paper-poster`
- `paper-slides`
- `paper-write`
- `paper-writing`
- `pixel-art`
- `proof-writer`
- `rebuttal`
- `research-lit`
- `research-pipeline`
- `research-refine`
- `research-refine-pipeline`
- `research-review`
- `result-to-claim`
- `run-experiment`
- `training-check`

## Layout

```text
skills-codex/
  <skill-name>/
    SKILL.md
    ...
  comm-lit-review/
    references/
  paper-write/
    templates/
  shared-references/
    ...
```

Notes:

- `shared-references/` is not a skill by itself; it supports `paper-plan` and `paper-write`.
- `comm-lit-review` includes extra reference files.
- `paper-write` includes venue templates used during drafting.

## Scope

This package mirrors portable skill content for Codex. It intentionally focuses on:

- task boundaries and workflows
- Codex-compatible instructions
- lightweight bundled references or templates required by the skills

It does not try to ship the full runtime environment. In particular, this package does not include:

- Python dependency installation
- LaTeX, Poppler, GPU, SSH, or conda setup
- MCP server configuration
- API keys or environment variables

The following upstream-only areas are also intentionally not mirrored here:

- `.system/*`

## Install

Copy this directory into your Codex skills path:

```bash
mkdir -p ~/.codex/skills
cp -a skills/skills-codex/* ~/.codex/skills/
```

Optional companion dependency for the `deepxiv` skill:

```bash
pip install deepxiv-sdk
```

If you also use reviewer overlay packages, install this base package first, then apply the overlay on top.
