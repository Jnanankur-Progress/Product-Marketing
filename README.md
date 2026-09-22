# Product Marketing Skills

Six product marketing skills for Claude and GitHub Copilot: context setup,
messaging, competitive intelligence, customer research, go-to-market planning,
and pricing.

Claude uses the packaged `.skill` archives in `.claude/skills`. GitHub Copilot
uses the repository-native `SKILL.md` directories in `.github/skills`. Both
formats contain the same skill instructions and share context through
`.agents/product-marketing-context.md`.

## Included Skills

| Skill | Purpose |
|---|---|
| `product-marketing-context` | Creates and maintains the shared PMM context file |
| `messaging-positioning` | Builds positioning, value props, message houses, and persona messaging |
| `competitive-intelligence` | Produces competitor analysis, battle cards, and comparison-page inputs |
| `customer-research` | Develops ICP, personas, JTBD, VoC, and win/loss insights |
| `go-to-market` | Plans launches, campaigns, timelines, enablement, and cross-functional GTM execution |
| `pricing-packaging` | Recommends pricing models, tiers, value metrics, and pricing-page guidance |

## How It Works

1. Start with `product-marketing-context`.
2. Save shared context in `.agents/product-marketing-context.md`.
3. Run the specialized skills as needed. They should read the context file first and only ask for missing task-specific details.
4. Save strategy docs and working outputs in `.agents` unless your workflow requires another location.

## Repository Layout

- `.claude/skills/*.skill`: packaged skills used by Claude
- `.claude/.claude-plugin/plugin.json`: Claude plugin metadata
- `.github/skills/<skill-name>/SKILL.md`: repository-native skills discovered
  by GitHub Copilot
- `.github/copilot-instructions.md`: repository-level operating instructions
  for GitHub Copilot
- `skills/*.skill`: distribution copies of the packaged skills
- `.agents/product-marketing-context.md`: shared PMM context created during use
- `CLAUDE.md`: repository-level operating instructions for Claude
- `my-gtm-context.md`: reference context template

## Using With Claude

### Claude Code / Claude Desktop

Open this repository as your working directory. Claude can use the packaged skills from `.claude/skills` directly.

### Claude.ai Projects

Upload:

- `CLAUDE.md`
- The packaged `.skill` files from `.claude/skills`
- Optionally `.agents/product-marketing-context.md` if you want to preload context

### GitHub Copilot

Open this repository in a Copilot coding session. Copilot reads
`.github/copilot-instructions.md` for the shared workflow and discovers each
skill from `.github/skills/<skill-name>/SKILL.md`.

Start with the `product-marketing-context` skill when shared context is missing
or stale. For specialized PMM work, ask Copilot to use the matching skill; it
should read existing `.agents` documents first and save working strategy
documents there unless you request another location.

## Recommended Workflow

1. Create or update product context.
2. Define messaging and positioning.
3. Run customer research and competitive intelligence.
4. Build pricing and packaging guidance.
5. Turn that strategy into a GTM plan.

## Notes

- This repo ships 6 PMM skills.
- Keep each `.github/skills/<skill-name>/SKILL.md` synchronized with the
  corresponding packaged `<skill-name>/SKILL.md`.
- Use `.agents/product-marketing-context.md` for shared context.
- If you add more skills later, update `README.md`, `CLAUDE.md`,
  `.github/copilot-instructions.md`, and `.claude/.claude-plugin/plugin.json`
  together.
