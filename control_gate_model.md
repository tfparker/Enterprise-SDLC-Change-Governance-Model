# Control Gate Model

This document defines the control gate model for a tool-agnostic SDLC change governance operating model.

Control gates define the minimum evidence, ownership, review, approval, and risk-disposition conditions required before a change can move forward in the lifecycle.

The purpose of a control gate is not to slow delivery. The purpose is to prevent unclear ownership, incomplete evidence, unresolved risk, or weak validation from being treated as release-ready.

##

## Purpose

A governed SDLC process should not move forward only because a task was completed, a status was updated, or a deadline arrived.

A change should move forward because the required governance conditions have been met.

Control gates help confirm:

- the business need is understood
- ownership is clear
- requirements are documented
- risk is classified
- testing expectations are defined
- evidence is sufficient
- defects are dispositioned
- approvals are captured
- production readiness is supported
- post-production outcomes are reviewed
- closure is justified

##

## Core Principle

A workflow status records movement.

A control gate justifies movement.

The workflow tool may show that a change moved from one stage to another, but the control gate should show why that movement was appropriate.

##

## Control Gate Principles

### 1. Evidence Before Movement

A change should not advance unless required evidence exists or an approved exception is documented.

Evidence may include requirements, test results, approvals, defect dispositions, release-readiness checklists, implementation notes, or post-production validation.

### 2. Ownership Must Be Explicit

Every meaningful change should have clear ownership.

At minimum, ownership should be clear for:

- business outcome
- requirements
- technical execution
- test execution
- defect disposition
- risk acceptance
- release readiness
- post-production validation
- final closeout

### 3. Approval Should Match Risk

Not every change requires the same approval depth.

Governance should scale based on:

- financial reporting impact
- regulatory or compliance impact
- customer or operational impact
- data integrity impact
- production system impact
- reversibility
- downstream dependency
- defect severity
- organizational sensitivity
- timing pressure
- residual risk

### 4. Exceptions Must Be Visible

A change may deviate from the standard lifecycle, but it should not deviate silently.

Exceptions should include:

- reason for exception
- affected control expectation
- approving owner
- residual risk
- compensating control, if any
- follow-up action
- review or expiration date, if applicable

### 5. Signoff Does Not Replace Evidence

A business or technology approval is not a substitute for sufficient evidence.

Approval should be supported by traceable requirements, test results, defect dispositions, release-readiness information, or a documented exception.

### 6. Release Readiness Is Separate From Completion

Development completion, SIT completion, and UAT completion do not automatically mean production release readiness.

Production release readiness requires a separate decision that considers evidence, residual defects, dependencies, implementation risk, communication needs, and post-release validation.

### 7. Closeout Requires Outcome Review

A change should not close merely because it was deployed.

Production closeout should confirm that the implementation outcome was reviewed, post-production issues were identified or ruled out, and follow-up actions were assigned or closed.

##

# Standard Lifecycle Gates

The following gates support the illustrative governed SDLC lifecycle:

```text
Intake Review
→ Draft BRD & FRD
→ Requirements Review
→ Build / Configuration
→ Governance Review & Approval
→ Development
→ SIT Creation, Review & Approval
→ UAT Ready
→ UAT In Progress
→ UAT Evidence Review
→ UAT Completion
→ Production Release Readiness
→ Production Deployment & Implementation
→ Post-Implementation Review & Approval
→ Post-Production Issue Identification
→ Production Closeout
````

##

## 1. Intake Gate

### Purpose

Determine whether a proposed change is sufficiently defined to enter the governed SDLC lifecycle.

### Movement Controlled

Pre-intake / request creation → Intake Review

### Minimum Gate Criteria

* business objective identified
* requesting owner identified
* affected process, system, data flow, or reporting area identified
* initial scope documented
* expected outcome described
* initial risk or sensitivity noted
* target timing or urgency captured
* known dependencies identified, where applicable

### Required Evidence

* change request or intake record
* business need summary
* affected process/system/reporting area
* initial owner assignment
* preliminary risk or impact notes

### Primary Owner

Change Requestor / Business Owner

### Supporting Stakeholders

Business Analyst, Product Owner, Technology Owner, Data Owner, Risk or Control Partner

### Gate Decision

The change may proceed if it has enough information to support initial governance review.

The change should be returned or held if ownership, scope, affected area, or business purpose is unclear.

##

## 2. BRD / FRD Draft Gate

### Purpose

Confirm that the intake concept has been translated into structured business and functional requirements.

### Movement Controlled

Intake Review → Draft BRD & FRD → Requirements Review

### Minimum Gate Criteria

* draft BRD exists
* draft FRD exists, where applicable
* initial acceptance criteria documented
* assumptions and dependencies captured
* open questions documented
* downstream reporting, reconciliation, data quality, or operational impact considered
* business owner or LOB reviewer confirms the draft is ready for requirements review

### Required Evidence

* draft BRD
* draft FRD
* acceptance criteria
* assumption / dependency log
* open question log
* affected process or reporting impact notes

### Primary Owner

Business Analyst / Product Owner

### Supporting Stakeholders

Business Owner, Technology Owner, Data Owner, Risk or Control Partner, Operations Representative

### Gate Decision

The change may proceed to requirements review if the documentation is sufficiently complete for review, challenge, sizing, and validation planning.

The change should not proceed if the requirements are vague, untestable, or materially incomplete.

##

## 3. Requirements Review Gate

### Purpose

Confirm that the requirements are complete, testable, understood by delivery stakeholders, and suitable for controlled execution.

### Movement Controlled

Requirements Review → Build / Configuration or Governance Review & Approval

### Minimum Gate Criteria

* business requirements reviewed
* functional requirements reviewed
* acceptance criteria confirmed
* affected systems, reports, controls, or data flows identified
* known dependencies documented
* testing expectations identified
* risk classification reviewed or updated
* open questions documented with owner and target resolution path

### Required Evidence

* reviewed BRD / FRD
* comments or review notes
* updated acceptance criteria
* dependency notes
* testing scope assumptions
* risk classification notes
* documented open items

### Primary Owner

Product Owner / Business Analyst

### Supporting Stakeholders

Business Owner, Technology Owner, Data Owner, Risk or Control Partner, QA/SIT Lead, UAT Coordinator

### Gate Decision

The change may proceed when requirements are sufficiently clear to support governance review, build/configuration, or development.

The change should be held if the team cannot determine what will be built, how it will be tested, or what business outcome will be validated.

##

## 4. Governance Review & Approval Gate

### Purpose

Determine whether the change is approved to proceed through the controlled delivery path.

This gate may include review of requirements, sizing, risk, prioritization, dependency, funding, release feasibility, control implications, or executive sensitivity depending on the organization.

### Movement Controlled

Requirements Review / Build / Configuration → Governance Review & Approval → Development

### Minimum Gate Criteria

* requirements sufficiently reviewed
* business owner confirmed
* technology impact understood at an appropriate level
* risk classification confirmed or updated
* required approvals identified
* delivery path defined
* critical dependencies surfaced
* control or compliance implications considered
* approval, deferral, rejection, or return-for-clarification decision documented

### Required Evidence

* governance review notes
* approval record
* risk classification
* sizing / impact assessment, where applicable
* dependency notes
* required gate path
* decision record

### Primary Owner

Governance Owner / Product Owner / Program Lead

### Supporting Stakeholders

Business Owner, Technology Owner, Risk or Control Partner, Data Owner, Release Manager, PMO

### Gate Decision

The change may proceed to development if it has the required approval and governance path.

The change should be returned, deferred, or rejected if scope, risk, ownership, sizing, or control impact is unresolved.

---

## 5. Development Entry Gate

### Purpose

Confirm that development or configuration work may begin under the approved scope and governance conditions.

### Movement Controlled

Governance Review & Approval → Development

### Minimum Gate Criteria

* governance approval captured, if required
* development scope understood
* approved requirements or authorized baseline identified
* technology owner assigned
* dependencies understood
* defect tracking method identified
* scope-change handling expectations defined

### Required Evidence

* approved requirements or authorized baseline
* development work item
* assigned technology owner
* dependency notes
* scope-change handling notes
* linkage to change record

### Primary Owner

Technology Owner / Development Lead

### Supporting Stakeholders

Product Owner, Business Analyst, Business Owner, QA/SIT Lead, Data Owner

### Gate Decision

Development may begin if the work is authorized, traceable, and sufficiently defined.

Development should not begin if governance approval is required but missing, if the change lacks ownership, or if requirements are too unstable to support controlled build.

---

## 6. Development Exit Gate

### Purpose

Confirm that development or configuration work is complete enough to enter technical/system validation.

### Movement Controlled

Development → SIT Creation, Review & Approval

### Minimum Gate Criteria

* development or configuration completed
* scope changes documented
* known development defects documented or resolved
* technical notes captured, where appropriate
* linkage to approved requirements maintained
* SIT scenarios can be prepared or executed

### Required Evidence

* development completion note
* linked development item
* defect log, if applicable
* scope-change notes
* technical implementation notes, where appropriate
* readiness confirmation for SIT

### Primary Owner

Technology Owner / Development Lead

### Supporting Stakeholders

QA/SIT Lead, Business Analyst, Product Owner, Data Owner

### Gate Decision

The change may proceed to SIT if the build/configuration is complete enough for system or integration testing.

The change should not proceed if defects, undocumented scope changes, or incomplete build activity would make SIT unreliable.

##

## 7. SIT Gate

### Purpose

Confirm that the change has been technically or system-validated before business UAT begins or is treated as valid.

### Movement Controlled

SIT Creation, Review & Approval → UAT Ready

### Minimum Gate Criteria

* SIT scenarios documented
* expected results defined
* actual results captured
* pass/fail outcomes recorded
* defects documented and dispositioned
* SIT completion or exception approved
* open SIT items communicated to UAT stakeholders
* UAT validity not compromised by unresolved SIT items

### Required Evidence

* SIT test scenarios
* SIT execution evidence
* defect references
* defect disposition
* SIT completion summary
* approval or exception record

### Primary Owner

QA/SIT Lead / Technology Owner

### Supporting Stakeholders

Development Lead, Business Analyst, Product Owner, Data Owner, UAT Coordinator

### Gate Decision

The change may proceed to UAT when SIT has confirmed the change is technically ready for business validation.

The change should not proceed if unresolved SIT defects could invalidate UAT results, affect downstream processing, or change expected business behavior.

##

## 8. UAT Readiness Gate

### Purpose

Confirm that business validation can begin with sufficient scope, data, instructions, ownership, and evidence expectations.

### Movement Controlled

SIT / SIT Exception → UAT Ready → UAT In Progress

### Minimum Gate Criteria

* UAT scope defined
* UAT scenarios prepared
* expected outcomes documented
* testers identified
* test data or environment available
* evidence requirements communicated
* defect logging process identified
* known SIT limitations disclosed

### Required Evidence

* UAT test plan or scenario list
* expected results
* tester list or role assignment
* test data/environment notes
* evidence instructions
* known limitations or exceptions

### Primary Owner

UAT Coordinator / Business Owner

### Supporting Stakeholders

Business Testers, Business Analyst, Product Owner, Technology Owner, Risk or Control Partner

### Gate Decision

UAT may begin when testers can perform meaningful validation and capture evidence.

UAT should not begin if test scenarios, data, expected outcomes, or evidence expectations are unclear.

##

## 9. UAT Evidence Gate

### Purpose

Determine whether UAT evidence is sufficient, traceable, and decision-useful.

### Movement Controlled

UAT In Progress → UAT Evidence Review → UAT Completion

### Minimum Gate Criteria

* UAT results captured
* expected and actual results documented
* pass/fail/blocker outcomes recorded
* failed or blocked tests dispositioned
* defects referenced
* open issues assigned or accepted
* business review completed
* evidence stored or linked in an accessible location

### Required Evidence

* UAT execution results
* screenshots or supporting evidence, where appropriate
* defect references
* defect disposition
* business signoff or rejection
* UAT completion summary

### Primary Owner

Business Owner / UAT Coordinator

### Supporting Stakeholders

Business Testers, Business Analyst, Product Owner, Technology Owner, Risk or Control Partner

### Gate Decision

The change may proceed to UAT completion if evidence supports business acceptance or documented risk acceptance.

The change should not proceed if evidence is incomplete, failed tests are unresolved, or business validation cannot be substantiated.

##

## 10. UAT Completion Gate

### Purpose

Confirm that UAT is formally complete, rejected, deferred, or returned for remediation.

### Movement Controlled

UAT Evidence Review → UAT Completion → Production Release Readiness

### Minimum Gate Criteria

* UAT execution complete or exception documented
* defects dispositioned
* business owner decision documented
* rejected or deferred items identified
* residual risk understood
* release-readiness eligibility determined

### Required Evidence

* UAT completion record
* business approval or rejection
* defect disposition summary
* residual risk notes
* open follow-up items
* remediation record, if required

### Primary Owner

Business Owner

### Supporting Stakeholders

UAT Coordinator, Product Owner, Business Analyst, Technology Owner, Risk or Control Partner

### Gate Decision

The change may proceed to release-readiness review if UAT completion supports production consideration.

The change should be returned or held if UAT failure, incomplete evidence, unresolved blockers, or unacceptable residual risk prevents release consideration.

##

## 11. Production Release Readiness Gate

### Purpose

Determine whether the change is ready for production implementation.

### Movement Controlled

UAT Completion → Production Release Readiness → Production Deployment & Implementation

### Minimum Gate Criteria

* UAT completion or approved exception captured
* required approvals completed
* release scope confirmed
* open defects dispositioned
* dependencies confirmed
* implementation plan documented
* release timing identified
* communication needs assessed
* rollback or contingency considerations documented
* post-release validation owner assigned
* residual risk accepted where applicable

### Required Evidence

* release readiness checklist
* UAT completion summary
* approval record
* defect/accepted-risk summary
* implementation plan
* dependency confirmation
* rollback or contingency notes
* communication plan, if applicable
* post-release validation assignment

### Primary Owner

Release Manager / Technology Owner

### Supporting Stakeholders

Business Owner, Product Owner, Business Analyst, Risk or Control Partner, Operations Representative, Data Owner

### Gate Decision

The change may proceed to production deployment if release readiness is supported by evidence and approval.

The change should not proceed if readiness depends on assumptions, unresolved blockers, unclear ownership, or unaccepted residual risk.

##

## 12. Production Deployment Gate

### Purpose

Confirm that the approved production implementation was executed, documented, and ready for post-implementation review.

### Movement Controlled

Production Release Readiness → Production Deployment & Implementation → Post-Implementation Review

### Minimum Gate Criteria

* deployment executed or deferred
* implementation outcome documented
* production validation performed or assigned
* incidents, deviations, or failed steps captured
* communication completed, if applicable
* rollback or contingency action documented, if used

### Required Evidence

* deployment record
* implementation outcome
* production validation result or pending assignment
* incident or defect references, if applicable
* communication note, if applicable
* rollback/contingency record, if applicable

### Primary Owner

Technology Owner / Release Manager

### Supporting Stakeholders

Business Owner, Operations Representative, Product Owner, Risk or Control Partner, Data Owner

### Gate Decision

The change may proceed to post-implementation review if the production outcome is known or validation is assigned.

The change should not proceed to closure solely because deployment occurred.

##

## 13. Post-Implementation Review Gate

### Purpose

Confirm whether the change behaved as expected after implementation and whether follow-up action is required.

### Movement Controlled

Production Deployment & Implementation → Post-Implementation Review & Approval → Post-Production Issue Identification / Production Closeout

### Minimum Gate Criteria

* production outcome reviewed
* expected business or operational result assessed
* defects, incidents, or deviations documented
* unresolved follow-up items assigned
* lessons learned captured, where applicable
* business or governance approval captured, where required

### Required Evidence

* post-implementation review notes
* production validation evidence
* incident/defect references
* follow-up action log
* business confirmation
* closure approval, where applicable

### Primary Owner

Business Owner / Governance Owner

### Supporting Stakeholders

Technology Owner, Release Manager, Product Owner, Risk or Control Partner, Operations Representative

### Gate Decision

The change may proceed to closeout if the production outcome is acceptable and follow-up items are assigned or resolved.

The change should remain open, create follow-up records, or return to remediation if production issues affect the intended outcome.

##

## 14. Production Closeout Gate

### Purpose

Confirm that the change record is complete, evidenced, and ready for closure.

### Movement Controlled

Post-Implementation Review / Post-Production Issue Identification → Production Closeout

### Minimum Gate Criteria

* implementation outcome documented
* production validation completed or follow-up assigned
* post-production issues identified and dispositioned
* open actions linked or closed
* approvals captured
* final closure note completed
* evidence retained or referenced

### Required Evidence

* final closure note
* PIR approval or completion note
* linked follow-up items
* defect/incident disposition
* evidence references
* closure approval, where applicable

### Primary Owner

Business Owner / Governance Owner

### Supporting Stakeholders

Technology Owner, Release Manager, Product Owner, Risk or Control Partner

### Gate Decision

The change may close when the record supports a reasonable independent review of what was requested, changed, tested, released, validated, and resolved.

The change should not close if material outcomes, defects, follow-ups, or approvals remain undocumented.

##

# Exception and Edge-Case Gate Patterns

The following sections address common real-world conditions that may require risk-based governance treatment.

These are not separate lifecycle stages in every organization. They are patterns that should trigger additional review, documentation, ownership, or approval.

##

## Parallel SIT & UAT

### Governance Issue

SIT and UAT may occur in parallel or partially overlap due to timeline pressure, environment constraints, iterative delivery, release-window dependency, or organizational preference.

Parallel SIT/UAT can be valid, but it introduces a risk that business users are validating behavior before technical or integration readiness is fully confirmed.

### Governance Expectation

Parallel SIT and UAT should be treated as a risk-based delivery pattern, not as an undocumented shortcut.

The change record should document:

* why parallel execution is necessary
* which SIT scenarios are complete
* which SIT scenarios remain open
* which UAT scenarios depend on unresolved SIT outcomes
* whether UAT evidence is provisional or final
* whether unresolved SIT findings could invalidate UAT results
* business owner awareness of the overlap
* risk/control review, where required
* approval to proceed under parallel testing conditions

### Gate Requirement

Before production release readiness, the record should confirm:

* SIT completion or approved SIT exception
* UAT evidence remains valid after SIT completion
* unresolved SIT findings are dispositioned
* business owner accepts any residual risk
* release approver understands the parallel testing condition

### Blocking Conditions

Parallel SIT/UAT should block release if:

* unresolved SIT defects could change expected UAT outcomes
* UAT scenarios are invalidated by later SIT findings
* downstream processing has not been validated
* business owner is unaware of the testing overlap
* release approvers do not see the residual risk

##

## Development Before Governance Approval

### Governance Issue

Development may begin before documented governance approval due to urgency, capacity availability, informal prioritization, or assumptions that approval is inevitable.

This creates risk when build activity outruns approved scope, requirements, ownership, or risk review.

### Governance Expectation

Development before governance approval should be documented as either:

* formally approved early-start work
* limited discovery / technical assessment
* unauthorized deviation requiring remediation
* emergency or break-fix action
* rework risk accepted by the accountable owner

### Gate Requirement

The record should document:

* why development began early
* whether work was exploratory or production-directed
* who authorized the early start
* whether requirements were stable
* whether risk classification was known
* whether rework risk was accepted
* whether governance approval later confirmed, changed, or rejected the work

### Blocking Conditions

The change should not proceed to release if:

* development scope does not match approved requirements
* no accountable owner accepted early-start risk
* governance approval materially changes the requirement
* development created unreviewed production risk
* evidence does not distinguish discovery from implementation

##

## Change and Risk Ownership

### Governance Issue

A change may have many participants but no clear owner for the outcome or residual risk.

This creates ambiguity when defects, exceptions, delays, or release decisions arise.

### Governance Expectation

Every governed change should identify ownership for:

* business outcome
* technical implementation
* requirements
* UAT
* defect disposition
* risk acceptance
* release readiness
* post-production validation
* closure

### Gate Requirement

The change should not pass key gates unless accountable ownership is clear.

At minimum:

| Ownership Area        | Required Owner                     |
| --------------------- | ---------------------------------- |
| Business outcome      | Business Owner                     |
| Requirements          | Product Owner / Business Analyst   |
| Technical execution   | Technology Owner                   |
| UAT                   | Business Owner / UAT Coordinator   |
| Defect disposition    | Business Owner / Technology Owner  |
| Risk acceptance       | Authorized Business / Risk Owner   |
| Release readiness     | Release Manager / Technology Owner |
| Production validation | Business Owner / Operations Owner  |
| Closeout              | Business Owner / Governance Owner  |

### Blocking Conditions

The change should be held if:

* residual risk has no accountable owner
* UAT approval is unclear
* defect acceptance is not assigned
* production validation owner is missing
* closure owner cannot confirm outcome

##

## UAT Without Production-Quality Comparison Data

### Governance Issue

UAT may occur with incomplete, synthetic, masked, stale, limited, or non-production-like data.

This can reduce the reliability of business validation, especially for finance reporting, reconciliations, data quality, operational workflows, and downstream dependencies.

### Governance Expectation

If UAT does not use production-quality comparison data, the evidence should disclose the limitation and explain how validation remains meaningful.

### Gate Requirement

The record should document:

* type of data used
* known limitations
* scenarios that could not be validated
* comparison method used
* compensating validation, if any
* risk of false pass / incomplete validation
* business owner acceptance
* additional post-production validation required, if applicable

### Blocking Conditions

UAT data limitations should block release if:

* core business outcome cannot be validated
* financial or regulatory reporting impact cannot be assessed
* reconciliation or ledger impact is untested
* test data materially differs from production behavior
* no compensating validation exists
* business owner has not accepted the limitation

##

## Break-Fix Changes

### Governance Issue

Break-fix changes may require faster execution to restore service, correct production defects, or remediate operational disruption.

Speed may be necessary, but evidence and ownership should not disappear.

### Governance Expectation

Break-fix changes should use a risk-adjusted path.

The process may be compressed, but the record should still capture:

* problem being fixed
* urgency
* impacted process or system
* owner
* implementation action
* testing performed
* approval or emergency authorization
* production validation
* follow-up documentation
* root cause or recurrence consideration, where appropriate

### Gate Requirement

Before closeout, the break-fix record should confirm:

* issue was resolved or mitigated
* validation was performed
* residual risk is known
* follow-up items are assigned
* any skipped standard steps were documented
* retrospective review occurred where required

### Blocking Conditions

Break-fix closeout should be held if:

* production outcome is unknown
* fix was applied without validation
* recurring defect risk is not addressed
* issue created downstream reporting or operational impact
* no owner accepts residual risk

##

## External Regulatory, Compliance, or Control-Driven Execution

### Governance Issue

External requirements may require execution that exceeds, compresses, or conflicts with the organization’s standard SDLC process.

Examples include regulatory deadlines, audit remediation commitments, compliance mandates, legal obligations, industry requirements, or external control findings.

### Governance Expectation

When external factors require execution outside the defined SDLC path, the change should be governed through explicit exception handling.

The record should document:

* external driver
* required timing
* impacted standard SDLC steps
* risk of deviation
* compensating controls
* approving authority
* evidence to be completed before or after implementation
* post-implementation validation requirements
* issue or regulatory commitment linkage, where applicable

### Gate Requirement

The change may proceed if the organization documents why standard SDLC steps cannot fully apply and what compensating governance will be used.

### Blocking Conditions

The change should not proceed silently if:

* external requirement is asserted but not documented
* SDLC deviation has no approval
* compensating control is missing
* residual risk is not accepted
* post-implementation validation is not required or assigned

##

## Sensitive or Organizationally Critical Changes

### Governance Issue

Some changes carry significance beyond normal delivery risk because they affect executive reporting, regulatory commitments, financial statements, liquidity, customer obligations, board visibility, or enterprise reputation.

These changes may require CFO, C-suite, senior risk, steering committee, or executive sponsorship.

### Governance Expectation

Sensitive or critical changes should have enhanced visibility, approval, and documentation.

The record should identify:

* why the change is sensitive
* executive sponsor or accountable senior owner
* business or financial consequence
* regulatory or reputational exposure
* required approval level
* communication expectations
* escalation path
* post-implementation review depth

### Gate Requirement

The change should not move to release readiness unless required senior-level approval and risk acceptance are captured or explicitly waived.

### Blocking Conditions

Release should be held if:

* executive sponsor is unclear
* approval level does not match sensitivity
* financial or regulatory impact is not understood
* communication obligations are unresolved
* post-release validation owner is missing

##

## Negative UAT

### Governance Issue

Negative UAT means the change does not meet expected business outcomes, generates failed scenarios, reveals defects, or cannot be validated as acceptable.

Negative UAT is not a documentation failure. It is a decision point.

### Governance Expectation

Negative UAT should trigger clear disposition:

* remediate and retest
* accept defect / residual risk
* defer defect with owner and target path
* reject release
* reduce scope
* return to requirements
* create follow-up change
* escalate for decision

### Gate Requirement

The record should include:

* failed scenarios
* expected vs actual results
* severity / impact assessment
* affected requirement
* defect reference
* business owner decision
* technology owner input
* risk/control review, where required
* retest evidence, if remediated
* release implication

### Blocking Conditions

Negative UAT should block release if:

* failed scenario affects core business outcome
* financial or regulatory reporting risk remains unresolved
* defect invalidates acceptance criteria
* business owner does not accept residual risk
* no remediation or deferral path exists
* release approvers are not aware of the failure

##

## Deferred UAT Defects

### Governance Issue

A UAT defect may be deferred when the issue is known, documented, risk-assessed, and accepted before release.

Deferral is a governance decision, not a way to hide failed validation.

### Governance Expectation

Deferred UAT defects should include:

* defect description
* affected requirement or test scenario
* severity and impact
* reason for deferral
* business owner acceptance
* technology owner input
* risk/control review, where applicable
* follow-up record
* expected remediation timing, if known
* workaround or compensating control, if applicable
* release impact assessment

### Gate Requirement

A release may proceed with deferred defects only if:

* residual risk is accepted
* release approvers are aware
* the defect does not invalidate the core business outcome
* owner and follow-up path are documented
* remediation does not depend on informal tracking

### Blocking Conditions

A deferred defect should block release if it:

* prevents a core business process
* creates unresolved financial or regulatory reporting risk
* materially affects reconciliation, ledger, or subledger integrity
* invalidates UAT evidence
* affects downstream consumers without accepted mitigation
* lacks an accountable owner
* lacks business approval or risk acceptance

##

## Changes With No Development Required

### Governance Issue

Some changes do not require software development but may still affect production behavior, reporting, controls, access, data, or operational outcomes.

Examples include configuration updates, reference data changes, workflow routing changes, parameter changes, mapping updates, entitlement changes, or manual data remediation.

### Governance Expectation

No-development changes should not bypass governance merely because no code is built.

The record should document:

* change type
* affected process/system/reporting area
* business owner
* implementation action
* validation method
* approval requirement
* rollback or correction approach
* post-change validation

### Gate Requirement

The change may proceed if ownership, approval, validation, and release impact are clear.

### Blocking Conditions

The change should be held if:

* production effect is not understood
* validation method is missing
* owner is unclear
* approval path is undefined
* manual update risk is not controlled
* rollback/correction approach is unknown

##

## UAT-Only Changes

### Governance Issue

Some changes may not require development or SIT but still require business validation, such as reporting configuration, process changes, workflow routing, parameter updates, manual remediation, dashboard logic review, or operational procedure updates.

### Governance Expectation

UAT-only changes should define why development and SIT are not required and what UAT is expected to prove.

### Gate Requirement

The record should document:

* rationale for UAT-only path
* affected requirement or business process
* validation scope
* expected results
* test data or comparison method
* business owner signoff
* release or operationalization criteria

### Blocking Conditions

The UAT-only path should not be used if:

* technical behavior changed but SIT was skipped
* downstream system impact exists
* production configuration changed without validation
* UAT cannot prove the intended outcome
* release risk is not assessed

##

## Known UAT Quality Issues

### Governance Issue

Some organizations operate with known UAT weaknesses, including inconsistent test design, incomplete evidence, rushed business signoff, poor test data, unclear defect disposition, or limited tester availability.

In such environments, UAT completion alone may not be a reliable readiness signal.

### Governance Expectation

When known UAT quality issues exist, additional evidence or compensating controls may be required.

Examples include:

* stricter UAT templates
* independent evidence review
* scenario traceability to requirements
* required defect disposition summary
* business owner attestation of review
* post-release validation plan
* heightened release-readiness review
* sampling by governance or control partners

### Gate Requirement

Release readiness should consider whether UAT quality is sufficient for the risk level of the change.

### Blocking Conditions

Release should be held if:

* UAT evidence is materially incomplete
* failed tests are not dispositioned
* business signoff is unsupported
* core scenarios are missing
* known UAT weaknesses affect a high-risk change
* compensating validation is absent

##

## Scope Expansion After Approval

### Governance Issue

A change may expand after approval due to newly discovered requirements, stakeholder requests, technical findings, or bundling pressure.

Scope expansion can undermine original risk classification, testing scope, approvals, and release readiness.

### Governance Expectation

Material scope expansion should trigger supplemental governance review.

The record should document:

* original approved scope
* proposed expanded scope
* reason for expansion
* impact on requirements
* impact on risk classification
* impact on SIT/UAT
* impact on release timing
* approval of revised scope

### Gate Requirement

The change may continue only if the expanded scope is reviewed and accepted.

### Blocking Conditions

Release should be held if:

* delivered scope differs materially from approved scope
* testing does not cover expanded scope
* risk classification was not revisited
* approvers did not approve revised scope
* downstream impact changed

##

## Business Signoff Without Evidence

### Governance Issue

A business owner may approve a change without sufficient test evidence, especially under time pressure.

This creates the appearance of acceptance without proof of validation.

### Governance Expectation

Business signoff should be supported by evidence or a documented exception.

The record should show:

* what was reviewed
* what evidence supports approval
* what limitations exist
* whether the business owner accepts any evidence gaps
* whether additional post-release validation is required

### Gate Requirement

If evidence is incomplete, the approval should state what risk is being accepted.

### Blocking Conditions

Release should be held if:

* signoff exists but no evidence supports it
* core scenarios were not validated
* business owner is unaware of evidence gaps
* risk acceptance is implicit rather than documented
* release approvers cannot determine what was actually tested

##

## Evidence Stored Outside the System of Record

### Governance Issue

Evidence may exist in email, shared drives, Teams/Slack messages, spreadsheets, screenshots, meeting notes, or separate test-management tools.

This may be acceptable, but the change record must make evidence findable and reviewable.

### Governance Expectation

The change record should identify where evidence is stored and how it supports the approval decision.

### Gate Requirement

The record should capture:

* evidence location
* evidence owner
* summary of evidence
* relationship to test scenario or requirement
* date or version reference
* access consideration, where applicable

### Blocking Conditions

Release or closeout should be held if:

* evidence exists but cannot be located
* evidence is not linked or summarized
* evidence owner is unclear
* approvers cannot review supporting material
* evidence is stored in a way that prevents auditability

##

## Environment Constraint or Test Environment Mismatch

### Governance Issue

Testing may occur in environments that do not fully represent production.

Examples include incomplete interfaces, stale data, masked data, unavailable downstream systems, partial batch processing, configuration mismatch, or missing integrations.

### Governance Expectation

Environment limitations should be disclosed and assessed.

The record should document:

* environment limitation
* affected scenarios
* validation impact
* compensating test approach
* residual risk
* business acceptance
* post-production validation need

### Gate Requirement

The change may proceed only if the limitation does not invalidate the core validation or if residual risk is accepted.

### Blocking Conditions

Release should be held if:

* core behavior cannot be validated
* downstream dependency is untested
* test environment materially differs from production
* no compensating validation exists
* business owner does not accept the limitation

##

## Downstream Dependency Not Validated

### Governance Issue

Changes often affect downstream reports, reconciliations, consumers, interfaces, ledgers, subledgers, operational workflows, or data quality processes.

Failure to validate downstream impact can create delayed production defects.

### Governance Expectation

If a change affects downstream dependency, readiness should include downstream validation or documented acceptance of unvalidated dependency risk.

### Gate Requirement

The record should document:

* downstream consumers or processes
* expected downstream impact
* validation performed
* validation not performed and why
* owner accepting downstream risk
* follow-up validation plan, if applicable

### Blocking Conditions

Release should be held if:

* downstream dependency is material
* no validation occurred
* impact is unknown
* downstream owner was not consulted
* financial, regulatory, or operational consequences are possible
* no residual risk acceptance exists

##

## Manual Data Remediation / Data Correction Changes

### Governance Issue

Manual data remediation or correction may not involve code but can materially affect balances, reporting inputs, reference data, reconciliations, customer records, or operational outcomes.

### Governance Expectation

Manual data changes should be governed based on impact, not based on whether development is required.

### Gate Requirement

The record should include:

* data population affected
* reason for remediation
* source of truth
* correction method
* maker/checker or independent review, where appropriate
* validation result
* approval owner
* downstream impact
* evidence of before/after state
* rollback or reversal considerations

### Blocking Conditions

The change should be held if:

* source of truth is unclear
* correction cannot be validated
* impact population is unknown
* no approval exists
* no independent review exists for material changes
* downstream reporting impact is unresolved

##

## Reporting Logic Changes

### Governance Issue

Changes to reporting logic, calculations, mappings, classifications, filters, rules, or reference data can affect financial, regulatory, operational, or executive reporting.

### Governance Expectation

Reporting logic changes require traceability from requirement to logic change to validation evidence.

### Gate Requirement

The record should document:

* affected report, metric, rule, field, mapping, or calculation
* business rationale
* before/after logic summary
* impacted downstream users
* test scenarios
* expected vs actual results
* reconciliation or tie-out evidence, where applicable
* approval from reporting or data owner
* post-release validation

### Blocking Conditions

Release should be held if:

* logic change is not documented
* validation does not test material scenarios
* downstream users are not considered
* reconciliation impact is unknown
* reporting owner approval is missing
* change affects regulatory or financial reporting without appropriate review

##

## Rollback Not Feasible

### Governance Issue

Some changes cannot be cleanly rolled back, especially data remediation, reporting logic changes, configuration changes, batch updates, ledger-affecting changes, or changes with downstream consumption.

### Governance Expectation

If rollback is not feasible, release readiness should include contingency planning and explicit risk acceptance.

### Gate Requirement

The record should document:

* why rollback is not feasible
* potential failure impact
* detection method
* remediation approach
* contingency owner
* communication path
* residual risk acceptance
* post-release validation plan

### Blocking Conditions

Release should be held if:

* rollback is assumed but not possible
* no contingency plan exists
* impact of failure is material
* owner has not accepted residual risk
* post-release validation is not assigned

##

## Control or Audit Finding Remediation

### Governance Issue

Some changes exist to remediate audit findings, control issues, regulatory concerns, or internal risk findings.

These changes require traceability between finding, remediation objective, validation, and closure.

### Governance Expectation

Control remediation changes should document how the change addresses the finding or control gap.

### Gate Requirement

The record should include:

* source finding or issue reference
* remediation objective
* control gap being addressed
* requirements
* validation approach
* evidence of remediation
* control owner approval
* audit/risk/compliance review, where applicable
* closure support

### Blocking Conditions

Closure should be held if:

* remediation objective is unclear
* evidence does not address the finding
* control owner approval is missing
* validation does not demonstrate remediation
* follow-up testing or monitoring is required but not assigned

##

## Calendar-Driven Release Pressure

### Governance Issue

Release timing may be driven by month-end, quarter-end, regulatory filing windows, external commitments, vendor windows, freeze periods, or leadership deadlines.

Calendar pressure can override readiness discipline if not controlled.

### Governance Expectation

Timing pressure should be visible, but it should not replace readiness evidence.

### Gate Requirement

The record should document:

* timing driver
* readiness gaps, if any
* residual risk
* owner accepting timing-driven risk
* compensating controls
* post-release monitoring
* escalation approval, where appropriate

### Blocking Conditions

Release should be held if:

* timing is the only release rationale
* readiness gaps are material
* residual risk is not accepted
* no compensating control exists
* critical validation is incomplete
* release could create financial, regulatory, or operational exposure

##

## Materiality Threshold

### Governance Issue

Finance and reporting changes may require different governance depth based on materiality, even if the technical change appears small.

### Governance Expectation

Materiality should influence risk classification, approval level, UAT depth, evidence expectations, release readiness, and post-implementation review.

### Gate Requirement

The record should consider:

* financial statement impact
* regulatory reporting impact
* balance or transaction population affected
* downstream reporting consumers
* reconciliation impact
* error tolerance
* repeatability of impact
* reversibility

### Blocking Conditions

Release should be held if:

* materiality is unknown
* change could materially affect reporting without review
* validation does not cover material scenarios
* approval level does not match potential impact
* post-release validation is not defined

##

## Data Lineage or Source-System Dependency Change

### Governance Issue

A change may affect source-system feeds, data lineage, upstream/downstream transformations, field definitions, mapping logic, or authoritative source usage.

This is especially relevant in finance, risk, regulatory reporting, reconciliation, and executive reporting environments.

### Governance Expectation

Data lineage and source-system changes should include traceability and downstream impact review.

### Gate Requirement

The record should document:

* source system or data feed affected
* downstream consumers
* field, mapping, or transformation change
* lineage impact
* reconciliation or tie-out method
* data owner approval
* reporting owner approval, where applicable
* production validation plan

### Blocking Conditions

Release should be held if:

* authoritative source is unclear
* downstream consumers are not identified
* lineage impact is unknown
* reconciliation method is missing
* data owner approval is absent
* reporting or regulatory impact is unreviewed

##

# Defect Disposition Standards

Defect disposition should be consistent across SIT, UAT, release readiness, and post-production review.

| Disposition         | Meaning                                       | Governance Expectation                                 |
| ------------------- | --------------------------------------------- | ------------------------------------------------------ |
| Resolved            | Defect corrected before release               | Retest evidence should exist                           |
| Accepted            | Known issue accepted by authorized owner      | Risk acceptance should be documented                   |
| Deferred            | Moved to future release or follow-up item     | Owner and remediation path required                    |
| Blocked             | Prevents forward movement                     | Release should not proceed until resolved or escalated |
| Not a Defect        | Reviewed and determined not to be a defect    | Rationale should be documented                         |
| Out of Scope        | Valid issue but outside approved change scope | Follow-up path should be documented if material        |
| Duplicate           | Already tracked elsewhere                     | Related record should be linked                        |
| Cannot Reproduce    | Issue not reproducible                        | Investigation notes should be retained                 |
| Monitoring Required | Issue not blocking but requires observation   | Monitoring owner and period should be defined          |

##

# Gate Decision Outcomes

Each control gate should result in a clear decision.

| Decision                 | Meaning                                                    |
| ------------------------ | ---------------------------------------------------------- |
| Proceed                  | Gate criteria met; change may advance                      |
| Proceed with Conditions  | Change may advance if conditions are tracked and owned     |
| Return for Clarification | Change lacks sufficient definition                         |
| Return for Remediation   | Evidence, defects, or requirements require correction      |
| Defer                    | Change should pause or move to future release              |
| Reject                   | Change should not proceed                                  |
| Escalate                 | Decision requires higher-level review or approval          |
| Exception Approved       | Standard gate not fully met, but residual risk is accepted |
| Blocked                  | Change cannot move forward until issue is resolved         |

A gate decision should be documented with the decision, owner, date, rationale, and any required follow-up.

##

# Minimum Control Gate Record

A control gate record should capture:

* change identifier
* lifecycle stage
* gate being reviewed
* decision
* decision owner
* review date
* evidence reviewed
* open risks
* open defects
* conditions or exceptions
* required approvals
* follow-up actions
* next permitted stage

##

# Summary

Control gates are the decision structure of the governed SDLC lifecycle.

They ensure that movement is supported by evidence, ownership, risk review, approval, and issue disposition.

The central principle is:

A change may deviate from the standard lifecycle, but it should not deviate silently.

Exceptions, compressed paths, deferred defects, parallel testing, sensitive changes, and no-development changes can all be handled within a governed model when the record clearly captures ownership, rationale, residual risk, approval, and follow-up.

