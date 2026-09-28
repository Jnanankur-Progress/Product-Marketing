# Product Marketing Skills

Eight packaged Claude skills for core product marketing work and Progress/Chef brand compliance.

These skills live in `.claude/skills` as packaged `.skill` files and share a common context file at `.agents/product-marketing-context.md`.

## Included Skills

| Skill | Purpose |
|---|---|
| `product-marketing-context` | Creates and maintains the shared PMM context file |
| `messaging-positioning` | Builds positioning, value props, message houses, and persona messaging |
| `competitive-intelligence` | Produces competitor analysis, battle cards, and comparison-page inputs |
| `customer-research` | Develops ICP, personas, JTBD, VoC, and win/loss insights |
| `go-to-market` | Plans launches, campaigns, timelines, enablement, and cross-functional GTM execution |
| `pricing-packaging` | Recommends pricing models, tiers, value metrics, and pricing-page guidance |
| `progress-brand-compliance` | Produces and audits fully branded Progress collateral, including editable DOCX/PPTX and rendered PDF |
| `chef-brand-compliance` | Produces and audits fully branded Chef DOCX/PPTX/PDF using Chef overrides on the Progress baseline |

## How It Works

1. Start with `product-marketing-context`.
2. Save shared context in `.agents/product-marketing-context.md`.
3. Run the specialized skills as needed. They should read the context file first and only ask for missing task-specific details.
4. Save strategy docs and working outputs in `.agents` unless your workflow requires another location.

## Repository Layout

- `.claude/skills`: packaged skill files used by Claude
- `skills`: byte-identical mirrors of the packaged skill files
- `.claude/.claude-plugin/plugin.json`: Claude plugin metadata
- `.agents/product-marketing-context.md`: shared PMM context file
- `CLAUDE.md`: repo-level operating instructions for Claude
- `my-gtm-context.md`: reference template

## Using With Claude

### Claude Code / Claude Desktop

Open this repository as your working directory. Claude can use the packaged skills from `.claude/skills` directly.

### Claude.ai Projects

Upload:

- `CLAUDE.md`
- The packaged `.skill` files from `.claude/skills`
- Optionally `.agents/product-marketing-context.md` if you want to preload context

Do not look for unpacked `SKILL.md` folders in this repo. The shipped artifacts are the `.skill` packages themselves.

## Recommended Workflow

1. Create or update product context.
2. Define messaging and positioning.
3. Run customer research and competitive intelligence.
4. Build pricing and packaging guidance.
5. Turn that strategy into a GTM plan.
6. Create or audit Progress collateral with `progress-brand-compliance`.
7. Create or audit Chef collateral with `chef-brand-compliance`.

## Notes

- This repo ships 8 packaged skills.
- Brand-compliance packages include authoritative rule, workflow, and source references; official logo/font binaries remain in the Progress Brand Bank and are not redistributed.
- The brand skills remediate colors, typography, imagery, icons/illustration/devices, layout, accessibility, and eligible Progress-owned logos. They preserve third-party logos unchanged and keep compliance reports separate from clean output files.
- Use `.agents/product-marketing-context.md` for shared context.
- If you add more skills later, update `README.md`, `CLAUDE.md`, and `.claude/.claude-plugin/plugin.json` together.
