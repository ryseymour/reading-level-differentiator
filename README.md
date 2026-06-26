# Reading-Level Differentiator

A free AI Skill that rewrites a classroom passage at multiple reading levels, keeps the key vocabulary and meaning intact at every level, and hands you a short checklist of what to verify before you use it.

Built for the teacher who has one text and a class that reads at five different levels. Works across subjects: science, social studies, civics, any reading you hand students. (It is a general differentiation tool, not a reading-instruction program.)

This tool is introduced in the Substack post [A Passage for All Readers](https://ryseymour.substack.com/p/a-passage-for-all-readers).

## What it does

- Takes a passage, your target levels (grade bands, Lexile, or guided-reading), and any must-keep vocabulary.
- Returns one version per level, filled into your worksheet format if you give it one.
- Scaffolds key terms instead of deleting them, so a lower level still teaches the same concept.
- Handles EAL/multilingual and SEN needs differently, because they are different jobs.
- Appends a "Check before you use this" block. You decide whether each version fits your students.
- Writes plainly. No em-dashes, no chatbot tells.

## The method: Brief, Build, Check

1. **Brief** the model on your own template and content.
2. **Build** the leveled versions in that format.
3. **Check.** You verify the facts and the fit. The tool drafts. You decide.

## How to use it

This is a Claude Skill (a `SKILL.md` file Claude reads as instructions).

- **Claude Code:** download this repo and drop the folder into `~/.claude/skills/`.
- **Claude app / Projects:** add `SKILL.md` to a Project's knowledge, or paste it in.

Then just ask, for example:

> Level this passage for grades 4, 6, and 8. Keep the terms photosynthesis, chlorophyll, and glucose. Here is my worksheet format: Title / Passage / Glossary / 2 questions.

## Example

See [`examples/photosynthesis.md`](examples/photosynthesis.md) for a full input and output.

## A note on reading levels

No AI can output a *validated* Lexile or Fountas and Pinnell level. Lexile is a proprietary measure; Fountas and Pinnell is assigned by a teacher watching a child read. This skill aims at your target through sentence length, vocabulary, and syntax, and it reminds you to spot-check with your own tool. Being honest about that limit is the point.

## Feedback

Tried it with a class? Tell me how it went: **[share 1-minute feedback](https://docs.google.com/forms/d/e/1FAIpQLSc0LG3JEm_2PCY18Zf730smPIEi8_jNwCVoUVjaQdL2RpE5Lg/viewform)**. What worked, what broke, and what you would want next. It shapes the next version.

## Who made this

Built by Ryan Seymour, Seymour Learning Insights. Practical AI for high-impact learning, from someone who taught the class and shipped the tools at scale.

- Site: https://seymourlearning.com
- Writing: https://ryseymour.substack.com

MIT licensed. Use it, fork it, adapt it to your school.
