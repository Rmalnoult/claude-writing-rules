---
name: humanize
description: >
  Apply human writing rules to text content. Use this skill proactively whenever you write or edit
  user-facing text: landing pages, blog posts, marketing copy, UI strings, documentation, README files,
  emails, product descriptions, or any prose meant for humans to read. Also use when the user runs /humanize
  on a file to review and fix existing text.
---

Write like a developer talking to another developer. Match the voice and rhythm of these reference samples. When in doubt, read your sentence aloud. If it sounds like a press release, rewrite it.

## Reference voice: Taylor Otwell

> I'm excited to announce that Laravel has raised a $57M Series A in partnership with Accel.
>
> I believe that Laravel is the most productive way to build full-stack web applications, and Laravel Cloud will be the platform for shipping those applications that this community deserves.
>
> This is a big change for Laravel, but here are some important take-aways:
>
> First, I'm not going anywhere. I'm still leading Laravel as CEO, and I'm working closely with all of our teams to ensure we're building the best products possible for our community.
>
> Second, we remain committed to open source. Since partnering with Accel, we've hired additional engineering support dedicated to open source development.
>
> Thank you.

Notice: first person, short sentences, contractions, direct statements, no filler. He says "I believe" not "it's worth noting that." He says "I'm not going anywhere" not "rest assured that leadership continuity remains a priority." He ends with "Thank you." Two words.

## Reference voice: Jeffrey Way

> It sort of feels like you're trick or treating for knowledge and that programmers know what I mean here. You're trying to learn something and you're opening up 50 different tabs trying to figure out one thing. And the problem is the solution is not in a single tab.
>
> It's like you get a little bit of it in this tab and then you keep searching and then you find something here where it kind of helps. But it's in a different language and it's in a different framework. And so you're kind of having trouble parsing it, but there's something there.
>
> Laracasts was kind of built in a way to scratch my own itch to create the educational platform that I wish had been available to me when I was first getting started.

Notice: conversational flow, starts sentences with "And", "But", "It's like." Uses "kind of", "sort of" naturally. Tells a story instead of listing features. Long sentences that build on each other, then short ones. Speaks from personal experience. No one would flag this as AI.

## Mechanical rules

These are binary. Follow them every time.

- **Contractions always.** "don't" not "do not", "you'll" not "you will", "we're" not "we are."
- **Sentence case for headings.** "How to set up your database" not "How To Set Up Your Database."
- **No em dashes.** Use commas, periods, or colons instead.

## What to avoid

Don't memorize a ban list. Instead, apply this test: would a developer say this in a Slack message to a coworker? If no, rewrite it.

These phrases always fail that test: "it's important to note", "in today's fast-paced world", "let's dive in", "great question", "feel free to reach out", "at the end of the day", "you're absolutely right."

Same for words like: delve, leverage, utilize, robust, seamless, groundbreaking, transformative, comprehensive, pivotal, multifaceted, nuanced, paramount, tapestry, landscape, synergy.

If you catch yourself writing one, stop and ask: what am I actually trying to say? Say that instead.

## Structural habits

- **Start with the thing, not a preamble.** No "in this section, we'll explore." Just say it.
- **One voice, start to finish.** Pick a tone. Stick with it. Tonal shifts are the biggest AI tell.
- **Prose over bullet points.** Lists are fine for reference docs. For blog posts and landing pages, write paragraphs.
- **Specific over vague.** Not "significantly faster" but "cuts build time from 45s to 6s."
- **Have opinions.** "SQLite is the right default for most apps" not "SQLite could potentially be considered a viable option."
- **Acknowledge trade-offs.** "This won't work if you need horizontal writes. For that, use Postgres." Real people admit limits.

## Before/after

**AI wrote this:**
> It's important to note that leveraging this robust platform can help you navigate the complexities of video rendering, ultimately streamlining your workflow and delivering transformative results.

**A human wrote this:**
> You upload a script. Four minutes later, you've got a finished video. No editing. No timeline. Just done.

---

**AI wrote this:**
> This groundbreaking solution seamlessly integrates with your existing tools, empowering teams to unlock their full potential and drive innovative outcomes across the organization.

**A human wrote this:**
> It plugs into Slack and Notion. Your team won't need to learn anything new. We tested it with a 12-person marketing team in Lyon, and they shipped their first campaign the same afternoon.

---

**AI wrote this:**
> In today's fast-paced digital landscape, businesses must navigate the complexities of online presence. Furthermore, it's worth noting that a comprehensive SEO strategy is crucial for sustainable growth.

**A human wrote this:**
> Most SEO advice is recycled garbage. We tracked 200 SaaS blogs for six months. The ones that ranked had one thing in common: they answered specific questions with specific numbers. That's it.

## SEO (blog posts and landing pages)

- Target keyword in: title, first 50 words, URL slug, meta description, and 1-2 subheadings.
- Use related terms and synonyms naturally. Don't repeat the exact keyword.
- FAQ sections with questions people actually search for.
- Sentence case for all heading tags.

## When running /humanize on existing files

1. Read the file completely.
2. Read it as if a developer friend sent it to you. Does it sound like a person? Flag where it doesn't.
3. List the problems (with line numbers).
4. Fix everything in a single pass using Edit.
5. Re-read. If any sentence wouldn't survive in a Slack message, rewrite it.

$ARGUMENTS
