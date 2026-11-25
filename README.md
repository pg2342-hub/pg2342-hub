# Pranav Gudise

I've spent the last two years helping enterprise clients get AI systems live, most recently designing the rubrics that judge agent output at Surge.

Each repo here is a small, working build for one deployment problem: the eval, check or go-live gate I'd want in place before an AI system goes live with a customer. All of them use synthetic or public data, and most have a one-click demo page that needs no install.

[LinkedIn](https://www.linkedin.com/in/pranav-gudise/)

## Toolkit

| Build | What it does | |
|---|---|---|
| [golive-gate](https://github.com/pg2342-hub/golive-gate) | An open-source Python package, CLI and GitHub Action that several builds below use for their gates: eval cases, rule and LLM judge checks, and a go-live gate written as YAML that answers go, partial or no-go, with the reason. Includes ablation and regression diffs | [Demo](https://pg2342-hub.github.io/golive-gate/) |

## Evals and go-live gates for agents

| Build | What it does | |
|---|---|---|
| [frontdesk-call-gate](https://github.com/pg2342-hub/frontdesk-call-gate) | Go-live gate for an AI hotel front desk: 30 guest calls graded by rules and a Claude judge on every outcome (answer, task, hand-off, sales lead), with go, partial or no-go in CI | [Demo](https://pg2342-hub.github.io/frontdesk-call-gate/) |
| [outbound-autosend-gate](https://github.com/pg2342-hub/outbound-autosend-gate) | Go-live gate for an AI outbound sales agent: 30 accounts with opt-outs, customers and another rep's deals as traps, rules and a Claude judge, and a per-step ladder that decides which emails can send without a rep | [Demo](https://pranavgudise.dev/outbound-autosend-gate/) |
| [sourced-memo-gate](https://github.com/pg2342-hub/sourced-memo-gate) | Graduation gate for an AI analyst drafting sourced research-memo sections: 30 requests with a client-wall trap, rules and a Claude judge, prompt versions compared on recorded live runs | [Demo](https://pranavgudise.dev/sourced-memo-gate/) |
| [booking-eval-harness](https://github.com/pg2342-hub/booking-eval-harness) | 25-case eval and go-live gate for an agent that books field-service jobs (job, fee, area, slot, hand-off) | [Demo](https://pg2342-hub.github.io/booking-eval-harness/) |
| [appointment-agent-eval](https://github.com/pg2342-hub/appointment-agent-eval) | Eval for a freight appointment-scheduling agent; switch any check off and see which cases catch it | [Demo](https://pg2342-hub.github.io/appointment-agent-eval/) |
| [voice-agent-bakeoff](https://github.com/pg2342-hub/voice-agent-bakeoff) | Scorecard and rollout gate for moving a voice screening agent to a new model: replay, then 10%, then 50% | [Demo](https://pg2342-hub.github.io/voice-agent-bakeoff/) |
| [service-desk-gap-finder](https://github.com/pg2342-hub/service-desk-gap-finder) | Finds the service desk fixes that live only in ticket notes, often the outside provider's, and lets a topic auto-resolve only after 48 of its last 50 drafts are approved | [Demo](https://pranavgudise.dev/service-desk-gap-finder/) |
| [ticket-routing-eval](https://github.com/pg2342-hub/ticket-routing-eval) | Picks the confidence threshold for auto-routing support tickets, with accuracy, misroutes and cost per 1,000 tickets | [Demo](https://pg2342-hub.github.io/ticket-routing-eval/) |
| [sim-texas-file-prereview](https://github.com/pg2342-hub/sim-texas-file-prereview) | A Sim workflow that pre-reviews home sale files for compliance, with a 25-case eval and a go-live gate | |
| [othello-moment-test](https://github.com/pg2342-hub/othello-moment-test) | 25-moment test of whether a live-call sales coach suggests the right next step | |
| [contract-memory-harness](https://github.com/pg2342-hub/contract-memory-harness) | Compares long context, retrieval, a tool agent and a precomputed memory over a contract bank, and what breaks when a contract is amended | [Demo](https://pg2342-hub.github.io/contract-memory-harness/) |
| [agent-coldstart-study](https://github.com/pg2342-hub/agent-coldstart-study) | Can a fresh coding agent find and set up an email inbox on its own? 8 cold-start runs, traces and findings | [Results](https://pg2342-hub.github.io/agent-coldstart-study/) |
| [notice-simulator](https://github.com/pg2342-hub/notice-simulator) | Tests versions of a bank-migration notice on Claude persona panels for 8 income and age groups, and only trusts a group whose panel first matches the Federal Reserve's household survey; recorded live run, replayed in CI | [Demo](https://pranavgudise.dev/notice-simulator/) |

## Monitoring live data

| Build | What it does | |
|---|---|---|
| [complaint-signal-detector](https://github.com/pg2342-hub/complaint-signal-detector) | Flags complaint types rising in a medical device's public FDA reports, backtested on what FDA had received before each recall; Claude tags free text behind guardrails, scored on 76 hand-labeled reports | [Demo](https://pg2342-hub.github.io/complaint-signal-detector/) |
| [attack-path-readout](https://github.com/pg2342-hub/attack-path-readout) | Turns validated attack paths from a security test into fix tickets for the teams that own each asset: Claude writes each ticket behind guardrails, anything that reaches a crown-jewel system waits for a person, and a weekly readout tracks retests and time to close; real CISA KEV and FIRST EPSS data on a made-up utility, gated in CI | [Demo](https://pranavgudise.dev/attack-path-readout/) |

## Agents and tools

| Build | What it does | |
|---|---|---|
| [freight-appointment-agent](https://github.com/pg2342-hub/freight-appointment-agent) | An email agent that books freight dock appointments, running live on Cloudflare with Claude: real tool calls, a trace for every thread, a go-live gate on held-out email in CI and a staged 10/50/100 rollout | [Live](https://freight-appointment-agent.pg2342.workers.dev) |
| [clinic-voice-agent](https://github.com/pg2342-hub/clinic-voice-agent) | A phone agent for a two-clinic mental health practice that books, moves and cancels visits in a mock scheduler on Cloudflare, with a crisis path and hand-offs to staff; talk to it in the browser, and read ten scored test conversations and what each round changed | [Demo](https://pranavgudise.dev/clinic-voice-agent/) |
| [watchlist-hit-reviewer](https://github.com/pg2342-hub/watchlist-hit-reviewer) | Reviews OFAC sanctions hits from a KYC platform's webhook: decrypts only the fields it needs, has Claude compare each hit with the real SDN entry, posts a pass only when code confirms the hit is not the customer, and hands the rest to an analyst; backtested on 40 past reviews | [Demo](https://pranavgudise.dev/watchlist-hit-reviewer/) |
| [order-intake-agent](https://github.com/pg2342-hub/order-intake-agent) | Turns messy shipment-request emails (PDF tenders, spreadsheets, forwarded threads) into orders with Claude, applies each shipper's rules, and hands anything risky to an operator with a note; per-shipper rollout from shadow to approve to auto, 30-email test set in CI | [Demo](https://pranavgudise.dev/order-intake-agent/) |
| [lease-issues-list](https://github.com/pg2342-hub/lease-issues-list) | Reviews a commercial office lease against a landlord's standard positions and drafts the issues list a lawyer reviews: Claude reads the lease, code checks every quote word for word, and anything unverified becomes a check item; 90 of 90 positions right on six answer-keyed leases, run on four public SEC-filed leases | [Demo](https://pranavgudise.dev/lease-issues-list/) |
| [page-change-agent](https://github.com/pg2342-hub/page-change-agent) | Turns a website change request filed as a GitHub issue into an unpublished CMS draft with Claude: compliance checks it cannot talk past, a read-back from Contentful and a before and after diff on the issue, while disclosures, rates and claims go to compliance; 30 of 30 requests right on three recorded live runs | [Demo](https://pranavgudise.dev/page-change-agent/) |
| [prebill-chart-check](https://github.com/pg2342-hub/prebill-chart-check) | Checks each urgent care claim against its note before it goes out: pulls visits over FHIR R4, Claude grades the note's medical decision making without seeing the billed level, and fixed rules release, auto-fix, route to the clinician or hold; a go-live gate on 30 hand-labeled visits caught a prompt miss and re-ran it in CI | [Demo](https://pranavgudise.dev/prebill-chart-check/) |
| [prompt-to-quote](https://github.com/pg2342-hub/prompt-to-quote) | A rep's plain-English deal becomes a priced quote with its approvals, on a public price book; runs in the browser | [Demo](https://pg2342-hub.github.io/prompt-to-quote/) |
| [imessage-reorder-agent](https://github.com/pg2342-hub/imessage-reorder-agent) | Text "the usual," confirm, pay; everything else goes to a person. Tested on 28 conversations against a mock API | [Demo](https://pg2342-hub.github.io/imessage-reorder-agent/) |
| [intake-to-po-agent](https://github.com/pg2342-hub/intake-to-po-agent) | Takes a plain-language purchase request through to a PO decision under a buying policy, with a labeled eval set | |

## Rollout and data-readiness checks

| Build | What it does | |
|---|---|---|
| [scenario-coverage-map](https://github.com/pg2342-hub/scenario-coverage-map) | Maps which conditions real driving logs cover and where a perception model misses cars, compares a simulated twin and its fog, rain and low-sun renders, and ranks which scenario packs to simulate next | [Demo](https://pranavgudise.dev/scenario-coverage-map/) |
| [golive-readiness-check](https://github.com/pg2342-hub/golive-readiness-check) | Unit-by-unit go/no-go for a hospital staffing rollout across HR, timekeeping and EHR feeds, with fixes grouped by owning team | [Demo](https://pg2342-hub.github.io/golive-readiness-check/) |
| [robot-cabling-gate](https://github.com/pg2342-hub/robot-cabling-gate) | Decides when a cabling robot in a data center can work without a tech watching: every connection graded each shift, ten GO shifts in a row to go unsupervised, Claude triage of tech notes and a number-checked weekly update | [Demo](https://pg2342-hub.github.io/robot-cabling-gate/) |
| [migration-cutover-gate](https://github.com/pg2342-hub/migration-cutover-gate) | Go-live gate for moving a law firm's data into a new practice management system: rules clean the export, Claude makes the matching calls rules cannot, and nothing loads until counts, balances owed and trust totals tie to the old system's reports | [Demo](https://pranavgudise.dev/migration-cutover-gate/) |
| [restaurant-onboarding-monitor](https://github.com/pg2342-hub/restaurant-onboarding-monitor) | Takes a multi-location restaurant group live on back-of-house software: maps distributor order guides into one catalog with rules first and Claude behind guardrails, says location by location what blocks go-live and who fixes it, then checks the live data every day; planted problems caught in CI, recorded live run replayed | [Demo](https://pranavgudise.dev/restaurant-onboarding-monitor/) |
| [capital-account-tieout](https://github.com/pg2342-hub/capital-account-tieout) | Ties every LP capital account to the prior administrator's statement before a fund admin switch, and names the likely cause of each break | [Demo](https://pg2342-hub.github.io/capital-account-tieout/) |
| [margin-bridge-tieout](https://github.com/pg2342-hub/margin-bridge-tieout) | Rebuilds a quarter's gross-profit bridge from ERP invoice lines, ties it to the ledger first, and finds the driver a favorable total hides; 25-case go-live gate in CI | [Demo](https://pg2342-hub.github.io/margin-bridge-tieout/) |
| [variance-commentary-gate](https://github.com/pg2342-hub/variance-commentary-gate) | Drafts monthly budget-vs-actual commentary with the query behind every figure, stops on an extract that does not tie, and holds risky lines for FP&A; 25-case gate in CI | [Demo](https://pranavgudise.dev/variance-commentary-gate/) |
| [sales-tax-return-checks](https://github.com/pg2342-hub/sales-tax-return-checks) | Recomputes each prepared sales tax return from its sales and blocks it or sends it to review before filing; six planted errors are caught in CI | [Demo](https://pranavgudise.dev/sales-tax-return-checks/) |
| [ap-autoforward-gate](https://github.com/pg2342-hub/ap-autoforward-gate) | Decides which jobs have earned AI invoice auto-forwarding and which invoices AP must still clear | [Demo](https://pg2342-hub.github.io/ap-autoforward-gate/) |
| [interview-stall-monitor](https://github.com/pg2342-hub/interview-stall-monitor) | Flags stalled interview-scheduling threads and seats nobody uses after a rollout, and writes the weekly value report; rules tested on 28 labeled threads in CI | [Demo](https://pg2342-hub.github.io/interview-stall-monitor/) |
| [carrier-sourcing-scorecard](https://github.com/pg2342-hub/carrier-sourcing-scorecard) | Scores an AI carrier-sourcing agent against what reps actually booked, with the broker's rules as a hard gate | [Demo](https://pg2342-hub.github.io/carrier-sourcing-scorecard/) |
| [carrier-onboarding-checks](https://github.com/pg2342-hub/carrier-onboarding-checks) | Checks carriers against public FMCSA data and a broker's rules before TMS entry, with every decision logged | [Demo](https://pg2342-hub.github.io/carrier-onboarding-checks/) |
| [partner-deliverable-qa](https://github.com/pg2342-hub/partner-deliverable-qa) | Holds a consulting partner's discovery deliverable to standard before it reaches the customer | [Demo](https://pg2342-hub.github.io/partner-deliverable-qa/) |
| [contract-obligation-tracker](https://github.com/pg2342-hub/contract-obligation-tracker) | Pulls obligations and notice dates out of contracts; a person verifies each field before it can trigger an alert | [Demo](https://pg2342-hub.github.io/contract-obligation-tracker/) |
| [odyssey-doctor](https://github.com/pg2342-hub/odyssey-doctor) | Command-line checker for common integration gaps in apps built on the Odyssey API, no key needed | [Demo](https://pg2342-hub.github.io/odyssey-doctor/) |
