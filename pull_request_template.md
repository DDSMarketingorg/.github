<!--
Four questions, then the gates a person has to check. Each one is here because it was missed in
production, not because it sounds good.

Don't list CI checks here (lint, types, tests, coverage, build and so on). They run on their own,
and a red one tells you what to fix. A checkbox means a person had to look.
-->

## Intention

<!-- What is this for? Link the issue here, and link this PR from the issue. -->
Linear:

<!-- If a patient can reach this behaviour, one line each. Otherwise delete these two lines. -->
Must:
Must never:

## Governance

<!-- Does the diff add an external hostname, SDK or third-party destination for company data?
     If yes, name the approver and the agreement (BAA or DPA). No agreement means no merge. -->
New third-party data flow (yes/no):

## Verification

<!-- Name the check that fails if this regresses. "Tested manually" is not a check.
     If you added or changed an evaluation, show that it can return a pass: an evaluation that
     can never pass looks exactly like one that always fails, and both get trusted. -->
Regression check:

## Evidence

<!-- What will show this happened, six months from now? UI change: a screenshot. Behaviour
     change: end-to-end proof, such as a trace, a log line, or a request and its response.
     Redact PHI from all evidence, screenshots included. -->

## Hard gates

<!-- Tick each one and write its evidence after the dash (file:line, test or trace).
     If it doesn't apply, tick it and write "n/a:" with the reason.
     If this repo's CI enforces it, tick it and write "n/a: enforced by <check name>".
     A tick with nothing after the dash is not a check. -->

- [ ] Routes that can return patient data require auth and scope the caller to their practice —
- [ ] New or changed inbound webhooks verify their signature before trusting the payload —
- [ ] No new third-party data flow without a named approver and a signed agreement —
- [ ] No PHI in logs, error messages, exceptions, traces, metrics labels or debug output —
- [ ] Removing access revokes it, not only hides it —
- [ ] A new or changed evaluation was shown to return a pass —
- [ ] Evidence is attached above —
