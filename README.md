# Product Requirements Document (PRD)

## Campus Lost-and-Found System

**Course:** BU-209 Backend Engineering  
**Version:** 1.0

## 1. Introduction

The Campus Lost-and-Found System is a proposed web-based platform for students and authorized campus staff to report lost items, record found items, search reports, submit ownership claims, and track item returns.

The first version will focus on the backend and the essential lost-and-found process.

## 2. Problem Statement

Students may lose belongings while moving between lecture halls, libraries, laboratories, hostels, cafeterias, and other campus locations. Lost-item reports are often shared informally through classmates or group chats, where they can be missed or become difficult to find.

There is no consistent way to search reports, track an item’s status, or verify a claimant’s ownership. A central system could make the process more organized and help protect private information.

## 3. Research and Problem Validation

The problem must be validated through campus research before assumptions are treated as confirmed findings.

Research should involve students who have lost or found items and staff who receive lost property. It should explore commonly lost items, locations, current reporting methods, recovery difficulties, existing staff processes, and safe ways to verify ownership.

**Research status:** Interview responses and survey results have not yet been provided. Add the number and general roles of participants, research dates, and a summary of collected findings before final submission. Do not present uncollected results as facts.

## 4. Goal and Objectives

**Goal:** Provide a simple, organized platform for reporting, searching for, claiming, and recovering lost belongings.

The system should:
- Provide one place for lost-and-found reports.
- Support searching by keyword, category, location, and date.
- Allow ownership claims and review.
- Track item custody and status.
- Protect personal and ownership information.

## 5. Proposed Solution and Users

The system will allow users to report lost or found items and search existing reports. A person who believes an item is theirs can submit a claim with details to help verify ownership. Authorized staff can record items received at a designated desk and update custody information.

**Primary users:** Students, people who find items, and authorized campus staff such as designated porters or security personnel.

**Other stakeholders:** University administration, campus security, the course instructor, and the student community.

The system will support coordination; it will not physically collect, store, or deliver items, and it cannot guarantee ownership automatically.

## 6. Main User Stories

- As a student, I want to create an account and report a lost item.
- As a finder, I want to report an item so its owner can search for it.
- As a user, I want to search and filter reports.
- As an owner, I want to submit a claim for an item.
- As a finder or authorized staff member, I want to review claims before returning an item.
- As authorized staff, I want to record items received and update their custody.
- As a report creator, I want to update or close my report and view its status.

## 7. Functional Requirements

The backend must:

1. Allow users to register, log in, and log out.
2. Allow authenticated users to create lost-item and found-item reports.
3. Allow users to view active reports and individual report details.
4. Support searching and filtering by keyword, report type, category, location, and date range.
5. Allow report creators to edit permitted fields or close their own reports.
6. Allow users to submit ownership claims on eligible found-item reports.
7. Allow authorized finders or staff to review, accept, or reject claims.
8. Allow authorized users to mark an item as resolved after a confirmed handover.
9. Allow authorized staff to record items received and update custody information.
10. Allow users to view and manage their own reports and claims.

Reports and claims must have unique IDs and clear statuses. The system must reject invalid requests and prevent users from performing actions they are not authorized to perform.

## 8. Non-Functional Requirements

- **Security:** Hash passwords, require authentication for protected actions, and enforce permissions on the backend.
- **Privacy:** Do not expose personal contact details or private ownership-verification information in public reports.
- **Reliability:** Preserve valid reports and claims and record status changes accurately.
- **Performance:** Support pagination for report lists and search results.
- **Maintainability:** Keep requirements and API behavior documented and organize backend functionality into understandable modules.

## 9. Scope and MVP

The first version will include account management, lost-and-found reports, search and filtering, claims, custody and status tracking, basic staff permissions, and clear error handling.

The system will not include native mobile apps, AI image matching, real-time chat, push or SMS notifications, delivery services, payments or rewards, multi-campus support, advanced analytics, or automatic verification through university databases.

## 10. Roles and Permissions

- **Student:** Register, sign in, report items, search reports, submit claims, and manage their own reports.
- **Staff:** Perform student actions, record items received at a desk, manage custody, and review claims for items under their responsibility.
- **Administrator:** Manage staff access and oversee reports.

The backend must enforce these permissions. The process for verifying staff accounts must be agreed upon before implementation.

## 11. Main Workflow

1. A user signs in and submits a lost-item or found-item report.
2. The system validates and stores the report with a unique ID and status.
3. Users search active reports and view non-sensitive details.
4. A person who believes a found item is theirs submits a claim.
5. The finder or authorized staff reviews the claim and records a decision.
6. If approved, the parties arrange a handover. After the return is confirmed, an authorized person marks the item as resolved.

A claim approval alone does not mean the item has been returned.

## 12. Data and API Requirements

The system will store user details, item reports, claims, custody information, and status changes. It should collect only necessary information and protect private ownership details.

The backend will provide endpoints for accounts, reports, claims, and staff actions. These endpoints will support reporting, searching, claiming, reviewing, and managing items.

## 13. Conclusion

The Campus Lost-and-Found System aims to make reporting and recovering belongings easier for students and staff. A central place for reports, searches, and ownership claims can improve how lost property is managed on campus. Campus research will be used to validate the problem and guide the final design.
