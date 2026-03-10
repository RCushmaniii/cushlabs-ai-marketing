---
# =============================================================================
# PORTFOLIO.MD — AI Marketing Suite
# =============================================================================
portfolio_enabled: true
portfolio_priority: 3
portfolio_featured: true
portfolio_last_reviewed: "2026-03-09"

title: "AI Marketing Suite for Claude Code"
tagline: "15 slash commands that turn Claude Code into a full-service marketing analysis platform"
slug: "ai-marketing-suite"

category: "AI Automation"
target_audience: "Entrepreneurs, agency builders, and solopreneurs delivering AI-powered marketing services"
tags:
  - "claude-code"
  - "marketing-automation"
  - "ai-agents"
  - "seo-audit"
  - "competitive-analysis"
  - "copywriting"
  - "email-marketing"
  - "content-calendar"
  - "pdf-reports"
  - "parallel-agents"

thumbnail: "/images/portfolio/cushlabs-ai-marketing-thumb.webp"
hero_images:
  - "/images/portfolio/cushlabs-ai-marketing-01.webp"
  - "/images/portfolio/cushlabs-ai-marketing-02.webp"
  - "/images/portfolio/cushlabs-ai-marketing-03.webp"
  - "/images/portfolio/cushlabs-ai-marketing-04.webp"
  - "/images/portfolio/cushlabs-ai-marketing-05.webp"
  - "/images/portfolio/cushlabs-ai-marketing-06.webp"
  - "/images/portfolio/cushlabs-ai-marketing-07.webp"
  - "/images/portfolio/cushlabs-ai-marketing-08.webp"
  - "/images/portfolio/cushlabs-ai-marketing-09.webp"
  - "/images/portfolio/cushlabs-ai-marketing-10.webp"
  - "/images/portfolio/cushlabs-ai-marketing-11.webp"
demo_video_url: "/video/cushlabs-ai-marketing-brief.mp4"
demo_video_poster: "/video/cushlabs-ai-marketing-brief-poster.webp"

live_url: ""
demo_url: ""
case_study_url: ""

problem_solved: |
  Marketing audits are expensive ($2K–$10K) and slow (1–3 weeks). Small agencies and solopreneurs
  can't compete at that price point. The frameworks exist — CRO checklists, SEO rubrics, competitive
  analysis templates — but executing them manually across six marketing dimensions takes dozens of
  hours per client. This suite encodes those frameworks into repeatable, scored Claude Code skills.

key_outcomes:
  - "15 marketing commands available as Claude Code slash commands"
  - "Full website audit with 5 parallel subagents running simultaneously"
  - "Weighted scoring across 6 dimensions with revenue impact estimates"
  - "Client-ready PDF reports with score gauges, charts, and branded styling"
  - "Complete email sequences, ad campaigns, and 30-day content calendars generated in minutes"

tech_stack:
  - "Claude Code Skills System"
  - "Python 3"
  - "Bash"
  - "ReportLab"
  - "HTML Parser (stdlib)"

complexity: "Production"
---

## Overview

The AI Marketing Suite installs 15 slash commands into Claude Code that transform it into a full-service marketing analysis platform. Each command triggers specialized skill definitions that guide Claude through structured, repeatable marketing workflows — from 60-second website snapshots to comprehensive multi-agent audits with scored deliverables.

The system is built around a skill composition pattern: one main orchestrator routes `/market <command>` invocations to 14 specialized sub-skills. The full audit launches five independent subagents in parallel, each analyzing a different marketing dimension (content, conversion, technical SEO, competitive positioning, growth strategy). Results are synthesized into a weighted overall score with prioritized, revenue-focused recommendations.

Originally created by Zubair Trabzada and released under the MIT License. This fork is maintained by CushLabs for internal use and client delivery.

## The Challenge

- **Cost barrier:** Traditional marketing audits cost $2,000–$10,000 and take weeks to deliver, pricing out small agencies and solopreneurs
- **Consistency problem:** Manual audits vary wildly in quality depending on who performs them and what they remember to check
- **Framework execution gap:** The analysis frameworks exist (CRO checklists, SEO scoring rubrics, competitive matrices), but executing them comprehensively across content, conversion, SEO, competitive positioning, brand trust, and growth strategy takes 20–40 hours per client
- **Deliverable quality:** Most quick analysis tools produce generic output that isn't client-ready — no scoring, no prioritization, no revenue impact estimates

## The Solution

**Encoded frameworks, not improvised analysis:**
Every skill definition contains the exact methodology, scoring criteria, benchmarks, and output format for its domain. The analysis is consistent because the process is codified — not dependent on what Claude happens to think of in the moment.

**Parallel multi-agent architecture:**
The full audit runs five subagents simultaneously, each independently scoring their dimension on a 0–100 scale. This produces deeper analysis than a single-pass approach while completing faster.

**Client-ready output:**
Every command produces structured deliverables designed for direct client delivery. Proposals include Good-Better-Best pricing, ROI projections, and follow-up sequences. Reports include before/after copy examples, competitor comparison matrices, and prioritized action plans.

**Zero-friction deployment:**
One-command install copies skill definitions to `~/.claude/skills/` and agent definitions to `~/.claude/agents/`. No configuration, no API keys, no external services. Python scripts use stdlib only — ReportLab is the sole optional dependency for PDF generation.

## Technical Highlights

- **Skill composition pattern:** 14 sub-skills + 1 orchestrator, each self-contained with execution steps, scoring criteria, and output format specifications
- **Parallel subagent execution:** 5 independent agents analyze content, conversion, technical SEO, competitive positioning, and growth strategy simultaneously during full audits
- **Weighted scoring methodology:** 6 dimensions weighted by marketing impact, with letter-grade interpretation and benchmark comparisons
- **Custom HTML parser:** Python script extracts 20+ marketing elements from any webpage with quick scores for SEO, CTAs, trust signals, and analytics setup
- **PDF report pipeline:** ReportLab-based generator produces branded 5–7 page reports with score gauge visualizations, bar charts, and severity-coded findings tables

## Results

**For the End User:**
- Full website marketing audit completed in minutes instead of weeks
- Consistent, scored analysis across 6 dimensions for every client
- Client-ready deliverables (Markdown and PDF) that require no additional formatting
- Complete email sequences, ad campaigns, and content calendars generated on demand

**Technical Demonstration:**
- Multi-agent orchestration with parallel execution and result synthesis
- Framework-driven analysis design that produces repeatable, measurable output
- Skill system architecture that scales by adding new skill definitions without modifying existing code
