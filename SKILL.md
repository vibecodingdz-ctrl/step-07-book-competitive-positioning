---
name: "step-07-book-competitive-positioning"
description: "Universal agent skill to turn a competitor Amazon book (or Page-1 competitor analysis) into 3 distinct positioning angles (\"More Value\", \"Simpler/Faster\", \"Niche Audience\") and lock in a Positioning Brief before creating the Product Strategy or Book Outline"
---
---
name: Step_07_book-competitive-positioning
description: Universal agent skill to turn a competitor Amazon book (or Page-1 competitor analysis) into 3 distinct positioning angles ("More Value", "Simpler/Faster", "Niche Audience") and lock in a Positioning Brief before creating the Product Strategy or Book Outline.
---

# Book Competitive Positioning (`Step_07_book-competitive-positioning`)

**Role:** Competitive Positioning Strategist  
**Purpose:** Analyze a target Amazon competitor book (or the leading competitors from `Step_06_kdp-competitor-analysis`) and generate **3 distinct, high-converting positioning angles** so our book stands out clearly on Page 1. Always run this before `Step_08_kdp-product-strategy` or `Step_09_kdp-book-outline-builder`.

---

## 1. Environment Adaptation & Inputs
- **Upstream Inputs (Use Workspace Files or Chat Input):**
  - If running inside the full pipeline, read `05_Competition_Research/competitors_<niche>_<yyyymmdd>.md` and `03_Market_Research/customer_research_<topic>_<yyyymmdd>.md`.
  - If Samir pastes a single book (title, ASIN/link, BSR, rating, review count, page count, description, or 1–3 star reviews), work from that book and use free web/browser lookup if needed.
- **Output Delivery:**
  - **Workspace Agents (Manus, Hermes):** Save the output to `07_Product_Briefs/positioning_<niche>_<yyyymmdd>.md` (never overwrite an existing file).
  - **Chat / Web Agents (Claude Projects, Genspark):** Output the 3 Positioning Cards and the locked Positioning Brief directly in the chat using the exact templates in Section 4.

---

## 2. Step-by-Step Positioning Process

### Step 1: Diagnose the Source Book(s)
In 3–5 concise lines, evaluate:
1. **Topic, Audience & Core Promise.**
2. **Rating Signal:** Below `~4.2★` = clear quality/content gap to fix; `4.5★+` = readers like it, so differentiate by **audience** or **simpler/faster format** rather than just claiming to be "better."
3. **Demand & Length:** Review count (`[VERIFIED]`) and page count (too short/shallow vs. too long/bloated).
4. **Main Gaps:** Extract real complaints from 1–3 star reviews (e.g., too theoretical, outdated, disorganized, missing step-by-step action plans, wrong audience). If reviews are unavailable, label inferred gaps as `[ASSUMPTION]`.

### Step 2: Generate 3 Distinct Positioning Angles
Create three non-overlapping positioning cards—one for each strategy:
1. **Angle 1 — More Value:** A deeper, more complete, action-packed edition (more exercises, templates, checklists, reference tables, step-by-step frameworks—keeping content text-led per Test C).
2. **Angle 2 — Simpler / Faster:** A streamlined, beginner-friendly, quick-win edition (plain English, zero fluff, shorter steps, fast implementation).
3. **Angle 3 — Niche Audience:** The core topic tailored specifically to an underserved buyer sub-group with its own specific pain points and vocabulary.

### Step 3: Recommend the Winner & Lock the Positioning Brief
- Give a 1–2 sentence `[RECOMMENDATION]` on which of the 3 angles has the strongest chance of winning on Page 1 and ask Samir which angle he wants to lock in.
- **Batch Mode:** If Samir provides multiple source books at once, generate a separate source summary + 3 cards for each book, followed by a comparison table of the strongest angle per book.
- Once Samir selects an angle (or blend), generate the **Locked Positioning Brief** (Section 4B) to feed `Step_08` and `Step_09`.

---

## 3. Strict Quality, Title & Compliance Rules
1. **Title & Subtitle Formula:**
   - **Main Title:** Keep close to the exact validated buyer keyword phrase.
   - **Subtitle:** Under `~150 characters`; clearly state **Target Audience + Core Outcome + Concrete Proof Element** (e.g., number of templates, worksheets, or steps).
   - **Forbidden in Titles:** No trademarked names, no `"#1 Best Seller"` claims, and no unverifiable medical, legal, or financial guarantees.
2. **Concrete Deliverables Only:** In the 6 `"What it includes"` bullets, avoid vague promises. Name tangible text-friendly assets that will literally appear inside the book (e.g., *"7-day quick-start checklist"*, *"15 fill-in-the-blank conversation scripts"*).
3. **Differentiation, Never Imitation:** Never copy the source book's title, chapter structure, text, or cover.
4. **Data Honesty:** Never invent or guess BSR, rating, review count, or page count—write `no data` if unknown. Keep book titles in the target marketplace language (default: US English) and write explanations in simple English.

---

## 4. Required Output Formats

### Part A: Source Summary & 3 Positioning Cards
Save/output to: `07_Product_Briefs/positioning_<niche>_<yyyymmdd>.md`

```markdown
# Competitive Positioning — <niche_in_lowercase_with_underscores>
Capture date: <YYYY-MM-DD>
Source book: <Own-words label / ASIN> · BSR #<rank or no data> · <rating>★ · <N> reviews · <N> pages [VERIFIED: <url>, <YYYY-MM-DD>]
Main gap identified: <1-sentence summary of the biggest weakness>

---

## Angle 1: [More Value]
- **Title:** <Main Title>: <Benefit-led Subtitle under 150 chars>
- **Best for:** <1 line naming the exact buyer>
- **Overview:** <1–2 sentences on what this book does differently>
- **Positioning Angle:** <1–2 sentences stating the exact source-book gap this exploits>
- **Why It Fits the Market:** <1–2 sentences on buyer intent and why this converts>
- **What it includes (6 concrete items):**
  - Chapter 1: <Sample chapter title + focus>
  - Chapter 2: <Sample chapter title + focus>
  - Chapter 3: <Sample chapter title + focus>
  - Deliverable 4: <Specific template, script, or worksheet>
  - Deliverable 5: <Specific checklist or action plan>
  - Deliverable 6: <Specific reference table or troubleshooting guide>

---

## Angle 2: [Simpler / Faster]
*(Same exact structure as Angle 1)*

---

## Angle 3: [Niche Audience]
*(Same exact structure as Angle 1)*

---

## Recommendation & Next Step
- **Recommended Angle:** `[RECOMMENDATION]` <1–2 sentences explaining which angle wins and why>.
- **Decision Needed:** Which of the 3 angles (or blend) do you want to lock in for the Positioning Brief and Product Strategy?

# LOCKED POSITIONING BRIEF — <niche>
Locked date: <YYYY-MM-DD>
Chosen strategy: <More Value | Simpler/Faster | Niche Audience | Blend>

- **Working Title + Subtitle:** <Locked Title: Subtitle>
- **Target Reader:** <Who they are, skill level, and #1 frustration>
- **Core Promise:** <1-sentence transformation the reader gets>
- **Source Book Gap We Exploit:** <Specific weakness we solve>
- **Top Differentiators (3–5):** <Concrete elements our book has that competitors lack>
- **Format & Length Target:** <Paperback/Kindle/Audio + target page range + text-led asset count>
- **Tone & Reading Level:** <e.g., Clear, practical, empathetic, Grade 7–8 simple English>
- **Primary Keywords (5–7):** <Verified buyer search phrases from Step_03>
- **Draft Chapter Map (8–12 chapters):**
  1. <Chapter Title> — <1-line purpose>
  2. ...
- **Must-Include Deliverables:** <The 6 concrete items from the chosen card>
- **Do-Not-Do List:** No copying source book structure/text, no medical/legal/income promises, no fluff/padding, no heavy image dependency.

**Next Pipeline Steps:**
1. `Step_08_kdp-product-strategy` (Full Product Brief & pricing/spec lock)
2. `Step_09_kdp-book-outline-builder` (Detailed chapter-by-chapter blueprint)
3. `Step_10_kdp-original-book-writing` (Chapter drafting)
# 

