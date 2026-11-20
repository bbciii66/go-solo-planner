# go-solo-planner (Bee2Boss)

Public, single-file app (`index.html`, vanilla JS, no build). It's the generic version of a private rate calculator. The only person in it is the made-up sample, "Sam".

## Roles
- Planner / builder: Claude (Claude Code)
- Independent review: a separate Claude reviewer agent so far. Codex or Claude-in-agy are fine for future reviews.

## Git
- Push policy: push automatically (Ben, 2026-11-19). Work on a branch, open draft PRs, never force-push.
- Merge policy (Ben, 2026-11-19): when a PR is tested (and independently reviewed if significant), Claude asks Ben in the thread; on his yes, Claude marks it ready, squash-merges and confirms the live Pages site. Don't hand Ben merge steps.

## Privacy (public repo)
- Never add real people's names, pay, employers, documents or state-specific defaults taken from the private calculator. Run a name and employer sweep before every push.

## Tax engine notes
- 2026, single filer: federal brackets, $16,100 standard deduction, SS wage base $184,500, 0.9% additional Medicare over $200k.
- Consulting: SE tax on 92.35% of profit, half-SE, SE health deduction, Solo 401(k) (24,500 deferral, +8,000 at 50+, +11,250 at 60-63, 72,000 cap, never more than earnings), QBI 20% phasing out from $201,750 over $75k.
- State: one flat rate on (AGI minus a user-set standard deduction).
- Test hook: `window.__planner` (w2, consult, solveRevenue, rateFor, runway, billHours, S).
- The Artifact viewer blocks downloads, print and confirm(), so keep confirmations inside the page.

## Brand
- Name: Bee2Boss (capital E in "Self-Employed"). Logo/favicon: the face-bee hive badge (crowned bee, wings read as glasses). Header animation: a small bee flies up a dotted path and pops into a mini badge with a star; static when reduced motion is on. Click the logo to replay.
- Plan switch: "My plan / Sam's plan" toggle in the flow keeps both. Own plan is parked in `goSoloPlanner-own` while viewing Sam; Sam's edits live in `bee2boss-sam` (Reset Sam's numbers clears it). Switching keeps the same step for comparison.
- Themes: parchment light (#F3EBDA) and softer slate dark (#2B303B), toggle saved as `bee2boss-theme`. Saved-plan keys stay `goSoloPlanner-*` so old saves still load.
