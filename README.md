# humanize-text

A Claude Code plugin that makes AI-generated text sound like a developer wrote it. Not by banning 90 words, but by giving Claude reference samples of good writing to mimic.

**Zero token cost when you're not writing text.** The rules only load when Claude writes user-facing content or when you run `/humanize`.

## Install

```bash
/plugin marketplace add Rmalnoult/humanize-text
/plugin install humanize-text
```

## How it works

Most "humanize AI text" approaches ship a giant ban list: don't say "delve", don't say "leverage", don't use em dashes. Research shows this [backfires](https://medium.com/@scott_waddell/how-i-got-claude-and-chatgpt-to-stop-being-sycophantic-cheerleaders-7ab0b06f3111). Telling an LLM "never use X" primes it to think about X.

This plugin takes a different approach. It gives Claude writing samples from [Taylor Otwell](https://x.com/taylorotwell) and [Jeffrey Way](https://x.com/jeffrey_way) as reference voices and says "write like this." LLMs are much better at mimicking a style than following negative constraints.

It still has a short list of mechanical rules (contractions, sentence case, no em dashes) because those are binary and don't backfire. But the core is examples, not bans.

## What it covers

- **Reference voice samples** from Taylor Otwell and Jeffrey Way, with annotations explaining what makes each sample work
- **Three before/after examples** showing AI text rewritten as human text
- **Mechanical rules**: contractions always, sentence case headings, no em dashes
- **The Slack test**: would a developer say this in a Slack message? If no, rewrite it
- **Structural habits**: prose over bullets, specific over vague, have opinions, acknowledge trade-offs
- **SEO basics** for blog posts and landing pages

## Why these writers

Taylor Otwell writes short, direct, first-person sentences. No filler. He says "I'm not going anywhere" not "rest assured that leadership continuity remains a priority."

Jeffrey Way writes conversationally, starts sentences with "And" and "But", tells stories instead of listing features, and uses natural filler like "kind of" and "sort of." Nobody would flag his writing as AI.

Both write like developers talking to developers. That's the target.

## Customize

Fork the repo and swap in your own reference voice samples. Find 2-3 paragraphs of writing you like, paste them in, and annotate what makes them work. That's more effective than any ban list.

## Repo structure

```
.claude-plugin/
  marketplace.json          # makes this repo a plugin marketplace
plugins/
  humanize-text/
    .claude-plugin/
      plugin.json           # plugin metadata
    skills/
      humanize/
        SKILL.md            # voice samples + rules + /humanize command
```
