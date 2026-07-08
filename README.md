# Awesome Gamma [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of tools, guides, and resources for [Gamma.app](https://gamma.app) — the AI presentation maker. Export workflows, watermark solutions, pricing breakdowns, and alternatives.

Gamma generates presentations, documents, and websites from prompts. This list collects everything useful around it that Gamma's own docs don't cover.

## Contents

- [Official Resources](#official-resources)
- [Export Guides](#export-guides)
- [Watermark Removal](#watermark-removal)
- [Pricing & Plans](#pricing--plans)
- [Alternatives](#alternatives)
- [For Developers & AI Agents](#for-developers--ai-agents)
- [Contributing](#contributing)

## Official Resources

- [Gamma.app](https://gamma.app) — the product itself
- [Gamma Help Center](https://help.gamma.app) — official docs, export how-tos, credit rules
- [Gamma Pricing](https://gamma.app/pricing) — Free / Plus / Team tiers

## Export Guides

- [What's the easiest way to export my Gamma?](https://help.gamma.app/en/articles/8022861-what-s-the-easiest-way-to-export-my-gamma) — official export doc (PDF / PPTX / web)
- [How to Export from Gamma Without Branding](https://gammaremover.com/en/blog/how-to-export-gamma-without-branding/) — what each plan's exports contain and how to get clean output
- [Gamma Free Plan: Credits, Watermark & Limits](https://gammaremover.com/en/blog/gamma-free-plan-limits-2026/) — how the 400 lifetime credits actually work

## Watermark Removal

Free-tier exports carry a "Made with Gamma" badge on every page/slide. Ways to handle it, from fastest to most manual:

### Online (no install)

- [GammaRemover](https://gammaremover.com) — free, runs 100% in the browser via WebAssembly (no upload, no signup); removes the badge object losslessly from PDF & PPTX. [PDF tool](https://gammaremover.com/en/pdf/) · [PPTX tool](https://gammaremover.com/en/pptx/)

### CLI / Python

- [gammaremover/gamma-watermark-remover](https://github.com/gammaremover/gamma-watermark-remover) — `pip install gamma-watermark-remover`; CLI + library (pypdf / python-pptx), batch support
- [DedInc/gamma-ai-watermark-remover](https://github.com/DedInc/gamma-ai-watermark-remover) — local FastAPI web tool; also handles Keynote and PNG ZIP exports
- [K0STEP/gamma_watermark_remover](https://github.com/K0STEP/gamma_watermark_remover) — no-dependency Python script for PDFs
- [Aditya-233/Gamma-Watermark-Remover](https://github.com/Aditya-233/Gamma-Watermark-Remover) — FastAPI-based PDF/PPTX utility

### For AI agents

- [gamma-watermark-remover-mcp](https://github.com/gammaremover/gamma-watermark-remover-mcp) — MCP server for Claude Desktop / Claude Code / any MCP client
- [gamma-watermark-remover-skill](https://github.com/gammaremover/gamma-watermark-remover-skill) — agent skill for Claude Code & OpenClaw

### Manual methods

- **PowerPoint Slide Master** — View → Slide Master → delete the badge from the layouts (Gamma stores it there); free and lossless, PPTX only
- **Canva / Google Slides import** — import the PPTX and delete the badge per slide; conversion may shift fonts/layout
- [5 free methods compared](https://gammaremover.com/en/blog/remove-gamma-watermark-without-upgrading/) — honest comparison table (speed / quality / effort)

### Official route

- **Gamma Plus** removes the watermark from *new* exports (not files already on disk — [what actually happens after upgrading](https://gammaremover.com/en/blog/does-gamma-plus-remove-watermark/))

## Pricing & Plans

- [Gamma Free vs Pro: Is It Worth Paying?](https://gammaremover.com/en/blog/gamma-free-vs-pro-watermark/) — when the paid plan genuinely makes sense
- [How do credits work in Gamma?](https://help.gamma.app/en/articles/7834324-how-do-credits-work-in-gamma) — official credit mechanics
- Rule of thumb: ~40 credits per generated deck; 400 lifetime credits on Free ≈ 10 full decks with edits

## Alternatives

Presentation tools with no watermark on their free tier (or different tradeoffs):

- [Google Slides](https://slides.google.com) — free, collaborative, no AI generation built in
- [Canva](https://canva.com) — free tier, huge template library, AI features on paid
- [Beautiful.ai](https://beautiful.ai) — design-automation focus, trial-based
- [Comparison: Gamma vs Canva vs Google Slides](https://gammaremover.com/en/blog/gamma-vs-canva-vs-google-slides-watermark/) — export/watermark behavior side-by-side
- [Best free presentation tools without watermarks](https://gammaremover.com/en/blog/best-free-presentation-tools-no-watermark/)

## For Developers & AI Agents

- [How Gamma stores its watermark](https://github.com/gammaremover/gamma-watermark-remover#how-detection-works) — PDF object structure & PPTX slide-master anatomy, documented
- [pypdf](https://github.com/py-pdf/pypdf) · [python-pptx](https://github.com/scanny/python-pptx) — the pure-Python libraries that make structural editing possible
- [Model Context Protocol](https://modelcontextprotocol.io) — expose document tools to AI agents

## Contributing

Contributions welcome! Add tools, guides, or resources that are genuinely useful to Gamma users — one line, with a short factual description. Open a PR.

## License

[CC0](https://creativecommons.org/publicdomain/zero/1.0/) — public domain.
