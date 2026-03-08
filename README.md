# AI Marketing Suite for Claude Code

![Python](https://img.shields.io/badge/Python-3.6+-3776AB?logo=python&logoColor=white)
![Claude Code](https://img.shields.io/badge/Claude_Code-Skills_System-6B4FBB)
![License](https://img.shields.io/badge/License-MIT-green)
![ReportLab](https://img.shields.io/badge/ReportLab-PDF_Generation-FF6B35)

> A production-ready marketing analysis and automation skill system for Claude Code. Audit websites, generate copy, build email sequences, create content calendars, analyze competitors, and produce client-ready PDF reports — all from the terminal.

## Overview

The AI Marketing Suite installs 15 slash commands into Claude Code that transform it into a full-service marketing analysis platform. Each command triggers specialized skill definitions that guide Claude through structured, repeatable marketing workflows — from 60-second website snapshots to comprehensive multi-agent audits with scored deliverables.

The system is built for entrepreneurs, agency builders, and solopreneurs who want to deliver professional marketing services powered by AI. Every output is client-ready: scored, prioritized, and actionable. The full audit runs five parallel subagents simultaneously, each analyzing a different marketing dimension, then synthesizes results into a weighted overall score with revenue-impact estimates.

Originally created by [Zubair Trabzada](https://github.com/zubair-trabzada/ai-marketing-claude) and released under the MIT License. This fork is maintained by CushLabs for internal use and client delivery.

## The Challenge

Marketing audits are expensive and slow. A typical agency charges $2,000–$10,000 for a comprehensive website audit that takes 1–3 weeks to deliver. Solopreneurs and small agencies can't compete at that price point, and most skip the analysis entirely — jumping straight to tactics without understanding the full picture.

The gap isn't knowledge — it's process. The frameworks exist (CRO checklists, SEO scoring rubrics, competitive analysis templates), but executing them manually across content, conversion, SEO, competitive positioning, brand trust, and growth strategy takes dozens of hours per client.

## The Solution

This suite encodes proven marketing analysis frameworks into Claude Code skill definitions. Each skill contains the exact methodology, scoring criteria, and output format — so the analysis is consistent, comprehensive, and fast.

**Parallel multi-agent architecture:** The full audit launches five independent subagents simultaneously (content, conversion, technical, competitive, strategy), each scoring their dimension on a 0–100 scale. Results are synthesized into a weighted overall score with prioritized recommendations.

**Client-ready deliverables:** Every command outputs structured Markdown or professional PDF reports. Proposals include Good-Better-Best pricing, ROI projections, and follow-up sequences. Reports include before/after copy examples, competitor comparison matrices, and revenue impact estimates.

**Zero dependencies for core functionality:** The skill system runs entirely on Claude Code's native capabilities. Python scripts (stdlib only) handle automated page analysis. ReportLab is the sole optional dependency for PDF generation.

## Technical Highlights

- **Skill composition pattern:** 14 sub-skills + 1 orchestrator, each self-contained with execution steps, scoring criteria, and output format
- **Parallel subagent execution:** 5 independent agents run simultaneously during full audits, analyzing content, conversion, technical SEO, competitive positioning, and growth strategy
- **Weighted scoring methodology:** 6 dimensions weighted by marketing impact (Content 25%, Conversion 20%, SEO 20%, Competitive 15%, Brand 10%, Growth 10%)
- **Python page analyzer:** Custom HTML parser extracts 20+ marketing elements (meta tags, CTAs, forms, tracking pixels, schema markup) with quick scores for SEO, CTA effectiveness, trust signals, and analytics setup
- **PDF report generator:** ReportLab-based pipeline produces 5–7 page professional reports with score gauges, bar charts, severity-coded findings tables, and branded color scheme
- **Template library:** 6 ready-to-use templates for email sequences (welcome, nurture, launch), client proposals, content calendars, and launch checklists

## Getting Started

### Prerequisites

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) installed and configured
- Python 3.6+ (for page analysis and PDF generation scripts)
- Git (for cloning the repository)

### Installation

**One-command install:**

```bash
curl -fsSL https://raw.githubusercontent.com/RCushmaniii/cushlabs-ai-marketing/main/install.sh | bash
```

**Manual install:**

```bash
git clone https://github.com/RCushmaniii/cushlabs-ai-marketing.git
cd cushlabs-ai-marketing
./install.sh
```

**Optional — PDF report support:**

```bash
pip install reportlab
```

The installer copies skill definitions to `~/.claude/skills/` and agent definitions to `~/.claude/agents/`. No system-level changes are made.

### Uninstall

```bash
./uninstall.sh
```

## Commands

| Command | What It Does |
|---------|-------------|
| `/market audit <url>` | Full marketing audit with 5 parallel agents |
| `/market quick <url>` | 60-second marketing snapshot |
| `/market copy <url>` | Optimized copy with before/after examples |
| `/market emails <topic>` | Complete email sequences (welcome, nurture, launch) |
| `/market social <topic>` | 30-day social media content calendar |
| `/market ads <url>` | Ad creative and copy for all platforms |
| `/market funnel <url>` | Sales funnel analysis and optimization |
| `/market competitors <url>` | Competitive intelligence report |
| `/market landing <url>` | Landing page CRO analysis |
| `/market launch <product>` | Product launch playbook (8-week timeline) |
| `/market proposal <client>` | Client proposal with pricing and ROI projections |
| `/market report <url>` | Full marketing report (Markdown) |
| `/market report-pdf <url>` | Professional marketing report (PDF) |
| `/market seo <url>` | SEO content audit |
| `/market brand <url>` | Brand voice analysis and guidelines |

## Scoring Methodology

The full marketing audit scores websites across 6 weighted dimensions:

| Category | Weight | What It Measures |
|----------|--------|------------------|
| Content & Messaging | 25% | Copy quality, value props, headlines, CTAs |
| Conversion Optimization | 20% | Funnels, forms, social proof, friction, urgency |
| SEO & Discoverability | 20% | On-page SEO, technical SEO, content structure |
| Competitive Positioning | 15% | Differentiation, market awareness, alternatives |
| Brand & Trust | 10% | Design quality, trust signals, authority |
| Growth & Strategy | 10% | Pricing, acquisition channels, retention |

**Score interpretation:** A (85–100), B (70–84), C (55–69), D (40–54), F (0–39)

## Project Structure

```
cushlabs-ai-marketing/
├── market/                         # Main orchestrator skill
│   └── SKILL.md
├── skills/                         # 14 specialized sub-skills
│   ├── market-audit/SKILL.md       # Full audit orchestration
│   ├── market-copy/SKILL.md        # Copywriting analysis
│   ├── market-emails/SKILL.md      # Email sequence generation
│   ├── market-social/SKILL.md      # Social content calendar
│   ├── market-ads/SKILL.md         # Ad creative & campaigns
│   ├── market-funnel/SKILL.md      # Funnel analysis
│   ├── market-competitors/SKILL.md # Competitive intelligence
│   ├── market-landing/SKILL.md     # Landing page CRO
│   ├── market-launch/SKILL.md      # Launch playbook
│   ├── market-proposal/SKILL.md    # Client proposal generator
│   ├── market-report/SKILL.md      # Marketing report (MD)
│   ├── market-report-pdf/SKILL.md  # Marketing report (PDF)
│   ├── market-seo/SKILL.md        # SEO content audit
│   └── market-brand/SKILL.md      # Brand voice analysis
├── agents/                         # 5 parallel audit subagents
│   ├── market-content.md           # Content & messaging
│   ├── market-conversion.md        # CRO & funnels
│   ├── market-competitive.md       # Competitive positioning
│   ├── market-technical.md         # Technical SEO
│   └── market-strategy.md          # Brand & growth strategy
├── scripts/                        # Python utilities
│   ├── analyze_page.py             # Webpage marketing analysis
│   ├── competitor_scanner.py       # Competitor scanner
│   ├── social_calendar.py          # Calendar generator
│   └── generate_pdf_report.py      # PDF report generator
├── templates/                      # Marketing templates
│   ├── email-welcome.md            # Welcome sequence (5 emails)
│   ├── email-nurture.md            # Nurture sequence (6 emails)
│   ├── email-launch.md             # Launch sequence (8 emails)
│   ├── proposal-template.md        # Client proposal
│   ├── content-calendar.md         # 30-day calendar
│   └── launch-checklist.md         # Launch checklist
├── install.sh                      # One-command installer
├── uninstall.sh                    # Clean uninstaller
└── requirements.txt                # Python dependencies
```

## Results

This suite compresses what typically takes a marketing agency 1–3 weeks into minutes. A full 5-agent audit of any website produces a scored, prioritized report with specific copy recommendations, conversion fixes, SEO improvements, competitive positioning, and revenue impact estimates.

| Capability | Traditional Agency | AI Marketing Suite |
|------------|-------------------|-------------------|
| Full website audit | 1–3 weeks | Minutes |
| Client proposal | 2–5 hours | Minutes |
| Email sequence (5–8 emails) | 1–2 days | Minutes |
| 30-day content calendar | 3–5 hours | Minutes |
| Competitive analysis | 1–2 weeks | Minutes |

The output quality is consistent and repeatable because the analysis frameworks are encoded in the skill definitions — not improvised each time.

## Contact

**Robert Cushman**
Business Solution Architect & Full-Stack Developer
Guadalajara, Mexico

📧 info@cushlabs.ai
🔗 [GitHub](https://github.com/RCushmaniii) • [LinkedIn](https://linkedin.com/in/robertcushman) • [Portfolio](https://cushlabs.ai)

## License

MIT License — see [LICENSE](LICENSE) for details.

Based on [ai-marketing-claude](https://github.com/zubair-trabzada/ai-marketing-claude) by Zubair Trabzada.

---

*Last Updated: 2026-03-08*
