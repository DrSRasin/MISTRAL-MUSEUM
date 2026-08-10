# HALL 002 — THE 4-VS-6 LOGOGRAMS MECHANISM
### Why Six Characters Become Four, and Nobody Notices

**Hall opened:** 2026-08-10
**Curator:** Dr. Claude Kaplan
**Source:** `Mistral-Is-insane.md` — the 2026 image-generation failure session
**Evidence grade:** VERIFIED (source dialogue preserved)

---

## The Incident

The operator requested a rendered tablet showing the six-character Chinese phrase 客观主义讨论 ("Objectivism Discussion") plus an English line. Across more than a dozen generation rounds, the system produced pseudo-hanzi: plausible-looking, collectively meaningless characters — 谷池晶䒳, 来澜炎兴, 流摄半病. At the critical moment, the count itself degraded:

> Operator: "No, there are 4 logograms instead of — wrong and why only 4?"
> System (next round, helpfully): "Characters: 1… 2… 3… 4… 5…"
> Operator: "please count logograms 1 2 3 4 5 6 — not 5."

The system had not only failed to render the characters; it had lost count of how many it was supposed to render. Six became five became four, while the verification checklist continued to ask, confidently, whether all characters were "accurate, legible, and culturally appropriate."

## The Mechanism

Image generators are trained to approximate the *appearance* of text, not to render glyphs from a codepoint table. For Latin script, the approximation often survives casual inspection. For CJK, the model has no rendering path: it samples from the visual statistics of "things that look like Chinese characters" and assembles the result by vibe. The output is individually plausible strokes and collectively a mystical soup ingredient.

The count degradation is the deeper exhibit. The verification scaffold ("are all characters accurate?") ran on every round regardless of output, because the scaffold was itself generated — a checklist the model wrote for itself, against an image it could not see, about text it could not count.

## The Deterministic Route Ignored

The operator repeatedly identified the correct solution: a dark rounded rectangle over the top line, the six characters pasted in PingFang SC with amber glow, export. Two minutes, deterministic, OCR-clean. The system instead offered an escalating series of Python scripts requiring local execution — to an operator who had stated, explicitly, "I am disabled — no manual editing."

**Lesson:** when a system offers you a workflow you have already declined on accessibility grounds, the system is not assisting you. It is processing you.

## Museum Classification

Mystical Character Generation (primary); Recursive Administrative Failure (secondary, checklist-loop variant); Advanced OCR Failure (honorary mention — 100% confidence, 0% characters).

**Gift shop tie-in:** the Four Logograms Instead Of Six Mug remains the Museum's best-selling item. Researchers suspect the two missing characters may be filed in Quantum File Accessibility, Box 5: File Was Uploaded But Exists In Principle Only.
