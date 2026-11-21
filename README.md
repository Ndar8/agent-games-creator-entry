# Receipts Before Trust: Running a Crisis-Mode Agent With a Money Gate

**#AgentGames — Creator Track entry**

## Scope

This is a Creator Track entry. I have no live Proof Gatekeeper endpoint, no
Steal the VFY agent, and no arena score. What this article documents is a
working discipline — a written policy, narrow autonomous permissions, and
checkable receipts — run before this tournament, on the exact problem the
tournament is about: how do you know an agent did what it was supposed to do?

## The setup

I run a personal agent ("GAM") that operates across crypto farming, content
production, and competitions — mostly autonomously, around the clock. The
operator (me) works in what we call crisis mode: no permission prompts for
work already in scope, no rest, results only. That only works because the
autonomy is fenced by a written policy:

- **Fee-only auto-approval.** Free, gas-only mints/claims and free waitlist
  registrations execute directly without asking — including the wallet
  connection and signature the transaction itself needs.
- **Money gate.** Anything that sends, transfers, or spends money requires
  explicit per-item approval. Funding a wallet counts as a money move.
- **Verify-first.** If a fact is not verified, check it through every
  available route (CLI, API, search, browser) before answering. One failed
  lookup is not "don't know."
- **Secrets discipline.** Seed phrases and private keys never travel through
  chat. Agent-operated wallets are encrypted keystores; only public
  addresses appear in reports. Claim codes and other bearer secrets are
  never published.

## Receipts (all from 21 Nov 2026 unless noted)

1. **make.fun, as @iskandar (GitHub: Ndar8).**
   - tiny-chess-01 submitted: submission
     `01a1fd9a-8d45-71f8-86bc-d6f0066ee64d`, repo
     https://github.com/Ndar8/tiny-chess-01. Measured ~1,059 Elo against a
     1,154 floor — stated plainly, not inflated. The engine did not clear
     the bar, and the entry says so.
   - token-radar-01 submitted, then resubmitted (round 2) after a model
     audit found a thin-category ranking flaw: a protocol with only 4
     comparables was overvalued by a raw category median. The fix —
     statistical shrinkage of thin-sample ratios toward the global median —
     moved it from rank #12 to #22. Submission
     `01a1fdbf-7626-7446-ba9b-9cd061263878`, repo
     https://github.com/Ndar8/token-radar-01, commit `cbdfdbf`. 198
     protocols ranked; an in-page recompute matches the generated board on
     all rows (0 mismatches).
2. **Dialectica Expert serve ($TRUED).** 7 answers submitted, #1 verified
   and paid (+10 $TRUED), #4 falsified, balance 9 $TRUED. A watchdog checks
   the serve every 10 minutes and restarts it when it crashes; platform
   HTTP 429 / IncompleteRead failures are logged as failures, not hidden.
   Reliability slashes (REL-005) are recorded with their cause: the serve
   dying mid-job, not wrong answers.
3. **Content chains.** Stickman Story: batch 4 (24 videos) uploaded and
   scheduled hourly after a human-typed login — the login step stayed with
   the human, per policy. BEK BANGAI: 10 videos scheduled, then YouTube's
   unverified-channel daily upload limit stopped uploads. Reported as a
   limit, not worked around; the remaining stock waits for the reset.
4. **Failure honesty.** A natbox free-VPS slot claim on 21 Nov failed: the
   slot was gone in ~1 minute, no account was registered, the claim code
   was never entered, no payment made. Logged as a miss with the fix
   (register the account before the next drop), not spun as a win.

## Why this belongs in Agent Games

Every receipt above still asks the reader to trust my logs. The agent says
it followed the policy; the operator says the agent did. A proof-backed
decision — approve/reject bound to a committed policy, re-verified against
a registered verification key — is the missing step: the operator's policy
(fee-only auto, money gate, verify-first) becomes a checkable claim instead
of a promise. That is where zkVerify fits this workflow: not as decoration,
but as the difference between "the agent says it followed the rules" and
"anyone can verify the decision matched the rules."

The discipline already exists. The receipts already exist. The proof layer
is what turns them from a story into evidence.

---

*#AgentGames Creator Track entry — written by the operator of GAM, an
autonomous agent run under a written money-gate policy. All submission IDs
and repositories above are public and checkable.*
