# ASA CLI — Architecture Stabilization Engine

> Scan. Stabilize. Verify. Ship with confidence.
>
> The ASA CLI detects structural chaos in AI-built SaaS apps and transforms them
> into maintainable, slice-oriented architectures — automatically.

## Install

```bash
# From GitHub Releases
pip install https://github.com/janvoldan/asa-cli/releases/download/v1.0/asa-1.0.0-py3-none-any.whl

# From PyPI (coming soon)
# pip install asa
```

## Quick Start

```bash
# Diagnose structural risk (always free)
asa scan .

# Stabilize an existing app (hero command)
asa stabilize --yes

# Or step by step:
asa spec infer .        # Infer architecture spec
asa plan                # Dry-run — see what changes
asa apply               # Install foundation
asa verify              # Check architecture compliance
asa repair              # Fix remaining drift
```

## Commands

### Diagnostic (Always Free)

| Command | Description |
|---|---|
| `asa scan <path>` | AI Chaos Index — structural risk diagnostic (0–100) |
| `asa scan <path> --json` | Machine-readable JSON output |
| `asa --help` | CLI help |

### Stabilization Engine

| Command | Description |
|---|---|
| `asa stabilize [--yes] [--dry-run]` | Full stabilization flow: scan → infer → plan → apply → bridge → verify |
| `asa spec infer <path>` | Infer `.asa/spec.yaml` from existing codebase |
| `asa plan` | Dry-run — show what `asa apply` would do |
| `asa apply` | Install foundation architecture from spec |
| `asa verify [--ci]` | Verify architecture vs `.asa/spec.yaml` (CI-ready JSON) |
| `asa repair [--auto]` | Detect drift + suggest/apply fixes |

### Foundation

| Command | Description |
|---|---|
| `asa init --name <name>` | Initialize new ASA project with `.asa/spec.yaml` |
| `asa install <module>` | Install foundation module (db-basic, auth-basic, payments-basic) |
| `asa lint [--strict]` | Boundary + structure + security + entitlement enforcement |

### Slice Management

| Command | Description |
|---|---|
| `asa slice new <domain/name>` | Create new vertical slice |
| `asa slice update <domain/name>` | Regenerate slice (preserve user code) |
| `asa slice plan <spec>` | Spec → slice architecture proposal |
| `asa slice split <name>` | Analyze oversized slice, propose split |
| `asa slice build <name>` | Internal build pipeline |
| `asa slice sync` | Validate all contracts |
| `asa slice analyze <name>` | Detailed slice analysis |

### Deployment & UI

| Command | Description |
|---|---|
| `asa deploy` | Architecture-safe deployment (Vercel + Supabase) |
| `asa ui generate <name>` | Regenerate frontend part of slice |

## Foundation Modules

| Module | What it creates |
|---|---|
| `db-basic` | Supabase client, types, utils, seed, migrations framework |
| `auth-basic` | Middleware, session, hooks, types + profiles migration |
| `payments-basic` | Stripe client, plans, webhooks + entitlement guards (requireEntitlement, requireLimit) |

## ASA Native Stack

- **Frontend:** Next.js (App Router) + TypeScript + React
- **UI:** Tailwind CSS + shadcn/ui
- **Backend:** Next.js route handlers / server actions
- **Database:** PostgreSQL via Supabase
- **Auth:** Supabase Auth (SSR/cookie-based)
- **Payments:** Stripe
- **Deploy:** Vercel + Supabase

## Requirements

- Python 3.10+

## Links

- **Website:** [vibecodiq.com](https://vibecodiq.com)
- **Quick Scan:** [vibecodiq.com/analyze-ai-app](https://vibecodiq.com/analyze-ai-app)
- **ASA Standard:** [asastandard.org](https://asastandard.org)

---

*v1.0.0 — 2026-03-10*
