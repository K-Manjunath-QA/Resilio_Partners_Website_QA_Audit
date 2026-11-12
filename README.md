<div align="center">

# Resilio Partners | Website QA & UI/UX Audit

**Manual QA · Exploratory Testing · Responsive Review · Defect Analysis**

[![Manual QA](https://img.shields.io/badge/QA-Manual%20%2B%20Exploratory-245A81?style=flat-square)](#)
[![Test cases](https://img.shields.io/badge/Cases-21-2F855A?style=flat-square)](#results)
[![Open defects](https://img.shields.io/badge/Defects-7%20Open-C05621?style=flat-square)](#key-findings)

[Website](https://resilio-partners.com/) · **Tester:** K. Manjunath · **Audit:** 08–11 Nov 2026

</div>

## Project overview

Independent manual QA and UI/UX review of a live B2B website. The work covered requirements-based test design, scripted execution, exploratory checks, responsive/usability observations, defect reporting and a QA release recommendation.

## Results

| Measure | Outcome |
|---|---:|
| Website modules identified | 6 |
| Requirements / scenarios | 13 / 10 |
| Scripted test cases | 15 — 11 Pass · 1 Fail · 3 Blocked |
| Exploratory test cases | 6 — 6 Fail |
| Combined audit | 21 cases — 18 executed · 3 Blocked |
| Open defects | 7 — 3 Sev-2 · 3 Sev-3 · 1 Sev-4 |
| Scripted pass rate | **91.7%** (11 of 12 executed) |
| QA recommendation | **Conditional Hold** |

*Scripted and exploratory results are reported separately. Exploratory findings are not included in the scripted pass-rate calculation.*

## Key findings

| Jira | Finding | Severity |
|---|---|---|
| [RQA3-1](https://kmanjunath.atlassian.net/browse/RQA3-1) | 5.1 MB PDF upload returns HTTP 413; form remains in “Submitting…” | Sev-2 |
| [RQA3-2](https://kmanjunath.atlassian.net/browse/RQA3-2) | 4.3 MB PDF, below the stated 5 MB limit, also returns HTTP 413 | Sev-2 |
| [RQA3-3](https://kmanjunath.atlassian.net/browse/RQA3-3) / [RQA3-4](https://kmanjunath.atlassian.net/browse/RQA3-4) | Navbar overflow and portfolio heading/text overlap at intermediate widths | Sev-3 |
| [RQA3-6](https://kmanjunath.atlassian.net/browse/RQA3-6) / [RQA3-7](https://kmanjunath.atlassian.net/browse/RQA3-7) | Auth-page heading overlap and misleading pointer cursor on static cards | Sev-3 / Sev-4 |
| [RQA3-8](https://kmanjunath.atlassian.net/browse/RQA3-8) | Broken GitHub footer link; Privacy Policy and Terms links misroute | Sev-2 |

**Technical investigation:** Chrome DevTools Network evidence captured HTTP 413 responses from the resume-upload endpoint. The 4.3 MB observation is tracked separately from the 5.1 MB over-limit test. The server-side root cause has not been independently verified.

## Skills demonstrated

- **Test design:** equivalence partitioning, boundary-value analysis and error guessing.
- **Test execution:** functional, negative, responsive, keyboard-accessibility, performance.
- **Traceability:** requirements → scenarios → test cases → execution results.
- **Defect management:** reproduction steps, expected vs. actual results, impact, severity and evidence.
- **UI/UX review:** responsive layout, text overlap, navigation affordance and footer-link usability.

## Repository files

| File | Contents |
|---|---|
| `Resilio_Master_Test_Scenarios_and_Test_Cases.xlsx` | 17 sheets: dashboard, modules, scenarios, test cases, test suites, RTM, execution summary, exploratory tests and defect log |
| `Test_Execution_Summary.pdf` | Execution scorecard, module and test-type results, test register and QA recommendation |
| `Defect_Log_and_Jira.pdf` | Seven defect reports with Jira details, reproduction steps, severity and remediation suggestions |
| `Defects_Evidence` | directory contains supporting screenshots and screen recordings for reported defects. <br/>Evidence is organized by Jira defect ID (RQA3-1, RQA3-2, etc.) to make verification and defect reproduction easier. |
| `README.md` | Project overview and recruiter reading guide |

## Scope and limitations

- Testing was performed on the public production site using synthetic test data; no load/stress testing was performed.
- TC-009 (email delivery) and TC-010–TC-011 (login) were blocked by unavailable inbox access and test credentials.
- Accessibility, performance and security checks were limited to the specific checks documented; they are not full audits or formal conformance assessments.
- No test automation or source-code/server-log verification was performed.
- **Conditional Hold** is my QA recommendation, not an authorized production release decision.

## Tools

Jira · Google spreadsheets · Microsoft Word · Chrome DevTools · Google Lighthouse

## About

**K. Manjunath** · Aspiring Manual QA Engineer / UI/UX Reviewer  
LinkedIn: *(https://www.linkedin.com/in/k-manjunath-qa-engineer/)* · Email: *kmanjunath2307@gmail.com*
