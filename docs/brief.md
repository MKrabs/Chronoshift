# Chronoshift: Living Brief

*Living document. Last updated 2026-09-28. Repo: https://github.com/MKrabs/Chronoshift*

## 1. What this is

A **personal, very interactive car blog** that grows through shared knowledge and a data structure. Think of a quick, fun, digital car magazine for **everyday car enthusiasts**, not mechanics or dealers. You can browse it for general facts (the Civic lineage) and dig into niche ones (why a Porsche interior part also shows up in a VW Golf). The goal is to get people into cars and help them learn.

It **gathers and showcases** what's known, with sources, the way Wikipedia does. It does **not** claim to be the source of truth.

**Why it exists:** looking up car facts online today is a hassle, often wrong, or not searchable. It's a passion project and not meant to sell.

## 2. Decisions so far

| # | Decision | Why / notes |
|---|----------|-------------|
| D1 | The audience is enthusiasts and curious newcomers | This sets the tone: approachable, visual, fun |
| D2 | "Correlate" means lineage/ownership (a graph over time) plus platform, engine and part sharing (many-to-many). Tuning and culture trends come later | Two data shapes to support early on |
| D3 | Models and lineups are the main entities. Brands come second. Community, culture, races and aftermarket come later | This keeps the MVP small |
| D4 | The site stays neutral. Where sources disagree, we state the general consensus and show the conflicting claims, each with its sources. The reader decides | Every fact needs a source |
| D5 | The data model allows all eras and markets. Content starts with **1980s to 2000s** | Expand later |
| D6 | It's a living site, not a one-time snapshot | So it needs an update and contribution path |
| D7 | It's non-commercial | Share-alike licences are acceptable if we choose them |
| D8 | Quick and fun beats complete and perfect | We showcase sourced knowledge; we're not the authority |
| D9 | **Pilot focus: JDM with a Honda emphasis, plus the European rally/racing era** (e.g. Peugeot 205 T16, Lancia Delta Integrale, Audi Quattro, Escort Cosworth) | Owner's passion and the richest lore |
| D10 | **Roles:** AI researches and collects sourced snippets. The human sifts them and writes all the article text. AI builds the code and infrastructure. Planning is joint | A human stays the editor; AI never publishes unchecked text |
| D11 | 3D is nice to have, not an MVP feature | Cost, licensing, page weight |
| D12 | No page for every single part. Shared parts appear as a section on model pages and as comparison views ("what does the CRX share with the S2000?"). Only famous parts and engines (B16, K20, 2JZ, RB26) get their own page | Keeps the content manageable |
| D13 | **It's a personal blog** in the owner's voice, made extendable by a shared knowledge structure underneath | The owner's reflection, 2026-09-28 |
| D14 | **Working agreement:** Claude's work is labelled `needs-human-review`; the owner hands tasks over with `for-claude`; Claude checks the board at each session start. See `CLAUDE.md` | Keeps the owner in control of everything Claude produces |

## 3. Proposed principles (not yet agreed)

- **Broad skeleton, curated depth.** Pull the list of all brands and models with years automatically from Wikidata (CC0). Write deep content only for the pilot list. Pages with no content yet say so honestly and invite a suggestion.
- **The basic unit is a sourced claim.** This is plumbing that readers never see directly. Each fact is stored with its sources and linked to one or more cars, engines or parts. It shows up as the "shared parts" sections, comparison pages, and conflicting-claims boxes.
- **Content as code.** Pages and snippets live as files in the repo, and contributions come in as issues or pull requests. We'd only move to a database or CMS once that hurts.
- **Cite, don't copy.** Forums, Reddit and old blogs are sources to link (with archive.org snapshots), not text to copy. Old magazines: cite and summarise, don't host scans.
- **Images come from Wikimedia Commons**, with credit shown for each image.
- **Build-your-own (icebox):** start from *documented swaps and stories* rather than computing whether parts fit. Fitment data is the hardest data there is.

## 4. Open questions

1. **Three hero questions** the site answers better than a Google search.
2. **The exact pilot list** of ~30–50 cars.
3. **Reddit access.** Direct fetching is blocked in Claude's workspace. Options: the official Reddit API run by the owner, manual exports and paste-ins, or leaning on forums (honda-tech, s2ki), which *are* reachable.
4. **Stack.** Deliberately undecided until after the thin slice (M4).
5. **Personal voice vs. neutrality (D4 vs D13).** A personal blog has opinions. Suggestion: articles may have your voice and opinions, but *disputed facts* are always shown with both sides and their sources. Agree?

## 5. Backlog

Lives on the GitHub board: https://github.com/MKrabs/Chronoshift/issues. Milestones M0–M4 are the checkpoints: Brief → Data check → Design on paper → First small version → Look back and choose tech. Parked ideas carry the `icebox` label.
