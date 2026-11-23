# Pranav Gudise

I've spent the last two years helping enterprise clients get AI systems live, most recently designing the rubrics that judge agent output at Surge.

Each repo here is a small, working build for one deployment problem: the eval, check or go-live gate I'd want in place before an AI system goes live with a customer. All of them use synthetic or public data, and most have a one-click demo page that needs no install.

[LinkedIn](https://www.linkedin.com/in/pranav-gudise/)

## Toolkit

| Build | What it does | |
|---|---|---|
| [golive-gate](https://github.com/pg2342-hub/golive-gate) | The pattern behind the builds below as one open-source Python package, CLI and GitHub Action: eval cases, rule and LLM judge checks, and a go-live gate written as YAML that answers go, partial or no-go, with the reason. Includes ablation and regression diffs | [Demo](https://pg2342-hub.github.io/golive-gate/) |

## Evals and go-live gates for agents

| Build | What it does | |
|---|---|---|
| [booking-eval-harness](https://github.com/pg2342-hub/booking-eval-harness) | 25-case eval and go-live gate for an agent that books field-service jobs (job, fee, area, slot, hand-off) | [Demo](https://pg2342-hub.github.io/booking-eval-harness/) |
| [appointment-agent-eval](https://github.com/pg2342-hub/appointment-agent-eval) | Eval for a freight appointment-scheduling agent; switch any check off and see which cases catch it | [Demo](https://pg2342-hub.github.io/appointment-agent-eval/) |
| [voice-agent-bakeoff](https://github.com/pg2342-hub/voice-agent-bakeoff) | Scorecard and rollout gate for moving a voice screening agent to a new model: replay, then 10%, then 50% | [Demo](https://pg2342-hub.github.io/voice-agent-bakeoff/) |
| [ticket-routing-eval](https://github.com/pg2342-hub/ticket-routing-eval) | Picks the confidence threshold for auto-routing support tickets, with accuracy, misroutes and cost per 1,000 tickets | [Demo](https://pg2342-hub.github.io/ticket-routing-eval/) |
| [sim-texas-file-prereview](https://github.com/pg2342-hub/sim-texas-file-prereview) | A Sim workflow that pre-reviews home sale files for compliance, with a 25-case eval and a go-live gate | |
| [othello-moment-test](https://github.com/pg2342-hub/othello-moment-test) | 25-moment test of whether a live-call sales coach suggests the right next step | |

## Monitoring live data

| Build | What it does | |
|---|---|---|
| [complaint-signal-detector](https://github.com/pg2342-hub/complaint-signal-detector) | Flags complaint types rising in a medical device's public FDA reports, backtested on what FDA had received before each recall; Claude tags free text behind guardrails, scored on 76 hand-labeled reports | [Demo](https://pg2342-hub.github.io/complaint-signal-detector/) |

## Agents and agent studies

| Build | What it does | |
|---|---|---|
| [contract-memory-harness](https://github.com/pg2342-hub/contract-memory-harness) | Compares long context, retrieval, a tool agent and a precomputed memory over a contract bank, and what breaks when a contract is amended | [Demo](https://pg2342-hub.github.io/contract-memory-harness/) |
| [agent-coldstart-study](https://github.com/pg2342-hub/agent-coldstart-study) | Can a fresh coding agent find and set up an email inbox on its own? 8 cold-start runs, traces and findings | [Results](https://pg2342-hub.github.io/agent-coldstart-study/) |
| [prompt-to-quote](https://github.com/pg2342-hub/prompt-to-quote) | A rep's plain-English deal becomes a priced quote with its approvals, on a public price book; runs in the browser | [Demo](https://pg2342-hub.github.io/prompt-to-quote/) |
| [imessage-reorder-agent](https://github.com/pg2342-hub/imessage-reorder-agent) | Text "the usual," confirm, pay; everything else goes to a person. Tested on 28 conversations against a mock API | [Demo](https://pg2342-hub.github.io/imessage-reorder-agent/) |
| [intake-to-po-agent](https://github.com/pg2342-hub/intake-to-po-agent) | Takes a plain-language purchase request through to a PO decision under a buying policy, with a labeled eval set | |

## Rollout and data-readiness checks

| Build | What it does | |
|---|---|---|
| [golive-readiness-check](https://github.com/pg2342-hub/golive-readiness-check) | Unit-by-unit go/no-go for a hospital staffing rollout across HR, timekeeping and EHR feeds, with fixes grouped by owning team | [Demo](https://pg2342-hub.github.io/golive-readiness-check/) |
| [robot-cabling-gate](https://github.com/pg2342-hub/robot-cabling-gate) | Decides when a cabling robot in a data center can work without a tech watching: every connection graded each shift, ten GO shifts in a row to go unsupervised, Claude triage of tech notes and a number-checked weekly update | [Demo](https://pg2342-hub.github.io/robot-cabling-gate/) |
| [capital-account-tieout](https://github.com/pg2342-hub/capital-account-tieout) | Ties every LP capital account to the prior administrator's statement before a fund admin switch, and names the likely cause of each break | [Demo](https://pg2342-hub.github.io/capital-account-tieout/) |
| [margin-bridge-tieout](https://github.com/pg2342-hub/margin-bridge-tieout) | Rebuilds a quarter's gross-profit bridge from ERP invoice lines, ties it to the ledger first, and finds the driver a favorable total hides; 25-case go-live gate in CI | [Demo](https://pg2342-hub.github.io/margin-bridge-tieout/) |
| [ap-autoforward-gate](https://github.com/pg2342-hub/ap-autoforward-gate) | Decides which jobs have earned AI invoice auto-forwarding and which invoices AP must still clear | [Demo](https://pg2342-hub.github.io/ap-autoforward-gate/) |
| [interview-stall-monitor](https://github.com/pg2342-hub/interview-stall-monitor) | Flags stalled interview-scheduling threads and seats nobody uses after a rollout, and writes the weekly value report; rules tested on 28 labeled threads in CI | [Demo](https://pg2342-hub.github.io/interview-stall-monitor/) |
| [carrier-sourcing-scorecard](https://github.com/pg2342-hub/carrier-sourcing-scorecard) | Scores an AI carrier-sourcing agent against what reps actually booked, with the broker's rules as a hard gate | [Demo](https://pg2342-hub.github.io/carrier-sourcing-scorecard/) |
| [carrier-onboarding-checks](https://github.com/pg2342-hub/carrier-onboarding-checks) | Checks carriers against public FMCSA data and a broker's rules before TMS entry, with every decision logged | |
| [partner-deliverable-qa](https://github.com/pg2342-hub/partner-deliverable-qa) | Holds a consulting partner's discovery deliverable to standard before it reaches the customer | [Demo](https://pg2342-hub.github.io/partner-deliverable-qa/) |
| [contract-obligation-tracker](https://github.com/pg2342-hub/contract-obligation-tracker) | Pulls obligations and notice dates out of contracts; a person verifies each field before it can trigger an alert | [Demo](https://pg2342-hub.github.io/contract-obligation-tracker/) |
| [odyssey-doctor](https://github.com/pg2342-hub/odyssey-doctor) | Command-line checker for common integration gaps in apps built on the Odyssey API, no key needed | [Demo](https://pg2342-hub.github.io/odyssey-doctor/) |
