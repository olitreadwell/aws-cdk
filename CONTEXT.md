# aws/aws-cdk context
> refreshed 2026-09-04 | upstream default: main @ 3f3a22b66d91ba510ddfafcc2ce58aab7cdac3fd

## Identity & policies
- upstream: aws/aws-cdk, default branch `main`, primary language TypeScript, English-first (yes — all docs/issues/PRs in English)
- CLA/DCO: none — PR template carries an inline Apache-2.0 attestation ("By submitting this pull request, I confirm that my contribution is made under the terms of the Apache-2.0 license"); no CLA bot, no DCO
- AI-assisted PR policy: unstated — no ban, no disclosure requirement found in CONTRIBUTING.md, .github/, or org `aws/.github` (grep for AI/LLM/generated/ChatGPT/Copilot/automated/bot/machine)
- signed commits required: no (branch protection `required_signatures` = null)
- PR template: `.github/PULL_REQUEST_TEMPLATE.md` (Issue # / Reason / Description / Permissions / Validation / Checklist / Apache-2.0 attestation)
- external tracker: GitHub issues
- issue-first: "encouraged" for significant work only; typo/docs fixes need no issue

## Conventions (verified from merged PRs)
- branch naming: mixed — `fix/...`, `chore/...`, `feat/...`, `automation/...`, `merge-back/...`, `dependabot/...`, plus owner-prefixed (`otaviom/...`, `huijbers/...`). Dominant human pattern: conventional-commit type prefix (`fix/`, `chore/`, `feat/`).
- commit style: Conventional Commits `type(scope): subject` (e.g. `docs(glue-alpha): fix ...`, `fix(core): ...`)
- CI: GitHub Actions; substantive checks are lint/test/typecheck/build. Fork CI runs on fork PRs.
- outside PRs get merged: yes, actively — recent external merges (tadurisaikiran #38707, syukawa-gh typo PRs) and maintainer typo/docs PRs (rix0rrr #38723, otaviomacedo #38731/#38722). Typo/docs PRs are accepted.

## Maintainer picture
- active maintainers: rix0rrr, otaviomacedo, and others; fast turnaround (docs PRs merged within a day)
- areas actively worked: glue-alpha, core validation, logs, s3-deployment, eks-v2 — avoid these for new picks

## Issue-area health
- 2875 open issues; extremely active contribution pipeline; most narrow reported bugs already have an open PR
- environment constraint: aws-cdk-lib jsii build needs ~8GB heap; this container has ~2GB RAM, so the full test suite cannot be built/run here. Docs/typo/comment changes are verifiable by inspection only.

## Gap ledger (dedupe — READ FIRST, never re-pick)
- `2026-08-24` self-found (dropped) — no verifiable high-conviction fix available; every narrow bug had an open PR; only 1 typo found at the time (CONTRIBUTING.md 'doesnt'); jsii build OOMs in this container. Lesson: run codespell across the whole repo, not just CONTRIBUTING.md.
- `2026-09-04` self-found typo bundle (this run) — 9 genuine typos across 6 hand-written files (CONTRIBUTING.md, docs/CLOUDFORMATION.md, ROADMAP.md, codecov.yml, scripts/check-yarn-lock.js, scripts/update-sdkv3-parameters-model.ts). Deduped: no open/merged PR fixes these. Outcome: pr-opened.

## Mined gaps (discovered, not yet attempted)
- `2026-09-04` docs/typo — 9 genuine typos (inspite, doesnt x2, Succesful, lifecyle, contraints, intiatives, repect, compatibiltiy) — status: attempted (this run)
- `2026-09-04` docs — DEPRECATED_APIs.md has ~15 'superceded' typos; not included this run (uncertain if hand-maintained; keep PR focused) — status: proposed
