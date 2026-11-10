# Julylan Johnson

Senior developer and CTO building trading infrastructure, agent tooling, and the systems around them.

I write skills for AI agents — the reusable procedures that make an agent good at a specific job rather than merely capable of it. Each one is a public repo with the full method, the reference material, and the failure cases written down.

Everything here installs with one command:

```bash
claude plugin marketplace add Verstige/<skill-name>
claude plugin install <skill-name>@<skill-name>
```

## Skills

### Trading and finance

| Skill | What it does |
| --- | --- |
| **[broker-rate-limit-cache](https://github.com/Verstige/broker-rate-limit-cache)** | Stop hammering a throttling broker API. A persistent per-account cache with stale-while-revalidate, cross-key fallback, and the one cache-key bug that makes the cache never hit. · [$9 on Agensi](https://agensi.io/skills/broker-rate-limiter-cache-throttle-survive-429s) |
| **[broker-realtime-push](https://github.com/Verstige/broker-realtime-push)** | Give a REST-only broker a live feed. One server-side poll fans out deltas to every open tab over SSE, instead of each browser tab polling the broker on its own. · [$9 on Agensi](https://agensi.io/skills/realtime-trading-data-sse-fan-out-for-rest-brokers) |
| **[broker-contract-sizes](https://github.com/Verstige/broker-contract-sizes)** | Stop your P&L disagreeing with your broker. The verification workflow for contract sizes, why every broker differs, and how to audit a table that survived a broker migration. · [$12 on Agensi](https://agensi.io/skills/contract-sizes-make-your-p-l-match-the-broker) |
| **[trading-chart-debugging](https://github.com/Verstige/trading-chart-debugging)** | Fix trading dashboards that render wrong with a clean build. The class of bugs where the DOM is correct and the CSS is live, but the chart is blank, collapsed, or covered. · [$12 on Agensi](https://agensi.io/skills/trading-charts-that-render-fix-the-blank-canvas) |
| **[human-trader-signal-pipeline](https://github.com/Verstige/human-trader-signal-pipeline)** | Put humans into an automated signal pipeline. A trader role that shares the bot data path, gets badged in the community, mirrors to a channel, and lands in a public signal log. · [$9 on Agensi](https://agensi.io/skills/human-signal-desk-traders-on-a-bot-pipeline) |

### Shipping and deployment

| Skill | What it does |
| --- | --- |
| **[railway-deploy-verifier](https://github.com/Verstige/railway-deploy-verifier)** | Deploy to Railway and prove the running app actually serves the change. The push command is not the deployment -- a health check against the live domain is. · [$9 on Agensi](https://agensi.io/skills/railway-deploy-verifier-ship-then-prove-it-live) |
| **[railway-graphql-control](https://github.com/Verstige/railway-graphql-control)** | Drive Railway from a script when the CLI hangs on an interactive picker. Full GraphQL reference for deployments, variables, logs and service management. · [$6.75 on Agensi](https://agensi.io/skills/railway-graphql-control-script-deploys-without-cli) |
| **[nextjs-railway-triage](https://github.com/Verstige/nextjs-railway-triage)** | The Next.js app builds locally and dies on Railway. The failure modes are specific -- server bundles, env vars, standalone output, base paths -- and each has a known fix. · [$5 on Agensi](https://agensi.io/skills/next-js-on-railway-fix-the-builds-that-fail) |
| **[nextjs-security-hardening](https://github.com/Verstige/nextjs-security-hardening)** | The pre-deploy security pass for a Next.js app: bot protection, DevTools deterrence, rate limiting, security headers and audit logging, plus a subagent-driven audit that finds real issues. · [$18 on Agensi](https://agensi.io/skills/next-js-security-hardening-headers-bots-limits) |
| **[production-bug-recipes](https://github.com/Verstige/production-bug-recipes)** | Real production failures, each with the symptom, the actual cause, and the fix -- migrations that half-apply, caches that go stale, auth that works until it does not. · [$18 on Agensi](https://agensi.io/skills/production-bug-recipes-50-failures-and-their-fixes) |
| **[ship-grade-dev-workflow](https://github.com/Verstige/ship-grade-dev-workflow)** | Throwaway spikes for feasibility, parallel cleanup passes, pre-commit review with security scanning, and a strict RED-GREEN-REFACTOR loop. The workflow standards that keep a codebase from rotting. · [$14.99 on Agensi](https://agensi.io/skills/ship-grade-dev-workflow-spikes-tdd-review-sec) |
| **[patch-trap-inspector](https://github.com/Verstige/patch-trap-inspector)** | The find-and-replace edits that silently corrupt a codebase, and how to make them safely. Covers generic-pattern replace-all, mixed-indentation traps, template-literal damage and the byte-level recovery recipe. · [$14.99 on Agensi](https://agensi.io/skills/patch-trap-inspector-edits-that-silently-corrupt-code) |
| **[python-node-debugging](https://github.com/Verstige/python-node-debugging)** | pdb in a REPL, debugpy for remote attach, node inspect with Chrome DevTools Protocol, breakpoint configuration and post-mortem analysis for processes that will not die. · [$5 on Agensi](https://agensi.io/skills/python-node-debugging-pdb-debugpy-devtools) |
| **[open-source-release-readiness](https://github.com/Verstige/open-source-release-readiness)** | Audit a repo before you publish it: licence correctness, README quality, topics, branch protection and NOTICE compliance. Find the problems that block a clean open source release. · [$14.99 on Agensi](https://agensi.io/skills/open-source-release-readiness-license-notice) |

### Product and brand

| Skill | What it does |
| --- | --- |
| **[logo-identity-design](https://github.com/Verstige/logo-identity-design)** | Design a real identity, not one mark. Captures brand context, writes the visual brief, generates prompt concepts, then ships production SVGs, favicons, social images and a PWA manifest. · [$18 on Agensi](https://agensi.io/skills/logo-identity-design-from-brief-to-svg-brand-kit) |
| **[svg-logo-generator](https://github.com/Verstige/svg-logo-generator)** | Go from a blank page to a complete brand asset kit. Scans your project for existing colours and type, proposes concepts, then exports SVG variants, favicons and social cards. · [$9 on Agensi](https://agensi.io/skills/svg-logo-generator-concept-to-full-brand-kit) |
| **[brand-dna](https://github.com/Verstige/brand-dna)** | One file that captures who you are: identity, audience, positioning, values and voice. Every other design skill reads it first, so nothing drifts between projects. · [$9 on Agensi](https://agensi.io/skills/brand-dna-capture-identity-voice-and-positioning) |
| **[living-product-deck](https://github.com/Verstige/living-product-deck)** | A single self-updating HTML product document: table of contents, anchored sections, vertical-scroll slides, populated from the actual codebase so the deck stays true as the product moves. · [$14.99 on Agensi](https://agensi.io/skills/living-product-deck-docs-that-update-themselves) |
| **[anti-slop-ui-design](https://github.com/Verstige/anti-slop-ui-design)** | Stop shipping interfaces that look like every other AI-generated page. Enforces deterministic typography, one accent colour, real loading and error states, asymmetric layouts, and motion that runs at 60fps on a phone. · [$19.99 on Agensi](https://agensi.io/skills/anti-slop-ui-design-ship-interfaces-that-aren-t-ai) |

### Data, research and documents

| Skill | What it does |
| --- | --- |
| **[pdf-document-extraction](https://github.com/Verstige/pdf-document-extraction)** | Get text out of real documents. Text PDFs, scanned pages, images and Office files, plus natural-language edits that preserve the original layout. · [$5 on Agensi](https://agensi.io/skills/pdf-document-extraction-text-scans-and-edits) |
| **[academic-research-toolkit](https://github.com/Verstige/academic-research-toolkit)** | Search arXiv and Semantic Scholar, manage a wiki knowledge base, write papers with a full BibTeX pipeline, and monitor the feeds that matter for your field. · [$11.99 on Agensi](https://agensi.io/skills/academic-research-toolkit-papers-citations-feeds) |
| **[evidence-only-resume-writer](https://github.com/Verstige/evidence-only-resume-writer)** | Write a resume and bio from what you actually shipped. No adjectives, no invented impact — just concrete work, real numbers, and the evidence behind every claim. · [$5 on Agensi](https://agensi.io/skills/evidence-only-resume-writer-no-adjectives-just-proof) |
| **[infra-fact-check](https://github.com/Verstige/infra-fact-check)** | Verify an AI's infrastructure pricing and plan claims before you act on them. Checks the plan actually exists, prices the real workload, and flags the tier that quietly does not fit. · [$11.99 on Agensi](https://agensi.io/skills/infra-fact-check-verify-pricing-before-you-buy) |

### Automation and integrations

| Skill | What it does |
| --- | --- |
| **[gmail-operations](https://github.com/Verstige/gmail-operations)** | Search, read, label, draft and send through the Gmail API with the failure modes handled -- rate limits, partial failures, and the draft that never got sent. · [$5 on Agensi](https://agensi.io/skills/gmail-operations-read-triage-and-reply-reliably) |
| **[linear-cli](https://github.com/Verstige/linear-cli)** | Manage Linear issues, projects and teams over GraphQL and curl. No SDK to install, no MCP server to run, just the API and the query shapes that work. · [$5 on Agensi](https://agensi.io/skills/linear-without-the-sdk-issues-projects-teams) |
| **[webhook-driven-agent-runs](https://github.com/Verstige/webhook-driven-agent-runs)** | Turn an incoming event into work your agent actually does. Subscription lifecycle, signature verification, idempotent delivery and the retry behaviour that stops duplicate runs. · [$6.75 on Agensi](https://agensi.io/skills/webhook-driven-agent-runs-turn-events-into-work) |
| **[square-commerce-ops](https://github.com/Verstige/square-commerce-ops)** | Operate Square end to end: catalogue items and variations, inventory counts, payments, and per-employee sales attribution, with the exact request shapes that work. · [$6.75 on Agensi](https://agensi.io/skills/square-commerce-ops-catalog-inventory-payments) |
| **[pwa-push-notifications](https://github.com/Verstige/pwa-push-notifications)** | Service worker, manifest, VAPID keys, subscription lifecycle and the silent failures that make push work in dev and never arrive in production. · [$9 on Agensi](https://agensi.io/skills/pwa-push-wire-up-web-push-that-actually-delivers) |
| **[local-voice-transcription](https://github.com/Verstige/local-voice-transcription)** | Transcribe voice notes and recordings on the machine itself. Nothing leaves the device, and it works when the network does not. · [$5 on Agensi](https://agensi.io/skills/local-voice-transcription-no-cloud-no-upload) |
| **[lan-device-control](https://github.com/Verstige/lan-device-control)** | Discover devices on the local network, authenticate, and send commands over their local APIs -- no cloud round trip, no vendor app. · [$5 on Agensi](https://agensi.io/skills/lan-device-control-find-and-drive-what-s-on-your-network) |
| **[tv-remote-control](https://github.com/Verstige/tv-remote-control)** | Find a smart TV on the LAN, pair with it, and control playback and power from an agent -- the protocol is documented and the quirks are known. · [$5 on Agensi](https://agensi.io/skills/tv-remote-control-drive-your-set-over-the-network) |

### Working with agents

| Skill | What it does |
| --- | --- |
| **[skill-marketplace-publisher](https://github.com/Verstige/skill-marketplace-publisher)** | Package, license and sell agent skills as a public marketplace. Provenance checks, privacy gating, integrity gates and a self-verifying build that fails loudly instead of shipping something broken. · [$14.99 on Agensi](https://agensi.io/skills/skill-marketplace-publisher-package-license-sell) |
| **[skill-provenance-audit](https://github.com/Verstige/skill-provenance-audit)** | Audit a skill directory before you sell it: content hashing against upstream, registry lock-file checks, alias detection, and the licence rules that decide what you may ship. · [$5 on Agensi](https://agensi.io/skills/skill-provenance-audit-know-before-you-ship) |
| **[release-diff-reporter](https://github.com/Verstige/release-diff-reporter)** | Compare two snapshots of the same codebase — two zip releases, two git refs, two staging dumps — and get a categorised what-changed report instead of a directory listing. · [$5 on Agensi](https://agensi.io/skills/release-diff-reporter-what-changed-between-builds) |
| **[session-librarian](https://github.com/Verstige/session-librarian)** | Your conversation history is a library, not a landfill. Find the session you need, rename it so you can find it again, archive what is done, prune what is noise. · [$5 on Agensi](https://agensi.io/skills/session-librarian-find-rename-archive-prune) |
| **[scope-discipline](https://github.com/Verstige/scope-discipline)** | Ship the integration, ask before exposing the surface. The rule that keeps a small feature request from turning into a public API you have to support forever. · [$5 on Agensi](https://agensi.io/skills/scope-discipline-ship-integration-ask-before-surface) |
| **[implementation-plan-writer](https://github.com/Verstige/implementation-plan-writer)** | Turn a request into a plan an agent can execute. Bite-sized tasks, real file paths, ordered by dependency, with the verification step written in. · [$5 on Agensi](https://agensi.io/skills/implementation-plan-writer-bite-sized-tasks-paths) |
| **[desktop-cli-development](https://github.com/Verstige/desktop-cli-development)** | Ship software people install: Electron packaging, icons, macOS notarization, Apple Notes integration and Node CLIs built with Commander. · [$5 on Agensi](https://agensi.io/skills/desktop-cli-development-electron-notarization) |
| **[fork-to-brand](https://github.com/Verstige/fork-to-brand)** | Fork an open source app and make it yours without losing the merge. Renames every layer in dependency order, keeps upstream reachable, and proves the rename did not break anything. · [$14.99 on Agensi](https://agensi.io/skills/fork-to-brand-rebrand-an-app-without-breaking-upstream) |
| **[debug-hermes-tui-commands](https://github.com/Verstige/debug-hermes-tui-commands)** | Debug a slash command in the Hermes TUI: the Python command layer, the gateway transport, and the Ink UI that renders the result. |
| **[kanban-orchestrator](https://github.com/Verstige/kanban-orchestrator)** | A decomposition playbook for an orchestrator that routes work to specialists. The rules for splitting work, choosing the right agent, and never doing the job itself. |
| **[tui-widgets](https://github.com/Verstige/tui-widgets)** | Author live widget apps for a terminal dashboard: real-time data, custom layouts, and the lifecycle hooks that keep a panel updating without leaking processes. |

### Research and device work

| Skill | What it does |
| --- | --- |
| **[competitor-stack-recon](https://github.com/Verstige/competitor-stack-recon)** | Work out what a company actually runs. Fingerprints JS bundles, discovers the CMS and commerce platform, maps the API surface and infers the backend from public web assets alone. · [$11.99 on Agensi](https://agensi.io/skills/competitor-stack-recon-fingerprint-any-web-platform) |
| **[railway-ops](https://github.com/Verstige/railway-ops)** |  |
| **[hermex-iphone-setup](https://github.com/Verstige/hermex-iphone-setup)** | Connect the Hermex iPhone app to a local Hermes dashboard over the network, with the pairing and reachability checks that stop a half-installed setup. |
| **[petdex](https://github.com/Verstige/petdex)** | Install and select animated mascots for your terminal. Pick a companion, wire its idle and working animations, and keep it out of the way when you need the line. |

## Other work

- [verstige-skills](https://github.com/Verstige/verstige-skills) — the full Claude Code marketplace: 65 skills, one plugin each, with provenance and privacy gates in the build.

## Contact

- GitHub: [@Verstige](https://github.com/Verstige)
