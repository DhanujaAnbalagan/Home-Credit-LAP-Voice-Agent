# Home Credit Loan Against Property – Voice Qualification Agent

## Overview

An AI-powered voice agent designed to conduct preliminary eligibility screening for Home Credit Loan Against Property (LAP) applications. The agent collects applicant and property details, evaluates eligibility against predefined business rules, and determines the appropriate next step.

## Objectives

- Automate preliminary loan eligibility screening through voice conversations.
- Collect essential property, ownership, income, and loan requirement details.
- Apply consistent eligibility rules.
- Identify applications requiring specialist assistance.
- Produce structured qualification outcomes for review.

## Key Features

- Conversational voice-based qualification.
- Property type and ownership verification.
- Original property document availability checks.
- Loan amount and tenure validation.
- Occupation and income mode verification.
- Specialist transfer handling for existing property loans or EMI reduction requests.
- Structured qualification status and post-call data extraction.

## Business Rules

| Criteria | Eligibility rule |
|---|---|
| Maximum loan amount | ₹75,00,000 |
| Property types | Residential, commercial, and industrial |
| Agricultural property | Not eligible |
| Ownership | Sole or joint |
| Original property documents | Required |
| Occupation | Salaried or self-employed |
| Income mode | Bank income accepted; cash income is not eligible |
| Loan tenure | 3–15 years |

If the requested loan amount exceeds ₹75,00,000, the agent explains the maximum available amount and asks whether the applicant wishes to proceed with that limit.

Existing loans against the property or requests for EMI reduction are referred to a specialist when no disqualification condition has already been triggered.

## Qualification Outcomes

- `QUALIFIED` – The applicant meets the configured preliminary eligibility rules.
- `DISQUALIFIED` – The applicant fails a mandatory eligibility requirement.
- `TRANSFER_REQUIRED` – Specialist assistance is required.
- `CALLBACK_REQUESTED` – The applicant requests a callback.

These outcomes represent preliminary screening, not final loan approval.

## Project Structure

```text
Home-Credit-LAP-Voice-Agent/
├── 01_System_Prompt/
├── 02_Voice_Agent/
├── 03_Call_Recordings/
├── 04_Test_Results/
├── 05_Design_Notes/
├── business_rules.md.txt
├── conversation_states.md.txt
├── prompt_review.md.txt
└── test_cases.md.txt
```

## Testing and Validation

The project includes 15 voice-call scenarios, associated recordings and transcripts, call logs, and test result reports. The scenarios cover eligible applicants, disqualification conditions, specialist transfers, and callback requests.

## Technology

- Retell AI for voice-agent configuration and conversational interaction.
- Prompt engineering for qualification logic and conversation flow.
- Structured test scenarios for behavior validation.

## Limitations

The agent performs preliminary eligibility screening based on configured rules. Final approval, applicable interest rates, and loan terms must be confirmed by the lender's authorized specialist.

## Repository Purpose

This repository documents the voice agent configuration, qualification logic, test scenarios, and validation artifacts for a Loan Against Property qualification workflow.
