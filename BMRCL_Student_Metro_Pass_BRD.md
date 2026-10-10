# BUSINESS REQUIREMENTS DOCUMENT (BRD)

## Project Title
**NFC-Enabled Smart Student Metro Pass Management System for BMRCL**

- **Prepared for:** Bangalore Metro Rail Corporation Limited (BMRCL) — Proposed Initiative
- **Project Type:** BCA Final-Year Academic Project
- **Document Version:** 1.0
- **Date:** 9 October 2026

---

## 1. Executive Summary

The NFC-Enabled Smart Student Metro Pass Management System is a proposed digital solution intended for Bangalore Metro Rail Corporation Limited (BMRCL). The project aims to introduce a student-specific metro-pass scheme that could make daily metro travel more affordable for eligible college students.

The proposed system will allow students to apply for a metro pass through a digital platform, enable colleges to verify student eligibility, and allow authorised administrators to approve, manage and monitor passes. An approved pass would be associated with an NFC-enabled college identity card or compatible NFC credential.

Students could tap their NFC card on a compatible reader to verify their pass status. The system would check whether the pass is valid, active and within its authorised travel conditions before displaying an approval or rejection result.

The project addresses a potential gap in student travel concessions and demonstrates how a digital student-pass scheme could be implemented. The initial academic version will use simulated metro-gate validation rather than connecting to actual BMRCL infrastructure.

**Important:** This is a proposed initiative, not a claim that BMRCL has approved or launched such a scheme. Any real student concession, free-travel benefit or metro-gate integration would require formal approval from BMRCL and any other relevant authorities.

## 2. Business Background

Students who rely on Namma Metro for their daily college commute may face a significant recurring transportation expense. A dedicated student metro-pass scheme could help reduce this burden, improve accessibility and encourage public transportation use.

The proposed project explores a digital system through which BMRCL and participating colleges could manage student eligibility and travel-pass validity efficiently.

The project is intended to demonstrate a possible solution, not to represent an existing official BMRCL programme or confirmed partnership.

## 3. Problem Statement

The absence of a dedicated student metro-pass scheme, as understood from available public information, creates an opportunity to explore a student-focused travel-benefit system for Namma Metro.

A potential scheme would need a reliable process to:

- Identify eligible students.
- Verify college enrolment.
- Approve and manage student passes.
- Prevent the use of expired, suspended or revoked passes.
- Verify passes efficiently at compatible readers.
- Maintain records for auditing and reporting.

The proposed system aims to demonstrate how these requirements could be addressed through a centralised digital platform.

## 4. Project Objectives

1. Propose a digital student metro-pass scheme for BMRCL.
2. Provide a platform for student registration and pass applications.
3. Enable colleges to verify student details and eligibility.
4. Allow authorised administrators to approve, reject, suspend or revoke passes.
5. Associate an approved pass with an NFC-enabled identity card or compatible credential.
6. Validate pass status using an NFC reader and backend system.
7. Record verification attempts for monitoring and reporting.
8. Demonstrate valid and invalid pass scenarios through a simulated metro-gate interface.
9. Design the prototype so that future official integration could be explored, subject to approval.

## 5. Project Scope

### 5.1 In Scope

- Student registration and login.
- Student profile and college information.
- Digital student-pass application.
- College verification and approval workflow.
- Pass validity-period management.
- NFC card or test-tag registration.
- NFC credential reading using compatible hardware.
- Backend pass verification.
- Simulated access-approved and access-denied results.
- Configurable pass conditions, such as validity dates and permitted travel zones or routes.
- Pass suspension, revocation and renewal management.
- Verification logs and administrative reports.
- Role-based access for students, college administrators and system administrators.

### 5.2 Out of Scope for the Initial Prototype

- Direct connection to live BMRCL metro gates.
- Issuing actual metro tickets or travel entitlements.
- Guaranteeing free or discounted travel.
- Processing actual fare payments or refunds.
- Using BMRCL's production ticketing systems or databases.
- Official deployment across metro stations.
- Claiming an official partnership or approval without written authorisation.

These features may be considered in a future phase if BMRCL approves the proposal and provides the necessary technical and operational support.

## 6. Stakeholders

| Stakeholder | Responsibility |
|---|---|
| BMRCL | Potential scheme owner; defines policy, eligibility, fares and operational requirements |
| College administration | Verifies enrolment and student eligibility |
| Students | Register and apply for the proposed pass |
| System administrator | Manages accounts, credentials, pass status and system configuration |
| Metro operations team | Would assess and support any future operational integration |
| Project team | Designs, develops, tests and documents the academic prototype |
| Project coordinator | Reviews academic scope, progress and deliverables |

## 7. Business Requirements

- **BR-01 — Student eligibility:** The system must support eligibility rules defined by authorised administrators.
- **BR-02 — College verification:** Student enrolment must be verified before a pass can be activated.
- **BR-03 — Pass management:** The system must support pass application, approval, rejection, renewal, suspension and revocation.
- **BR-04 — NFC credential association:** An approved pass must be linked to a registered NFC credential.
- **BR-05 — Pass validation:** The system must verify whether a pass is active, within its validity period and compliant with configured travel restrictions.
- **BR-06 — Access decision:** The prototype must display an approved or denied result based on the validation response.
- **BR-07 — Audit trail:** The system must record pass-verification attempts, timestamps and outcomes.
- **BR-08 — Administrative reporting:** Authorised administrators must be able to view student-pass statuses and verification summaries.
- **BR-09 — Security and privacy:** Student information and administrative functions must be protected against unauthorised access.
- **BR-10 — Future integration readiness:** The design should allow future integration to be evaluated, subject to BMRCL's technical requirements and formal approval.

## 8. Functional Requirements

### 8.1 Student Module

- Register and log in securely.
- Enter student details and college information.
- Submit a student-pass application.
- View application status.
- View pass status and validity dates.
- Request renewal where supported.
- View relevant pass-verification history, where permitted.

### 8.2 College Administration Module

- Log in using authorised credentials.
- Review submitted student applications.
- Verify enrolment details.
- Approve or reject applications.
- Record the reason for rejection where appropriate.
- Review students whose eligibility requires renewal or re-verification.

### 8.3 System Administration Module

- Manage student and college accounts.
- Configure eligibility and pass-validity rules.
- Register and deactivate NFC credentials.
- Activate, suspend or revoke approved passes.
- View verification logs and generate reports.
- Restrict administrative actions according to user roles.

### 8.4 NFC Verification Module

1. The student presents a registered NFC credential to a compatible reader.
2. The reader obtains the credential identifier or supported secure credential data.
3. The application sends the credential data to the backend.
4. The backend checks the associated pass and its status.
5. The system verifies validity dates and any configured travel restrictions.
6. The interface displays an access-approved or access-denied result.
7. The system records the verification event.

A basic NFC tag UID alone should not be treated as secure proof of identity because it may be copied or emulated. A real transit system would require an appropriately secure credential and an approved validation design.

## 9. Proposed Business Rules

1. Each student must have a unique student record.
2. Only verified and approved students may receive an active pass.
3. Each active pass must be associated with an authorised credential.
4. Expired, suspended, revoked or unrecognised credentials must be rejected.
5. Travel restrictions must follow the policy configured for the proposed scheme.
6. Only authorised users may change pass status or eligibility information.
7. Verification records must be protected and accessible only to authorised users.
8. Pass validity and renewal rules must be configurable.
9. The scheme's concession level, eligibility criteria and permitted travel conditions must be decided by BMRCL or the relevant approving authority—not assumed by the prototype.

## 10. Non-Functional Requirements

- **Security:** Secure authentication, role-based access and protection of student information.
- **Performance:** The prototype should return a verification result promptly under normal test conditions.
- **Reliability:** The system should handle invalid credentials and backend failures without incorrectly approving a pass.
- **Usability:** The interface should be straightforward for students and administrators.
- **Maintainability:** The application should use modular code and documented database structures.
- **Scalability:** The design should permit future support for multiple colleges and additional users.
- **Privacy:** Collect only necessary student data and limit access and retention according to applicable requirements.
- **Auditability:** Important administrative actions and verification events should be recorded.

## 11. Proposed Technology Stack

| Component | Proposed Technology |
|---|---|
| Frontend | HTML, CSS, JavaScript, Bootstrap |
| Backend | Python with Flask |
| Database | MySQL |
| NFC credential | Compatible NFC test card or tag |
| NFC reader | Compatible USB NFC reader |
| Development environment | College laboratory or suitable development computer |
| Access interface | Web-based simulated metro-gate screen |
| Testing | Sample student records and test credentials |

The final hardware and software choices may change depending on the available college-lab equipment and compatibility.

## 12. High-Level System Workflow

1. A student creates an account and submits a pass application.
2. The college administrator verifies the student's enrolment.
3. An authorised administrator approves or rejects the application.
4. After approval, a compatible NFC credential is registered against the student's pass.
5. The student taps the credential on the test reader.
6. The backend checks the pass status, validity period and configured conditions.
7. The simulated gate displays an approval or rejection.
8. The verification result is stored in the database for reporting.

## 13. Data Requirements

The proposed database may contain the following logical entities:

- **Students:** Student ID, name, college ID and relevant contact details.
- **Colleges:** College identifier and approved administrative users.
- **Pass Applications:** Application ID, submission date and review status.
- **Metro Passes:** Pass ID, validity period and current status.
- **NFC Credentials:** Credential reference, associated pass and active status.
- **Verification Logs:** Timestamp, credential reference and validation outcome.
- **Users and Roles:** Login identity, role and authorised permissions.

Sensitive credential data and student information must be handled securely. Actual BMRCL data must not be used without appropriate permission.

## 14. Assumptions and Dependencies

- A suitable NFC reader and test credentials will be available.
- The academic prototype will use sample data.
- The college will provide an environment in which the project can be tested.
- Any real eligibility rules and travel benefits remain subject to official policy decisions.
- Production deployment depends on BMRCL approval, compatible infrastructure, security assessment and any required agreements.
- The prototype is intended to demonstrate feasibility, not certify readiness for operational metro use.

## 15. Risks and Mitigation

| Risk | Proposed Mitigation |
|---|---|
| BMRCL does not approve the proposed scheme | Keep the project as an academic prototype and document the approval dependency |
| NFC reader or card incompatibility | Test hardware compatibility early and use supported test credentials |
| Credential copying or misuse | Explain the limits of basic NFC UIDs and recommend secure credentials for real deployment |
| Incorrect student details | Include a college verification workflow |
| Expired or revoked passes being accepted | Test all pass-status and validity conditions |
| Network or backend failure | Display a safe failure response rather than automatically approving access |
| Unauthorised access to student records | Use role-based permissions and protect stored data |
| Scope becomes too large | Prioritise the web application, pass management, NFC validation and simulated gate |

## 16. Project Deliverables

1. Business Requirements Document.
2. System design and architecture diagram.
3. Database design and schema.
4. Student and administrator web interfaces.
5. Student-pass application and approval workflow.
6. NFC credential registration and validation prototype.
7. Simulated metro-gate approval/rejection interface.
8. Test cases and testing results.
9. Final project report and demonstration.

## 17. Success Criteria

The project will be considered successful when:

- A student can register and apply for a pass.
- A college administrator can verify and approve an application.
- An approved pass can be linked to a test NFC credential.
- The compatible reader can obtain the test credential data.
- Valid passes receive an approval result.
- Invalid, expired, suspended and revoked passes are rejected.
- Verification events are saved and viewable by authorised administrators.
- Access controls and core workflows pass the planned tests.
- The prototype clearly distinguishes simulated access from real BMRCL gate operation.

## 18. Future Enhancements

- Formal proposal and pilot discussion with BMRCL.
- Secure transit-compatible NFC credentials.
- Integration with official metro fare collection and access-control systems, if approved.
- Automated college-enrolment verification.
- Student mobile application.
- Support for multiple colleges and authorised metro locations.
- Configurable concession, subsidy or free-travel policies.
- Enhanced fraud detection, audit reporting and operational analytics.

## 19. Conclusion

The NFC-Enabled Smart Student Metro Pass Management System is a proposed solution for exploring how BMRCL could introduce a student-specific metro-pass scheme supported by digital eligibility verification and NFC technology.

The academic prototype will demonstrate the core application, administrative workflow, credential validation and simulated access decisions. It provides a foundation for evaluating feasibility while recognising that real travel benefits and integration with Namma Metro require formal approval and collaboration with the relevant authorities.

**Project positioning:** This document presents a proposed initiative for BMRCL. It does not imply that BMRCL has endorsed, approved or agreed to implement the project.
