# HPATPro QA Review Repo - Codex Instructions

This repo is the HPATPro QA review workspace for Web Codex and GitHub-connected review work. HPATPro is operated for Ivora Limited, owned by Anil (CEO).

## Before Starting

1. Identify the runtime: `Web Codex` unless the user says otherwise.
2. State the role: usually `Reviewer` or `Research/Process`; use `Builder` only for declared review-site changes.
3. State the exact scope: QA review page, data file, review workflow, PR, branch, or process target.
4. Check the latest project handoff before editing. Use `HPATPro_Project_Log.md` if present in the workspace; otherwise ask for the latest Mac Codex handoff, PR notes, or user instruction.

## Mac/Web Codex Coordination

- Web Codex is best here for independent QA review, review-page fixes, GitHub PR review, security/process review, and cloud-resumable review tasks.
- Mac Codex is best for local source screenshots, PDFs, slide decks, Google Drive exports, reviewer workbooks, and files that exist only under `/Users/banty/Desktop/Codex`.
- Do not assume Mac Codex local changes exist here unless they have been pushed, attached, pasted, or logged.
- Do not assume Web Codex changes exist on Mac Codex unless they have been pulled, attached, pasted, or logged.
- One owner per file/module/task at a time. If another Codex session is actively changing a file, stay in review mode or ask the user to coordinate.
- Reviewer sessions should produce findings first, ordered by severity, with file/page references where possible.
- Builder sessions should edit only the declared scope and leave a clear handoff.

## QA Safety

- Treat unreleased HPATPro question content as private.
- Do not send emails, share external files, change GitHub Pages/settings, change repository permissions/settings, or publish new review material externally without explicit user approval.
- Do not make Supabase production writes from this repo.
- For question-bank work, no `INSERT INTO questions`, `UPDATE questions`, or `DELETE FROM questions` is allowed unless the required QA gates are complete and CEO approval is explicit.

## Question Bank Gate 5 Blocker

Before any `INSERT INTO questions` statement, verify all of these exist:

1. Agent B verification log with 100% PASS.
2. `{Batch}_AI_Review_Consolidated.md` showing Gate 5 review from at least two external AIs.
3. Run manifest with a `gate5_report` field.

If the consolidated report does not exist, the database write is BLOCKED. Creating a reviewer package is not Gate 5 completion; the report must prove external AIs actually reviewed the batch.

## Completion Notes

For meaningful work, leave a short handoff containing:

- What changed.
- Files touched.
- Verification performed.
- What was not done.
- Safety notes: especially no database write, no email/share, no production or permission changes when applicable.
