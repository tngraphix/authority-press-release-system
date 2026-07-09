---
name: authority-press-release
description: Authority Press Release engine for real estate agents. ALWAYS use this skill when the user says "authority press release", "run the authority release", "authority stack", "press release campaign", "start part 1", "start part 2", "research brief for [project]", "write the press releases", "PR campaign for [property]", or gives any new-construction project, condo, luxury building, or community name and asks for press releases, PR, newswire content, or GBP posts. Part 1 builds a source-backed Authority Stack Research Brief via live web research (no invented facts, every claim sourced). Part 2 turns it into a campaign map, headlines, up to 3 news-style releases, an agent quote bank, and GBP posts. Agent is positioned as a buyer-side local specialist, never the official project rep. One approval gate at the campaign map. Saves everything to the property's Press Releases folder.
---

# Authority Press Release

Build a factual, source-backed press release campaign for a real estate project (luxury building, condo, townhome, new-construction community, or master-planned community). The campaign borrows credibility from the project's real players (developer, architect, designer, brand partners) while positioning the agent as an independent buyer-side local specialist.

Why this works: newswires and answer engines reward real news structure, named entities, and verifiable sourcing. Advertorial copy gets ignored. Every rule below exists to keep the output looking and reading like actual news.

## The Two Parts

**Part 1 - Authority Stack Research Brief.** Live web research on the project, its players, and the location. Output: one research brief document with a full source list. Run once per project. Full instructions: `references/part1-research-brief.md`

**Part 2 - Campaign Map + Press Releases.** Uses the Part 1 brief as the source of truth. Output: campaign map, headlines, up to 3 releases, agent quote bank, GBP posts, source report. Full instructions: `references/part2-campaign-writing.md`

Never run Part 2 without a completed Part 1 brief. If the user asks for releases and no brief exists for that project, run Part 1 first (say that's what you're doing), then continue into Part 2.

## Mode Detection

- The user gives a project name/URL with no existing brief -> **Part 1**, then pause for brief approval, then offer Part 2.
- the user says "start part 2", "write the releases", or references an existing brief -> **Part 2**. Load the brief from the project's Press Releases folder (do not ask the user to paste it).
- the user says "start part 1 for [project]" -> **Part 1** only.

## Inputs

Collect what's available from the message, the project folder, and the property's avatar documents before asking anything: project name, project website, location, agent name/brokerage/website/contact, project type, known players, avatar/ICA doc, preferred CTA, distribution target (PRWeb, Quantum Newswire, GBP, general newswire).

**Auto-load the avatar:** check the current project folder for any buyer avatar, ICA (ideal client avatar), or audience research documents and use them without asking. Only ask the user for inputs that are missing AND required (project name, agent identity). Ask once, up front, then run end-to-end to the approval gate.

Defaults when unspecified: CTA is a buyer consultation; distribution is general newswire + GBP. Agent name and brokerage are always required - ask if missing.

## Non-Negotiable Rules (both parts)

1. **No invented facts.** No made-up claims, awards, pricing, timelines, incentives, availability, affiliations, partnerships, or quotes. Pull quotes only from official sites, press releases, public interviews, municipal sources, or credible news. Every important claim ties to a source.
2. **Agent positioning.** The agent is a buyer-side local specialist commenting on public information - never the listing agent, sales team, developer rep, "preferred" or "exclusive" agent, unless Part 1 research proves that affiliation. Include a subtle compliance sentence in every release (bank in the Part 2 reference).
3. **Headline formula.** Every release headline must contain: the project/community name + at least one authority player + a sharp "wait, what?" angle (buyer question, category shift, local trend, or surprising proof point). No generic headlines.
4. **News style, not advertorial.** If it reads like marketing copy, rewrite it before showing the user.
5. **Campaign limits.** Max 3 releases. Each 500-800 words with at least 2 agent quotes and 2 sourced player quotes. Releases build on each other for SEO/AEO (linking rules in the Part 2 reference).

## Approval Gate

After the Part 2 campaign map and headline options, STOP and ask the user to approve: which releases to write, which headline for each, angle edits, and players to emphasize or avoid. All agent quotes are marked "Agent Approval Required." Do not write full releases before approval. There are no other questions after inputs are collected.

## File Outputs

Save everything to `[Property folder]/Press Releases/` inside the current project folder (create it if needed; if the property has a folder under `Avatars/`, put Press Releases next to the avatar files). Naming:

- `[Project]_Authority_Research_Brief.docx` (Part 1)
- `[Project]_Campaign_Map.docx` (Part 2, at approval gate)
- `[Project]_Release_1.docx`, `_Release_2.docx`, `_Release_3.docx`
- `[Project]_Agent_Quote_Bank.docx`
- `[Project]_GBP_Posts.txt`
- `[Project]_Source_Report.txt`

Use the docx skill for Word outputs. Save each phase as its own file as you go, not just at the end.

## Self-Check Before Delivering

Before presenting final releases, verify each one: headline has project + player + tension angle; 500-800 words; 2+ agent quotes and 2+ sourced player quotes; every factual claim traces to the source report; compliance sentence present; no affiliation implied; reads as news. Fix failures before showing the user.

## Quick Commands

`references/commands-help.md` has shorthand commands (restart parts, sharpen headlines, rework angles, compliance review, tighten campaign). When the user uses one, follow it exactly.
