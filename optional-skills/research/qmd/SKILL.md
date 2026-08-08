---
name: qmd
description: Bootstrap version-matched QMD instructions for specialist Profiles while enforcing work-only local retrieval.
license: MIT
compatibility: Requires qmd CLI. Run `qmd skill show` for version-matched command instructions.
allowed-tools: Bash(qmd:*), mcp__qmd__*
---

# QMD - specialist work-only retrieval

Load the full version-matched command instructions with `qmd skill show`.
The following local boundary is authoritative:

- Every `qmd search` or `qmd query` must include `-c work`.
- Never omit the collection filter.
- Never use `-c personal` or combine `work` with `personal` from a specialist
  Profile.
- A zero-result work search does not authorize access to personal content.
- If the user explicitly needs a personal or cross-domain search, hand the task
  back to a dynamic-scope runtime; do not call or supervise that runtime.

Use exact BM25 search for stable names and structured `qmd query` with `intent:`
plus `lex:` or `vec:` for conceptual recall. Fetch the full work source with
`qmd get` or `qmd multi-get` before answering, and preserve document provenance
and line numbers.

Index maintenance is not owned by specialist Profiles. They consume the shared
derived index read-only and make their own task decisions within the work-only
boundary.
