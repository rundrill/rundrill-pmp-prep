# RunDrill PMP

Your personal **PMP certification coach** inside your AI agent — prep PMI's **2026 exam** the way it
actually demands it: by **deciding what the project manager should do FIRST** and **reviewing project
decisions for the planted trap**, not by memorising process tables or watching the AI plan your project
for you. Short targeted drills, an honest picture of where you stand, mistake memory that resurfaces
what you got wrong, and timed mock exams. Your progress lives on the RunDrill MCP server
(`mcp.rundrill.com`), synced across machines — not in a local file.

**Why this course is different.** The PMP exam doesn't reward recall — it hands you a realistic
scenario and asks what the PM should do **FIRST**, and the PMI-preferred answer is rarely the forceful
one. The skill that matters is **situational judgment against the PMI mindset**: be a servant leader,
be proactive, address the root cause, collaborate before you escalate, never ignore or delay, do it
yourself last. When an AI can draft any project plan, charter, or decision on demand, the real risk is
the *illusion of competence* — accepting one that reads fine and is quietly wrong: it jumps to
authority instead of collaborating, escalates too early, taps the wrong reserve, or calls gold plating
a legitimate change. So the **signature drill hands you a confident project decision an AI drafted and
asks you to find the planted PMI-mindset trap, like a peer review.** Alongside it you drill the
situational items, the calculation items (earned value, PERT, the critical path, expected monetary
value, communication channels, the FPIF point of total assumption), classification and
approach-selection, and you build the real artifacts (RACI, scope statement, WBS, risk register) in
chat. Plus timed, domain-weighted **mock exams** as a boss battle (timed practice is the strongest
readiness signal).

The course follows the **2026 Examination Content Outline** — **Foundations** (the language, the
predictive/agile/hybrid approaches, PMBOK 7/8, and how the exam thinks) → **People** (33%) →
**Process** (41%) → **Business Environment** (26%). It is one exam, one path: there are no
specialization tracks to pick, and every domain stays on the way to passing.

**Learn in your language.** The PMP exam is in English, but you don't have to study only in English: set
your native language and the coach explains in it while giving every PMI term as *native (English
original)* — so you reason naturally and still recognise the exact terms on the exam.

## One plugin, three hosts

The coaching skill (`skills/pmp-prep-coach/SKILL.md`) and `.mcp.json` are shared; each host reads its own
manifest and ignores the rest.

| Host | Reads |
|---|---|
| Claude Code / Claude Desktop | `.claude-plugin/plugin.json` + `.mcp.json` |
| OpenAI Codex | `.codex-plugin/plugin.json` + `.mcp.json` |
| Google Antigravity | `plugin.json` + `mcp_config.json` (+ `rules/`) |

The MCP endpoint is `https://mcp.rundrill.com/skills/pmp` — the skills-course host, passing
`subject: "pmp"`. The server routes on the `/skills` segment and ignores the course name; the name makes
PMP register as its own MCP server in your agent. On first use the host opens a browser tab for the
OAuth handshake, then closes it — no API key to paste.

## Install

- **Claude Code / Desktop** — via the RunDrill marketplace:
  ```
  /plugin marketplace add rundrill/rundrill
  /plugin install rundrill-pmp-prep@rundrill
  ```
  Then run `/pmp-prep-coach`.
- **OpenAI Codex** — `codex plugin marketplace add rundrill/rundrill`, then install `rundrill-pmp-prep`.
- **Google Antigravity** — drop this folder into `~/.gemini/config/plugins/rundrill-pmp-prep/` (global) or
  `<workspace>/.agents/plugins/rundrill-pmp-prep/` (workspace-scoped).

## A note on PMP® and PMI®

This is an independent study aid for learning project management and preparing for the PMP certification
exam. It is **not** affiliated with, authorized, or endorsed by the Project Management Institute. *PMP®*,
*PMI®*, *PMBOK®*, and related marks are trademarks of the Project Management Institute, Inc. The course
teaches the publicly documented Examination Content Outline domains and project-management concepts in
our own words; it does not reproduce PMI exam content. PMI updates the exam content outline and the
PMBOK Guide periodically — always confirm current details against PMI's official materials.

## License & attribution

© RunDrill. Licensed under **Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International
(CC BY-NC-ND 4.0)** — full text in [LICENSE](LICENSE). You may view, run, and share this plugin
unchanged, non-commercially, with attribution; you may not use it commercially or publish
modified/derivative versions. For other licensing, contact **hello@rundrill.com**.
