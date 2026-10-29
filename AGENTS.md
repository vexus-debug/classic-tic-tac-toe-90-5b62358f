<!-- LOVABLE:BEGIN -->
> [!IMPORTANT]
> This project is connected to [Lovable](https://lovable.dev). Avoid rewriting
> published git history — force pushing, or rebasing/amending/squashing commits
> that are already pushed — as it rewrites history on Lovable's side and the
> user will likely lose their project history.
>
> Commits you push to the connected branch sync back to Lovable and show up in
> the editor, so keep the branch in a working state.
<!-- LOVABLE:END -->

- Branch-assigned non-admin staff automatically enter their sole sub-branch after sign-in, avoiding an unnecessary clinic picker.
- The installed app's `/sw.js` (scope /app/) never caches pages; it clears legacy caches and handles Web Push (VAPID, sent from a super-admin server function) whose taps open /app/inbox/:id.
- Dental dashboard data is role-focused: leadership sees clinic financials, dentists see their assigned schedule, and front-desk roles see queue and collections.
- All frontend images (including dashboard screenshots on marketing pages) must be stored as real image files in the codebase (`src/assets/`, imported directly) — never as `.asset.json` CDN pointers or remote storage URLs. Fresh dashboard screenshots go in `src/assets/dashboard-shots/`. Tutorial image files remain isolated and unchanged. Why: CDN pointers broke (404) when the project moved; in-code images always travel with the repo.
- Every shipped feature, improvement or bug fix must be logged as a new entry (newest first) in `src/data/updates.ts` (the public /updates page) in the same change — no exceptions.
- MANDATORY for any design/UI/layout/visual/styling task (plan or implementation): go through the Garden Skills suite — consult `skills/README.md`, then read `skills/web-design-engineer/SKILL.md` in full and follow its entire workflow, plus every reference file it routes to under `skills/web-design-engineer/references/` and any other matching design skills (e.g. `skills/creative-design/`, `skills/web-development/tailwind-design-system/`). Do not use `docs/design-skill/`. Why: the user requires all design work to be governed by the Garden Skills suite, not ad-hoc plans.
- MANDATORY for every AI assistant: the full Garden Skills suite lives in `skills/` (index: `skills/README.md`). Before any task matching a skill (design, articles, images, motion, presentations, knowledge retrieval), read that skill's `SKILL.md` in full plus its routed references and follow its workflow exactly. Why: guidelines must be tool-agnostic so any AI builder applies them identically.

- MANDATORY SKILL LOOKUP: before planning or implementing any task, consult `skills/README.md`, identify the matching category and skill, read that skill's `SKILL.md` in full and follow its workflow. Why: a curated skill library ensures every AI agent applies the same proven practices.
