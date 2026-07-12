# Agent instructions — LivingContext public docs

Customer-facing Mintlify site for [LivingContext](https://livingcontext.ai).
Live at https://livingcontext.mintlify.app — **deploys automatically on every
push to `main`**, so pushing IS publishing.

## The standing rule

This site must stay in sync with the product. **Whenever a new commit lands in
the main app repo (`~/Documents/GitHub/LivingContext`) that changes user-facing
behavior, update the matching page(s) here and push in the same working
session.** The main repo's `AGENTS.md` states the same rule from its side; if
a change has no reader-visible impact, say "no docs impact" explicitly.

## What belongs here (and what doesn't)

- Audience: **customers and prospects.** Write in product terms — what a user
  sees and configures, not how it's implemented.
- **Never** include: internal file paths, environment variable names, secrets,
  infra details, operational runbooks, or anything from the internal docs
  repo. Engineering content goes to `livingcontext-internal-docs`.
- Be honest about limits: features that don't exist yet belong in
  `admin/security.mdx` → "On the roadmap" (or equivalent), not in silence.

## Code-area → page map

| Change in the app | Update here |
| --- | --- |
| Settings sections, org policy | `admin/settings-reference.mdx`, `admin/security.mdx`, `admin/organizations.mdx` |
| Roles/permissions | `admin/roles-and-permissions.mdx` |
| Security features | `admin/security.mdx` (+ `admin/enterprise.mdx` governance table) |
| Docs viewer, editing, CRs, inbox, coverage, search | `guides/` |
| Agents (workspace, doc editor, coverage auditor) | `agents/` |
| Capture extension | `capture/` |
| GitHub/GitLab/Salesforce/Confluence/Slack/MCP | `integrations/` |
| Pricing/billing | `admin/billing.mdx`, `admin/enterprise.mdx` |
| Onboarding/login | `getting-started/` |

## Conventions

- Pages are MDX with `title` / `description` / `icon` frontmatter; navigation
  lives in `docs.json` — **add every new page to a `docs.json` group** or it
  won't appear.
- Use Mintlify components already in use: `<CardGroup>`, `<Card>`, `<Steps>`,
  `<Note>`, `<Warning>`, tables.
- Brand assets: `favicon.svg` + `logo/light.svg` + `logo/dark.svg` carry the
  LivingContext mark (blue `#2e5bff` square, amber `#ffaa00` quarter-circle).
- Preview locally with `mint dev` (http://localhost:3000).
