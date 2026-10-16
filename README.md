# Local Business Website Skill

An agent skill (Claude / Cursor / any SKILL.md-compatible agent) for finding well-reviewed local service businesses with **broken, outdated, non-mobile or missing websites**, verifying the problem, building an **honest mobile-first preview site** from their real public info, and preparing a **voice note + Loom pitch** and **setup + monthly pricing**.

**Created by [Katlego Mokwena](https://github.com/black-abys)** of CortexLab (cortexlab.co.za).
Inspired by a Christian | WTC Instagram reel about pitching AI-built websites to local businesses.

## What it does
1. Finds leads (rating ≥ 4.3 with a decent review count) from public sources
2. Fetches each site and records a concrete, verified problem
3. Builds static previews with click-to-call, WhatsApp and a sticky mobile call bar
4. Drafts a voice-note script, a 60–90 s Loom script, one follow-up text and pricing

## Built-in ethics
- Real, verified data only; no fake reviews, testimonials or claims; gaps marked `[placeholder]`
- No copyrighted photos
- Never claims affiliation; previews are labelled concept previews and `noindex`
- The human approves and sends every message; the agent never contacts anyone
- Respects anti-spam and privacy law (POPIA/ECTA, GDPR, CAN-SPAM, CASL...): public business contacts only, opt-out, one follow-up max

## Install
Copy the `local-business-website/` folder into your skills directory:
- Claude Code: `~/.claude/skills/` (or `.claude/skills/` in a project)
- Cursor: your project's or user skills folder

```bash
git clone https://github.com/black-abys/local-business-website-skill
cp -r local-business-website-skill/local-business-website ~/.claude/skills/
```

Then ask your agent: *"Find 20 local businesses in <area> with good reviews and bad websites, and build previews for the best 3."*

## Files
- `local-business-website/SKILL.md`: the skill
- `local-business-website/assets/preview-template.html`: starter mobile preview template

## License
MIT © 2026 Katlego Mokwena
