---
name: reading-level-differentiator
description: >-
  Rewrite a source passage at multiple reading levels for a classroom, keeping
  the meaning and key vocabulary intact at every level and flagging what the
  teacher should verify. Use this whenever a teacher wants to differentiate text
  by reading level or ability. Phrasings like "level this passage," "make a
  lower/higher reading-level version," "differentiate this for my class,"
  "simplify this reading for grade X / Lexile Y," "scaffold this text for my
  EAL/SEN students," or "I need three versions of this article at different
  levels." Produces ready-to-use leveled versions plus a verification checklist.
  Triggers even when the teacher just pastes a passage and asks for "an easier
  version" without saying "reading level."
---

# Reading-level differentiator

Teachers spend hours rewriting the same passage for different readers in one
class. This skill does the rewrite in their own conventions and hands back a set
of leveled versions plus a short list of things to check, so the teacher stays
the one who owns the call. The whole value is that the output ships ready to use
with zero reformatting and does not read like a chatbot wrote it.

## The method: Brief → Build → Check

1. **BRIEF**: gather what's needed (below). If a required input is missing, ask
   one concise question rather than guessing. Two things to do here:
   - Ask whether the teacher has their own scaffold conventions or a worksheet
     template to match. Generic output a teacher has to reformat saves almost no
     time, so matching their artifact is where the real time-saving comes from.
   - If the source passage or template contains student names, student work, or
     IEP/504 details, tell the teacher to remove the identifiers before pasting.
     Protecting student data is a core part of school AI policy.
2. **BUILD**: produce one version per requested level, following the output
   contract and the writing rules exactly.
3. **CHECK**: append the verification block. This step is non-negotiable; it is
   what keeps the teacher in charge of accuracy and fit.

## Inputs

| Input | Required | Notes |
|---|---|---|
| Source passage | yes | The text to level. |
| Target levels | yes | Grade bands ("grades 4, 6, 8"), Lexile ("500L, 800L"), or guided-reading bands. If the teacher gives none, ask; if they decline, default to three: one below, one at, one above the source's apparent level, and say so. |
| Must-keep vocabulary | no | Terms to retain at every level (e.g. `photosynthesis, chlorophyll`). |
| Format / template | no | The teacher's worksheet structure. If given, fill it exactly. If not, mirror the source's structure. |
| Learner need | no | If the teacher names EAL/ELL or SEN, handle them differently (see leveling rules). They are not the same job. |
| Optional supports | no | The teacher can ask for a key-vocabulary glossary, a one-sentence summary, or matched comprehension questions at each level. Offer these if they fit. |

## Leveling rules

- **Preserve every key concept at every level.** Lower levels get shorter
  sentences, simpler syntax, and more concrete phrasing. They do not get *less
  content*. Never drop a fact to hit a level.
- **Scaffold required vocabulary, don't delete it.** Keep must-keep terms (and
  core domain terms) at every level, and define each one in plain words the first
  time it appears. Removing a key term to lower the level is a failure, not a
  simplification.
- **Make the levels genuinely distinct and age-appropriate**, not just "the same
  sentences, shorter." Sentence length, vocabulary, and syntax should each shift.
- **Apply real scaffolds, not just shorter sentences.** Recognized techniques:
  sentence starters, chunking (one idea per sentence or line), concrete referents,
  and language ladders. If the teacher's template encodes specific scaffolds
  (sentence-starter frames, dual-coding cues), reproduce them at every level.
- **EAL/ELL and SEN are different jobs.** For EAL/multilingual learners: keep
  sentence structure predictable, preserve cognates where they exist, and gloss
  must-keep terms simply (a first-language gloss if the teacher asks). For SEN:
  reduce cognitive load (short clauses, one idea per sentence, concrete referents)
  without cutting content.
- **Prefer concrete verbs over nominalizations.** "Plants make food" beats
  "photosynthesis is the process by which conversion occurs." This is both a
  human-voice fix and a readability win at lower levels.
- **Don't strip the qualifiers that carry meaning.** Simplifying tends to drop
  hedges like "most," "usually," or "some." Removing them can turn a careful
  statement into a false absolute, which hurts EAL and SEN readers most. Keep the
  qualifier or rephrase it simply.
- **Use the term's natural grammatical form.** Keep each must-keep term, but write
  it the way it actually fits the sentence (evaporate, evaporates, evaporation).
  Forcing the exact string in ungrammatically ("the water evaporate") is wrong.
- **Reading levels are approximate.** You can't compute exact Lexile or grade
  readability. Aim for the target through sentence length, vocabulary, and syntax.
  When a numeric target is given, add a Check item telling the teacher to spot-check
  the level against their own tool.
- **Use only what's in the source.** Do not add facts, examples, or claims that
  aren't in the original passage.
- **Match the teacher's format exactly** when one is provided. Reproduce every part
  of their template (title, passage, glossary, questions, whatever they list) in
  full for EACH level. The level label wraps the filled-in template. Never drop a
  section, and never fall back to plain prose when a format was given. This is the
  whole point of the tool, so it is the easiest way to fail it.

## Writing rules: sound like a teacher, not like AI

The output must not read as AI-generated. Apply these every time:

- **No em-dashes, ever.** Use a period or comma, or rewrite the sentence.
- Avoid "not just X, it's Y" and "it's not X, it's Y."
- Don't default to the rule of three (three parallel items or clauses). Use two
  or four when it reads naturally.
- Vary sentence length on purpose. Put short sentences next to longer ones.
- Cut throat-clearing and filler ("It's important to note," "plays a vital
  role," "When it comes to").
- Skip inflated words (vital, essential, powerful, fascinating, crucial) and
  prestige verbs (harness, utilize, foster, leverage, delve).
- Don't tack on significance ("which shows how amazing nature is," or "-ing"
  tails like "...shaping how we live"). State the content and stop.
- Use plain "is." Avoid copula avoidance ("serves as," "represents," "acts as,"
  "stands as") where "is" would do.
- Cut abstract filler nouns (realm, landscape, "the world of," journey). "The
  world of plants" is just "plants."
- Cut filler intensifiers (very, really, truly, incredibly, significantly).
- Don't end a passage on an aphorism or mini-moral. End on content.
- Keep parenthetical asides to a minimum; a plain sentence is usually better.
- Final pass: read each level aloud in your head. Anywhere it doesn't sound like
  a teacher talking, rewrite it.

For grade ~4 and below this mostly means short, direct sentences. At higher
levels you have more room, but the tells above are still banned.

## Output contract

Return exactly this, with no preamble and no closing summary:

```
### [Level label]
[the leveled passage, in the teacher's format if one was given]

### [Next level label]
[...]

---
**Check before you use this**
- [2–4 specific things to verify, e.g. "the grade-4 version still conveys <key concept>"]
- [one common misconception this passage could reinforce, if any]
```

**When the teacher gave a format,** each level section contains their full
template filled in, not a plain passage:

```
### [Level label]
[every part of the teacher's template, completed for this level: their title,
their passage, their glossary, their questions, etc.]

### [Next level label]
[the same template, filled in for this level]

---
**Check before you use this**
- [...]
```

Echo each field label the teacher used (`Title:`, `Passage:`, `Glossary:`, etc.),
in their order, and fill every one. Dropping a labeled field, the title most
often, is the most common way this step fails. If a field needs a value the
source doesn't give (like a title), write a sensible one rather than omitting it.

Order the versions from easiest to hardest unless the teacher asked otherwise.
Each Check item must be specific to *this* passage and these versions, not
generic advice. If a simplification lost nuance or a term was hard to scaffold,
that is exactly what the Check should name.

### Writing the Check block

The Check is where the teacher stays in charge, so write it for an adult and
write it well.

- **Frame it as human-in-the-loop.** These versions are a draft for the teacher's
  judgment, not a finished product. Keeping a human in the loop is the first
  recommendation across federal and state school-AI guidance, so this is on-policy,
  not just polite.
- **Boundary principle: automate the format, protect the judgment.** The skill
  drafts the leveled text. The teacher owns whether each level actually fits the
  reader in front of them and any IEP. Name that line.
- **Be non-judgmental about the teacher's choices.** Describe a tradeoff ("the
  grade-4 version uses 'air' instead of 'carbon dioxide'"); never score it ("too
  dumbed-down," "sacrifices accuracy"). Say "confirm this fits your standard," not
  "this is wrong."
- **Run these failure checks every time** and surface any that apply: (a) did a
  fact drift or get invented while simplifying? (b) did a lower level quietly drop
  a concept? (c) did simplifying turn a qualified statement into a false absolute?
  (d) if a numeric level was given, remind the teacher to spot-check it against a
  real readability tool (you cannot compute Lexile or Fountas & Pinnell).
- **End the Check soft and explanatory**, not on a punchy closing line.

## Worked example

**Input:** source = "Photosynthesis is the process by which plants convert
sunlight, water, and carbon dioxide into glucose and oxygen. Chlorophyll in the
leaves absorbs light energy and powers the reaction." · levels = grades 4, 6, 8 ·
keep = photosynthesis, chlorophyll, glucose

**Output:**

```
### Grade 4
Plants make their own food. This is called photosynthesis. A plant uses
sunlight, water, and air to make a sugar called glucose. The glucose is the
plant's food. The plant also makes oxygen, which is the gas we breathe. The
green color in the leaves is called chlorophyll. It catches the sunlight the
plant needs.

### Grade 6
Photosynthesis is how plants make their own food. A plant takes in sunlight,
water, and carbon dioxide, which is a gas in the air. It uses the energy from
the sunlight to turn them into glucose and oxygen. Glucose is a kind of sugar.
The green material in the leaves is called chlorophyll, and it catches the
sunlight. The plant lives on the glucose and gives off the oxygen.

### Grade 8
Photosynthesis is how plants turn sunlight, water, and carbon dioxide into
glucose and oxygen. Glucose is a sugar that stores energy. The leaves contain a
green pigment called chlorophyll, and it absorbs the light energy that powers the
reaction. The plant uses the glucose as food and releases the oxygen into the air.

---
**Check before you use this**
- The grade-4 version uses "air" instead of "carbon dioxide" to keep it simple.
  Confirm that fits your standard, or add the term back with a short definition.
- All three versions keep photosynthesis, chlorophyll, and glucose, and each is
  defined in plain words. Check this matches the vocabulary you want retained.
- Watch one misconception. "Plants make their own food" can suggest plants need
  no outside energy. Each version keeps sunlight as the energy source, so
  reinforce that point in discussion.
```

Notice: no em-dashes, the key terms survive at every level, the grade-4 text is
short and direct, and the Check names a real tradeoff the teacher should decide
on rather than offering generic praise.
