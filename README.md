# OrangeHRM Manual QA & RBAC Security Testing Portfolio

End-to-end manual functional testing, Role-Based Access Control (RBAC) security verification, and Jira defect lifecycle documentation for the **OrangeHRM Enterprise HR Management System**.

## Project Overview
- **Application Under Test (AUT):** OrangeHRM Open Source Demo (v5.x)
- **Testing Scope:** Employee Master Data (PIM), Role-Based Access Control (ESS vs. Admin), and End-to-End Leave Approval Workflows
- **Tools Used:** Jira Cloud (Agile Scrum Board), Microsoft Excel (Executive Summary, Test Execution & Defect Log), Google Chrome on Windows 11

## Test Execution Summary
| Module Tested | Test Cases | Passed | Failed | Pass Rate |
| :--- | :---: | :---: | :---: | :---: |
| **PIM - Add Employee** | 4 | 3 | 1 | 75.0% |
| **RBAC / Security (ESS Role)** | 2 | 2 | 0 | 100.0% |
| **Leave Management Workflow** | 2 | 2 | 0 | 100.0% |
| **Total** | **8** | **7** | **1** | **87.5%** |

## Key Defect Logged in Jira
- **Jira Ticket ID:** `SCRUM-5` (Linked to `TC-02`)
- **Summary:** `[PIM - Add Employee] First Name and Last Name fields accept numbers and special characters without input validation`
- **Severity / Priority:** Medium / High
- **Impact:** Allows corrupted non-alphabetic employee records into master HR tables, risking downstream payroll and reporting integrity.
- **Evidence:** Reproduction steps and screenshot proof archived in `/screenshots/Jira_SCRUM5.png`, `/screenshots/Invalid_Name_Credentials.png`, and `OrangeHRM_QA_Testsuite.xlsx`.

## Repository Contents
- `OrangeHRM_QA_Testsuite.xlsx` — Multi-tab QA report featuring an automated Executive Summary, Test Execution Log (`TC-01` to `TC-08`), and Jira Defect Log.
- `/screenshots` — Visual proof of input validation checks, RBAC `Credential Required` URL blocks, end-to-end leave approval, and Jira ticket `SCRUM-5`.
