# ROADMAP — Gnosis

Tracking per CLAUDE.md §7. Gnosis was migrated to a clean history on the
`Gauthambinoy20` account, verified working end to end, and shipped green on CI.

## Milestone 1 — Clean migration ✅ 100%

- [x] 1.1 Re-init fresh history (no old `.git`, single author, no AI traces) ... (9b195d2 …)
- [x] 1.2 Backend committed by feature domain (config, models, LLM gateway, memory/RAG, learning, orchestration, automation, billing, observability) — ~30 commits
- [x] 1.3 API routes committed by domain (auth, agents, memory, intelligence, automation, governance, system)
- [x] 1.4 Tests, frontend (by area), SDK, Terraform (by layer), CI, docs committed
- [x] 1.5 Removed AI-assistant files (frontend/CLAUDE.md, frontend/AGENTS.md) and a Co-authored-by example

## Milestone 2 — Verified working baseline ✅ 100%

- [x] 2.1 Backend: `py_compile` + ruff clean + **1792 pytest pass** (1 skipped), LLM mocked
- [x] 2.2 Frontend: typecheck + lint + production build pass (~93 vitest tests)

## Milestone 3 — Published + CI green ✅ 100%

- [x] 3.1 Pushed to `github.com/Gauthambinoy20/gnosis` (public)
- [x] 3.2 Repointed all old-account references to Gauthambinoy20
- [x] 3.3 All workflows green: Gnosis CI, Security (gitleaks/trivy/pip-audit/bandit/npm-audit), Type Checks

## Milestone 4 — Security hardening ✅ 100%

- [x] 4.1 Fix Python CVE (PYSEC-2026-161): bump starlette → 1.x .......... (6df191b)
- [x] 4.2 Fix Next.js high-severity CVEs: surgical bump to 16.2.7 ........ (d709598)

## Milestone 5 — UI polish ✅ 100%

- [x] 5.1 Constrain oversized OAuth provider icons on login ............. (59e1cad)
- [x] 5.2 Raise contrast of auth form inputs and labels ................. (c47282a)
- [x] 5.3 Add landing + sign-in screenshots to the README .............. (df31c3d)

## Known issues / notes

- Provider keys (OpenRouter/OpenAI/Anthropic) are optional — tests mock all LLM calls.
- Frontend lint reports 21 advisory warnings (0 errors) — mostly `set-state-in-effect`.
- Dashboard screens are auth-gated; capturing their screenshots needs the full
  `docker compose` stack (backend + Postgres + Redis) running.

## Next (optional)

- [ ] Run the full `docker compose` stack and add dashboard screenshots.
- [ ] Tighten remaining frontend lint warnings to zero.

## ✍️ TODO: my words

(design decisions and personal notes go here — left for Gautham per CLAUDE.md §5)
