# Using AI to Gather Checklist Data

This document gives practical recommendations for using AI (LLMs, code assistants, agents) to automatically or semi-automatically gather the [What to handover?](README.md#what-to-handover) checklist data. The goal is to speed up filling the PHF checklist while keeping human review. All 15 checklist sections in the README are covered below.

## General principles

- **AI as assistant, not single source of truth.** Always verify AI output with humans and fill gaps from people and meetings.
- **Data sources to point AI at:** Repository (code, README, configs), wiki (Confluence, Notion, SharePoint), issue tracker (Jira, GitHub Issues), CI configs, runbooks, and exported docs. Use **Atlassian MCP** (Model Context Protocol) when available so AI can query Jira and Confluence directly instead of manual exports.
- **Privacy and compliance.** Do not feed sensitive data (passwords, PII, confidential contracts) into public or unapproved AI. Prefer local or approved tools where policy requires it.

## Section-by-section recommendations

### 1. Product/Project Overview

- Summarize requirements docs, product briefs, and OKRs; ask AI to extract functional/non-functional requirements and use cases.
- Infer scope and priorities from epics, backlog, and roadmap exports (sanitize if needed).
- From issue tracker exports, summarize pending work, milestones, overdue items, and commitments.

### 2. Team

- Extract names and roles from org docs, Active Directory exports, or wiki pages (only where approved for AI use).
- Feed structured lists (e.g. CSV or tables) and ask AI to draft an org chart or contact list.
- Do not put performance feedback, HR data, or personal plans into AI unless using an approved internal tool.

### 3. Design

- Infer architecture from repo structure, README, and architecture docs; ask AI to summarize software architecture and tech stack.
- Point AI at API specs (Swagger/OpenAPI, RAML) and integration docs to list third-party products and interfaces.
- Use package files (e.g. `package.json`, `requirements.txt`, `pom.xml`) and configs to list tech stack and known technical debt mentions.

### 4. Development Tools

- Parse repo: `.github/`, `Jenkinsfile`, `Makefile`, `.gitlab-ci.yml`, IDE configs (e.g. `.vscode/`) to list VCS, CI, linters, and wikis.
- Ask AI to list development environment setup, who provisions access (if documented), and automatic documentation building from configs.

### 5. Source Code

- Analyze repo layout, entry points, and dependencies; summarize from CONTRIBUTING, README, and code comments.
- Infer VCS strategy (e.g. git flow) from branch protection rules, README, or contributing guides.
- Use AI to summarize coding conventions, exception handling, logging approach, and where deployment/ops scripts and env config live.

### 6. Build and Release Management

- Extract build types, CI/CD pipelines, and release process from CI configs, release scripts, and changelog/versioning docs.
- Ask AI to summarize release and patch strategy from docs and repo history (tags, release notes).

### 7. QA

- Infer from test directory layout, coverage configs (e.g. Jest, pytest-cov), and test docs; summarize unit, integration, API, and UI testing approach.
- Summarize quality gates, test data sources, test environment access (from docs only), and QA sign-off process where documented.

### 8. Deployment

- Parse deployment and runbook docs, env configs (no secrets), and CI/CD definitions to list environments (DEV, QA, UAT, STAGING, PROD).
- Summarize who deploys, approval chain, and security checking (e.g. vulnerability scanning) from docs.

### 9. Documentation

- Index where docs live (Confluence, Notion, repo wiki, SharePoint) from README and project docs.
- Ask AI to summarize or list user guide, developer guide, setup guide, and integration/API docs and their locations.

### 10. Project management

- Summarize project history, stakeholders, SDLC, charter, key customers, roadmap, and risk management from PM docs and backlog exports.
- Extract meeting cadence, escalation paths, and reporting from meeting notes and process docs (avoid confidential budget details in prompts).

### 11. System Administration

- Summarize from runbooks and admin docs: accounts (no credentials), installed packages, third-party interfaces, licenses, cron jobs, network diagram references, backup/restore, monitoring.
- Do not put passwords or secrets into AI prompts.

### 12. Maintenance

- Summarize SLA, disaster recovery, change management, service desk, on-call rotation, maintenance windows, and known recurring issues from ops docs.
- Extract monitoring and logging approach from runbooks and config docs.

### 13. Contract and Budget

- Use only high-level, non-sensitive summaries (e.g. “budget approval thresholds” without figures); list suppliers/vendors and contact types if allowed by policy.
- Do not feed confidential contracts, invoices, or exact budget figures into public or unapproved AI.

### 14. AI tools and services

- Infer from repo (e.g. `.cursor/`, `.github/` workflows using AI APIs), docs, and policy; list AI tools used by the team (e.g. Copilot, Cursor, ChatGPT, Claude, internal assistants).
- Summarize usage policies, data handling, acceptable use, access and licensing, and ownership/escalation from policy docs.

### 15. Handover sign-off

- AI cannot gather this. Dates, acceptance by the incoming PM, and stakeholder sign-off remain human-only. Use the checklist to remind that this step is required after all other data is gathered.

## Suggested workflows

- **Atlassian MCP:** If your AI assistant supports MCP, enable the Atlassian MCP server for Jira and Confluence. Then ask the AI to query Jira (issues, epics, backlog, roadmap) and Confluence (pages, spaces) directly to fill checklist sections 1 (Product/Project Overview), 9 (Documentation), and 10 (Project management), and to cross-check other sections.
- **Cursor / VS Code + AI:** “Use this repo and the [What to handover?](README.md#what-to-handover) checklist section [N]. List what’s present and what’s missing for that section.”
- **One-off prompts:** “Given this [README / Confluence export / doc], fill a table: checklist section → evidence or gap.”
- **Incremental:** Run AI per section, then merge results into one handover doc and tick off items in the README or a copy of the checklist.

## Link back to PHF

- **Checklist:** [What to handover?](README.md#what-to-handover) in README.md is the canonical 15-section list.
- **Agents:** [AGENTS.md](AGENTS.md) instructs AI assistants to suggest checklist items and keep handover aligned with the PHF structure.
