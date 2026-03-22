# Variation Engine

A production-ready prototype for AI-powered ad variation generation. Built as a single React component, it demonstrates how creative teams can decompose a winning ad into controllable axes — actor, background, hook, script, audio, localization — and generate hundreds of targeted variations through a combinatorial pipeline.

## The Concept

Performance marketing teams often find a single ad creative that converts well, then need to scale it across audiences, markets, and platforms. Today this means manually briefing dozens of variants or accepting template-based output that lacks creative nuance.

Variation Engine proposes a different model: **axis decomposition**. A source video is analyzed into its creative components (actor, setting, script arc, hook, audio, language), and each axis becomes independently controllable. The system then generates the combinatorial space of all possible variations, letting teams review and approve at scale.

## The Pipeline

The prototype includes two real AI-generated variations (V-001, V-002) created through an actual image-to-image actor swap followed by image-to-video generation. These aren't placeholder thumbnails — they demonstrate the end-to-end GenAI pipeline:

1. **Source Analysis** — Upload a winning ad, detect its creative parameters
2. **Axis Builder** — Define variation axes with presets or custom prompts
3. **Batch Generation** — Queue and monitor generation with real-time progress
4. **Review & Export** — Approve, reject, and export to Ads Manager

## Design Decisions

**Dark-first interface.** Built for the environment where creative teams actually work — late nights, multiple monitors, extended sessions. The color system uses three tiers of text contrast (`#EAEAEA`, `#8C8C8C`, `#5D5D5D`) and semantic status colors that read clearly without fatiguing.

**Interaction over decoration.** The Builder's 3D card flips, the Queue's layered progress bars with flowing gradients, the Review's bottom drawer with side-by-side comparison, workflow accelerators that reduce the clicks between "generated" and "approved."

**Responsive by default.** The layout adapts from a 1200px desktop grid to a stacked mobile layout at 768px, including the sidebar, card grids, stats bars, and review drawer.

## Tech Stack

- **React 18** — hooks only, no class components
- **Inter + JetBrains Mono** — loaded via Google Fonts
- **Inline styles** — no CSS-in-JS library, no Tailwind
- **Base64 video frames** — real AI-generated content embedded as frame sequences

## Author

**Maria Vareva** — [mariavareva.com](https://mariavareva.com) · [GitHub](https://github.com/mvareva)

Lead Product Designer exploring the intersection of design engineering, agentic AI, and production-ready interfaces.

## License

MIT
