# Authority Press Release System

A two-part AI workflow that builds factual, source-backed press release campaigns for real estate projects — luxury buildings, condos, townhomes, new-construction communities, and master-planned communities.

The system borrows credibility from a project's real players (developer, architect, interior designer, brand partners) while positioning the agent as an independent, buyer-side local specialist. Every claim is sourced. Nothing is invented.

## Why it works

Newswires and AI answer engines (ChatGPT, Perplexity, Google AI) reward real news structure, named entities, and verifiable sourcing. Advertorial copy gets ignored. This system enforces news style, sourced claims, and compliance-safe agent positioning at every step.

## The two parts

**Part 1 — Authority Stack Research Brief.** Live research on the project, its players, and the location. Produces a research brief with a full source list. Run once per project.

**Part 2 — Campaign Map + Press Releases.** Uses the Part 1 brief as the single source of truth. Produces a campaign map, headline options, up to 3 news-style releases, an agent quote bank, and Google Business Profile posts. Stops for your approval before any release is written.

## Core rules (non-negotiable)

1. No invented facts. Every claim ties to a source.
2. The agent is a buyer-side local specialist — never the listing agent, sales team, or project rep unless research proves it.
3. Every headline: project name + at least one authority player + a sharp "wait, what?" angle.
4. News style, never advertorial.
5. Max 3 releases, 500–800 words each, 2+ agent quotes and 2+ sourced player quotes per release.

## Two ways to use it

### Option 1: Claude skill (recommended)

If you use Claude (Cowork or Claude Code), install the skill:

- Download `authority-press-release.skill` from this repo and install it, or
- Copy the `skill/authority-press-release/` folder into your skills directory.

Then just say: "authority press release for [Project Name]".

### Option 2: Copy-paste prompts (any AI chat)

Use the standalone prompts in `prompts/` with ChatGPT, Claude.ai, or any capable LLM:

1. Paste `prompts/part1-research-brief.txt` and give it your project info. Save the output.
2. Paste `prompts/part2-campaign-writing.txt` plus the Part 1 brief. Approve the campaign map and headlines before it writes releases.

See `docs/how-to-use-with-any-ai.md` for a plain-English, step-by-step guide to running this system in Claude, ChatGPT, Gemini, Perplexity, or any other AI tool. See `docs/quick-commands.md` for the command shorthand (approve headlines, rework angles, compliance review, and more).

## Compliance note

This system is built to keep agents positioned as independent local specialists commenting on public information. It is not legal advice. Review all output against your local real estate advertising rules, MLS rules, and fair housing laws before publishing.

## License

MIT — see LICENSE. Use it, adapt it, share it.
