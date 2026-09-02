# skillcare

Context engineering for Agents. Like a skincare routine, but for working memory.

## Install

**Tell your agent directly:**
```text
Install plugin as described by https://github.com/sinsniwal/skillcare
```

**For Claude Code (as a managed plugin):**
Inside the Claude Code chat, first add the repository as a marketplace, then install:
```text
/plugin marketplace add sinsniwal/skillcare
/plugin install skillcare
```

**For all agents (Cursor, Copilot, Antigravity) via `npx skills`:**
```bash
npx skills@latest add sinsniwal/skillcare
```
*You can also install an individual step: `npx skills@latest add sinsniwal/skillcare/cleanse`*

## The Routine

| # | Skill | Does |
|---|-------|------|
| 1 | **cleanse** | Strips away formatting and structural junk to leave only pure text. |
| 2 | **exfoliate** | Scrubs fluff, opinions, and bias to reveal just the facts. |
| 3 | **tone** | Structures messy data into clean Markdown or JSON. |
| 4 | **extract** | Pulls out exact targets like metrics, code, and entities. |
| 5 | **hydrate** | Fills in missing context and expands acronyms to complete the picture. |
| 6 | **screen** | Masks sensitive data and blocks bad prompts to ensure safety. |

## Usage

```text
"skillcare this webpage"
"exfoliate this press release"
"hydrate this — too many acronyms"
"screen this before sending"
```

Each skill is one `SKILL.md`. No scripts. No deps. No build step.

## FAQ

**Q: Why use separate skills when a single prompt can do all of this?**
A: Focus and cost. Monolithic prompts drop instructions on long documents. Breaking them into atomic skills forces the model to focus 100% on one specific task, cuts token burn by skipping unneeded steps, and makes debugging instant.

**Q: Is this just a naming stunt? Why keep the metaphor instead of literal terms?**
A: Literal terms like "clean" or "process" are dangerously vague. Does "clean" mean stripping HTML, removing author bias, or fixing broken JSON? The metaphor precisely defines the depth and order of the operation. It enforces a strict data pipeline: you intuitively know you must cleanse surface junk before you can hydrate with new context. It's architectural shorthand.

**Q: Do I have to run every step every time?**
A: No. You can call the master `skillcare` command to let the system route dynamically, or chain them manually. A raw server log might just need a `cleanse` and `tone`. A heavily sponsored blog post needs an aggressive `exfoliate`.

**Q: Who is this actually for?**
A: Multi-agent systems. When agents fetch web pages, APIs, or logs, raw noise breaks their reasoning loop. `skillcare` is the middleware that sanitizes their working memory before they hallucinate.

## License

MIT
