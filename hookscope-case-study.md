# Full ASDS lifecycle completed: RELEASED

After remediation, the same-input HookScope rebuild from an empty directory completed Startup → Finish → QA → Release and reached RELEASED. Release successfully executed the explicitly selected local artifact-delivery target: exact accepted artifact, no rebuild and hash/read-back reconciliation. External publication was intentionally outside the approved governance scope.

ASDS is a reusable delivery system around coding agents: Startup prepares the engineering foundation, Finish completes approved scope, QA evaluates the submitted candidate, and Release delivers what was accepted. Critic is separate and optional. HookScope, the dogfood project, is a local webhook inbox for inspecting deliveries and replaying them deliberately.

## Run 1: the system exposed its own failure modes

The first run completed Startup and reached a Finish product candidate. QA detected incompatible overlapping candidate/product and acceptance-contract roles in the Finish → QA handoff. After that defect was repaired, Finish submitted a new candidate and QA reported 59 unique product tests passed. QA nevertheless returned QA_FAILED because the mandatory audit of a development dependency chain remained blocking. Finish investigated but established no compatible clean-audit resolution under the frozen contract; the lifecycle ended BLOCKED before Release.

The handoff failure was a real Finish → QA compatibility defect, not a missing product feature or an early governance stop. Downstream QA challenged what the upstream stage supplied. Repairing the document roles restored intake, but did not erase the original rejection.

The functional results did not grant release acceptance. The audit finding involved braces 3.0.3 through Stylelint/micromatch development tooling. The retained reports distinguish one root advisory and seven affected dependency findings, rather than seven demonstrated exploits. No HookScope runtime exploit was demonstrated. The investigated upstream resolutions did not provide a compatible clean-audit path under the frozen contract.

Finish preserved the passed observations and investigated the blocker without pretending a failed mandatory audit had passed. The frozen contract did not authorize dropping the tool, suppressing the finding or silently accepting risk. The result was a policy deadlock: a completed functional candidate could not satisfy the release policy within the established repair scope.

## Run 2: after remediation

We kept those failures and remediated the delivery system. The rebuild reused the product inputs, not the first implementation. Startup completed; Finish submitted a candidate after 17 product tests and five browser journeys passed. QA exercised the actual extracted accepted package with its own external fixture and completed 22 expected/actual comparisons.

QA did not substitute builder PASS reports for acceptance or edit the candidate. Release then delivered the accepted ZIP bytes exactly to the authorized local destination. Public distribution and deployment were intentionally outside that target, rather than attempted and failed.

One Startup disposition-approval resume retained seven qualification groups without rerunning completed qualification. That is a concrete reuse observation, not a token-savings benchmark. The 59 first-run product tests and 22 second-run comparisons use different units and scope; they are not a first/second numerical quality comparison.

## Methodology and limits

This is one maker-run project, not a controlled A/B experiment or customer ROI study. Runtime, implementation and operator decisions changed. Second-run QA made fresh observations with its own fixture, but roles shared the same chat/agent context: process independence, limited contextual independence. Supporting Recorder telemetry missed a QA checkpoint and could not finalize a continuous record; this did not prevent product lifecycle completion. The checkpoint defect was subsequently fixed in v0.2.1 with targeted regression tests, without a third lifecycle run or reconstruction of the frozen historical recording. No measured token, cost or comparable timing savings are available.

Remote CI and optional trusted HTTPS success were not executed in the second run. The first-run manual BLOCKED observation was a fallback after Recorder rejected its checkpoint attempt; it is not proof of an accepted Recorder checkpoint. Product outcomes remain grounded in the final stage artifacts.

## What this means for a buyer

For someone using coding agents, the lesson is practical: a downstream acceptance stage must be able to challenge an upstream completion claim; evidence should survive interruptions; security findings need explicit finite decisions rather than silent waivers or permanent deadlocks; and delivery should preserve the candidate QA actually accepted. ASDS provides reusable structure around those boundaries. It complements your agent, CI and engineering judgment.

Choose the stage that addresses your workflow gap: Startup for the engineering foundation, Finish for completing agreed scope, QA for candidate acceptance, and Release for delivering accepted artifacts.

[Return to the overview](README.md).
