# go-solo-planner

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
