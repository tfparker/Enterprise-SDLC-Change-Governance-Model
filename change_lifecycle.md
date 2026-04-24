## 2. Draft BRD & FRD

### Purpose
Translate the approved intake concept into structured business and functional requirements that can be reviewed, sized, governed, built, tested, and approved.

### Entry Criteria
- Intake review completed
- Business owner identified
- Affected process, system, data flow, or reporting area identified
- Initial scope and expected outcome documented
- Initial risk or control considerations captured

### Required Artifacts / Evidence
- Draft Business Requirements Document
- Draft Functional Requirements Document
- Initial acceptance criteria
- Known assumptions and dependencies
- Initial risk considerations
- Open questions or unresolved design items

### Accountable Owner
Business Analyst / Product Owner

### Supporting Stakeholders
Business Owner, Technology Owner, Data Owner, Risk or Control Partner, Operations Representative

### Exit Criteria
- BRD and FRD are complete enough for formal requirements review
- Requirements are testable or have a documented path to clarification
- Open questions, assumptions, and dependencies are documented
- Potential downstream reporting, reconciliation, data quality, or operational impacts are identified
- Business owner or LOB reviewer has confirmed the draft is ready for requirements review
- Change is ready to enter the governance review process, if required by risk or organizational policy

### Common Failure Points
- Requirements are written as vague requests rather than testable outcomes
- Functional requirements are drafted after development has already started
- Business owner is unclear or passive
- Acceptance criteria are not testable
- Downstream reporting, reconciliation, data quality, or control impacts are not identified
- Oversized changes increase delivery, testing, approval, and release risk
- Open questions remain hidden in emails or meetings instead of being captured in the change record

## 3. Governance Review

### Purpose
Determine whether the change is sufficiently defined, appropriately owned, risk-assessed, and ready to proceed through the controlled SDLC path.

Governance review may include technology sizing, sequencing, prioritization, control review, funding consideration, dependency review, or approval to proceed, depending on the organization.

### Entry Criteria
- Draft BRD and FRD prepared
- Business owner identified
- Initial scope, expected outcome, and acceptance criteria documented
- Known dependencies and risk considerations captured

### Required Artifacts / Evidence
- Draft BRD and FRD
- Initial risk classification
- Technology sizing or impact assessment, where applicable
- Dependency assessment
- Proposed delivery path
- Governance review notes or approval record

### Accountable Owner
Governance Owner / Product Owner / Program Lead

### Supporting Stakeholders
Business Owner, Technology Owner, Risk or Control Partner, Data Owner, Release Manager, PMO

### Exit Criteria
- Change is approved to proceed, deferred, rejected, or returned for clarification
- Risk classification is confirmed or updated
- Required approvals or review path are identified
- Technology sizing or delivery complexity is documented, where applicable
- Required control gates are identified
- Change is ready for development or additional requirements refinement

### Common Failure Points
- Governance review becomes a status meeting rather than a decision point
- Technology sizing is performed without enough requirement clarity
- Risk classification is treated as administrative rather than decision-relevant
- Dependencies are discovered too late
- Approval to proceed is not clearly documented

## 4. Development

### Purpose
Build, configure, or implement the approved change in a controlled manner consistent with the reviewed requirements and governance expectations.

### Entry Criteria
- Governance review completed, if required
- BRD and FRD reviewed or approved according to organizational policy
- Development scope understood
- Technical owner assigned
- Dependencies and assumptions documented

### Required Artifacts / Evidence
- Development work item or implementation record
- Linkage to approved requirements
- Technical notes, where appropriate
- Defect or issue log, if applicable
- Updated requirement notes if scope changes during development

### Accountable Owner
Technology Owner / Development Lead

### Supporting Stakeholders
Business Analyst, Product Owner, Business Owner, Data Owner, QA/SIT Lead

### Exit Criteria
- Development or configuration work completed
- Known development defects documented or resolved
- Scope changes are reviewed and documented
- Change is ready for SIT preparation or execution

### Common Failure Points
- Development begins before requirements are stable
- Scope changes occur without governance review
- Technical assumptions are not communicated to business stakeholders
- Requirements traceability is lost
- Defects are handled informally rather than tracked

## 5. SIT Creation, Review & Approval

### Purpose
Validate that the change functions as expected within the technical, system, integration, data, or process environment before business UAT begins.

### Entry Criteria
- Development or configuration completed
- SIT scenarios identified
- Required test data or environment available
- Technical owner confirms readiness for SIT

### Required Artifacts / Evidence
- SIT test scenarios
- Expected and actual results
- Pass/fail outcomes
- Defect references
- Defect disposition
- SIT completion summary
- Approval or confirmation that the change is ready for UAT

### Accountable Owner
QA/SIT Lead / Technology Owner

### Supporting Stakeholders
Development Lead, Business Analyst, Product Owner, Data Owner, UAT Coordinator

### Exit Criteria
- SIT execution completed or exceptions documented
- Critical defects resolved or formally dispositioned
- SIT results reviewed
- Change approved to proceed to UAT readiness
- Open issues communicated to UAT stakeholders

### Common Failure Points
- SIT is skipped or compressed without documenting risk
- Integration or downstream impacts are not tested
- SIT defects are carried into UAT without clear disposition
- Test data does not represent the business scenario
- UAT begins before technical validation is complete

## 6. UAT

### Purpose
Confirm that the change meets business expectations and is acceptable for production use.

UAT should validate the business outcome, not merely confirm that a technical change was delivered.

### Entry Criteria
- SIT completed or exceptions approved
- UAT scenarios prepared
- Business testers identified
- Test data or test environment available
- Expected outcomes documented
- Evidence expectations communicated

### Required Artifacts / Evidence
- UAT test scenarios
- Expected results
- Actual results
- Pass/fail/blocker status
- Tester name or role
- Execution date
- Defect references, where applicable
- Defect disposition
- Business signoff or rejection
- UAT completion summary

### Accountable Owner
Business Owner / UAT Coordinator

### Supporting Stakeholders
Business Testers, Business Analyst, Product Owner, Technology Owner, Risk or Control Partner

### Exit Criteria
- UAT execution completed
- Failed or blocked test cases dispositioned
- Required evidence reviewed for sufficiency
- Business owner confirms UAT completion
- Change is approved, rejected, deferred, or returned for remediation

### Common Failure Points
- UAT tests what was built rather than what the business needs
- Evidence is incomplete or stored outside the change record
- Failed tests are not clearly dispositioned
- Business signoff occurs without sufficient review
- UAT completion is treated as a calendar milestone rather than an evidence-based decision

## 7. Production Release Readiness & Deployment

### Purpose
Determine whether the change is ready for production implementation and then execute the approved deployment or operationalization plan.

### Entry Criteria
- UAT completed or approved exception documented
- Required approvals captured
- Release scope confirmed
- Open defects dispositioned
- Implementation owner assigned
- Release window or deployment timing identified

### Required Artifacts / Evidence
- Release readiness checklist
- Approval record
- UAT completion summary
- Known defect or accepted-risk summary
- Implementation plan
- Rollback or contingency considerations
- Communication plan, if applicable
- Post-release validation owner

### Accountable Owner
Release Manager / Technology Owner

### Supporting Stakeholders
Business Owner, Product Owner, Business Analyst, Risk or Control Partner, Operations Representative

### Exit Criteria
- Production deployment completed or release deferred
- Deployment outcome documented
- Immediate validation completed or assigned
- Incidents, defects, or deviations captured
- Change is ready for post-implementation review

### Common Failure Points
- Release proceeds because of timeline pressure rather than readiness
- Accepted defects are not clearly owned
- Rollback or contingency considerations are missing
- Post-release validation owner is unclear
- Deployment outcome is not documented

## 8. Post-Production Review & Closeout

### Purpose
Confirm whether the production change behaved as expected, identify post-production issues, document follow-up actions, and close the change only when the outcome is sufficiently reviewed.

### Entry Criteria
- Production deployment completed
- Initial production validation performed or scheduled
- Known defects, incidents, or deviations captured
- Business or operational owner available for outcome review

### Required Artifacts / Evidence
- Production validation result
- Post-implementation review notes
- Defect or incident references, if applicable
- Follow-up action log
- Business confirmation or closure approval
- Lessons learned, if required
- Final closeout note

### Accountable Owner
Business Owner / Governance Owner

### Supporting Stakeholders
Technology Owner, Release Manager, Product Owner, Risk or Control Partner, Operations Representative

### Exit Criteria
- Production outcome reviewed
- Post-production issues identified and dispositioned
- Follow-up actions assigned or linked to new records
- Required approvals captured
- Change record is complete enough for closure
- Change is formally closed

### Common Failure Points
- Change is closed immediately after deployment
- Production issues are tracked informally outside the change record
- Business outcome is not validated after release
- Follow-up ownership is unclear
- Lessons learned are skipped for high-risk or problematic changes

