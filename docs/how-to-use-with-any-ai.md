# How to Use the Authority Press Release System in Your Favorite AI Tool

This system works in any capable AI chat tool: Claude, ChatGPT, Gemini, Perplexity, Copilot, or anything similar. You do not need to be technical. You copy, paste, and answer questions.

## What you'll need

1. The two prompt files from this repo's `prompts/` folder:
   - `part1-research-brief.txt` (the research prompt)
   - `part2-campaign-writing.txt` (the writing prompt)
2. Your project info: project name and website, your name and brokerage, your contact info, and your preferred call to action.
3. Optional but powerful: a buyer avatar or ideal-client description. Even one paragraph about who buys at this project makes the campaign sharper.

## The golden rule

Run Part 1 before Part 2, always. Part 1 does the research and builds a source list. Part 2 writes the campaign using ONLY what Part 1 found. If you skip Part 1, the AI will make things up, and made-up facts in a press release can hurt you.

## Step-by-step: any AI chat tool

### Step 1: Run the research prompt

1. Open your AI tool and start a new chat. If your tool has a web-search or browsing option, turn it on. Part 1 needs live web access to find real sources.
2. Open `prompts/part1-research-brief.txt`, copy the whole thing, and paste it into the chat.
3. The AI will ask for your project details. Answer them.
4. Let it work. You'll get an "Authority Stack Research Brief" with 10 sections and a source list.
5. Review it. Check the source list. Click a few links. If something looks invented or a source is missing, say: "Remove or flag any claim that does not have a real source."
6. Save the brief somewhere you can find it (copy it into a doc, or download it).

### Step 2: Run the campaign prompt

1. Start a new chat (fresh context works best).
2. Copy all of `prompts/part2-campaign-writing.txt` and paste it in.
3. Then paste your entire Part 1 brief below it.
4. The AI will give you a campaign map and headline options, then STOP and ask for your approval. This stop is on purpose. Do not let it skip ahead.
5. Approve with a message like: "Approved. Write releases 1-3 using headlines 1A, 2A, 3A."
6. You'll get the final releases, an agent quote bank, Google Business Profile posts, and a source report.

### Step 3: Before you publish

- Read every quote attributed to you. Edit them until they sound like you. They are drafts, not your words yet.
- Check the compliance sentence is in every release (it says you're an independent local buyer resource).
- Verify current pricing, availability, and dates directly. Projects change faster than articles do.
- Run the release through your broker or compliance review if your brokerage requires it.

## Tool-specific tips

**Claude (claude.ai, Claude Desktop, or Cowork):** best experience. Install the `authority-press-release.skill` file from this repo (download it, then add it as a skill in Settings > Capabilities). Then just type "authority press release for [Project Name]" and it runs the whole workflow, saves the files, and stops at the approval gate automatically.

**ChatGPT:** paste the prompts as described above. Make sure web browsing is enabled for Part 1. You can also create a Custom GPT: paste the Part 1 prompt as the instructions of one GPT and the Part 2 prompt as another.

**Gemini:** works the same way. Gemini has live Google access, which helps Part 1. Double-check the source list carefully - always confirm the links are real.

**Perplexity:** strong for Part 1 because search is built in. Run Part 1 there, copy the brief, then run Part 2 in the same or another tool.

**Any other tool:** if it can search the web and handle a long prompt, it can run this system. If it cannot search the web, do not use it for Part 1 - research without live sources is guessing.

## Quick commands

Once you're running the system, use the shorthand in `docs/quick-commands.md` to steer it: approve headlines, ask for sharper ones, rework an angle, tighten the campaign, or run a compliance pass.

## Common mistakes to avoid

1. Skipping Part 1 and asking the AI to "just write a press release." You'll get hype with invented facts.
2. Letting the AI call you the listing agent or the project's representative. You are an independent buyer-side local specialist unless you can prove otherwise.
3. Publishing AI-drafted quotes without editing them. Approve every quote personally.
4. Blending anecdotes with statistics. Keep "a realtor said" claims separate from closed-transaction data.
5. More than 3 releases per project. More is not better - newswires and answer engines reward focused, source-backed campaigns.
