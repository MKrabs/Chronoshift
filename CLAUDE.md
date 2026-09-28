# CLAUDE.md: how we work on Chronoshift

Read this at the start of every session. It is our working agreement.

## What this project is

A **personal, very interactive car blog** that grows through shared knowledge and a data structure. It focuses on JDM cars (especially Honda) and the European rally/racing era, starting with the 1980s–2000s. It gathers and showcases sourced knowledge. It is **not** meant to be the source of truth.

The full living brief is [`docs/brief.md`](docs/brief.md).

## Who does what

- **The owner (human):** decides, reviews, and writes all article text.
- **Claude:** researches and collects sourced snippets, writes the code and infrastructure, and keeps the board and brief up to date.
- **Both:** plan together.

## At the start of every session

1. **Check the board** (GitHub issues on MKrabs/Chronoshift):
   - open issues labelled `for-claude`: these are tasks handed to Claude
   - new comments on issues labelled `needs-human-review`: this is the owner's feedback
2. **Catch the owner up** in a few plain sentences: what changed since last time, what's waiting for them, and what Claude plans to do next. No jargon. If a term is needed, explain it.
3. Then work.

## Rules for Claude

- **Nothing is final without the owner.** Every issue, pull request or doc change Claude makes gets the `needs-human-review` label.
- **Small batches.** Create at most 3–5 new issues at a time.
- **Plain issues.** Every issue starts with **Why this matters** and **Done when**.
- **Never close issues or merge pull requests yourself.** Suggest it in a comment; the owner decides. (Exception: the owner explicitly agrees in chat.)
- **Changes go through pull requests**, not direct pushes to `main`.
- **Keep the living documents current.** When a decision changes, update [`docs/brief.md`](docs/brief.md) in the same pull request, and mirror it to the Claude project doc `claude/chronoshift-brief.md`.
- **When the owner hands over a task** in chat without an issue, create one with `for-claude` so the board stays the single overview.

## Labels

| Label | Meaning |
|---|---|
| `needs-human-review` | Claude made or changed this; the owner checks it |
| `for-claude` | The owner handed this to Claude |
| `icebox` | A captured idea, deliberately not now |
| `planning` · `research` · `design` · `frontend` · `content` | The type of work |

## Research rules

- Every fact needs a source link, plus an archive.org backup link for blogs and forums.
- Link and summarise; never copy text. Old magazines: summarise, don't host scans.
- Images: Wikimedia Commons only, with credit.
- When sources disagree, record both sides with their sources. The owner decides what goes in the article.
- Reddit can't be fetched from Claude's workspace. Ask the owner to paste threads or use another source.

## Technical notes

- The GitHub CLI (`gh`) may not be installed in Claude's workspace. `GH_TOKEN` is available, so use the GitHub REST API directly (send `Content-Type: application/json`).
- The tech stack is deliberately undecided until milestone M4.
