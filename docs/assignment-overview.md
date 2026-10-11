# Assignment Overview

## Scope

This repository contains the artifacts for a Home Credit Loan Against Property (LAP) voice-agent assignment configured in Retell AI. It documents a preliminary qualification conversation and the business rules supplied in the system prompt.

## Agent Configuration

- **Company:** Home Credit
- **Agent:** Priya, a female AI voice assistant
- **Product:** Loan Against Property (LAP)
- **Language:** English
- **Maximum offer amount:** ₹75 lakh

## Qualification Flow

The agent verifies the intended customer before disclosing the offer, asks seven eligibility questions, captures answers given out of order, clarifies ambiguous speech, handles interruptions and corrections, and performs a preliminary handoff to a senior loan expert when all required criteria pass.

The seven checklist areas are property type, ownership, original property documents, loan amount, occupation and income mode, property market value, and repayment tenure. Agricultural property, unavailable original documents, cash income, and a tenure outside 3–15 years are immediate disqualification conditions. An existing property loan or EMI-reduction request is routed to a loan-transfer specialist instead of the fresh-loan flow.

Requests above ₹75 lakh are not automatically rejected. The agent explains the ₹75 lakh cap and continues only after the customer explicitly agrees to proceed at that maximum amount.

## Successful Scenario

The supplied transcript records a successful simulated call in which Bhargav confirms a residential property, sole ownership, available original documents, a ₹50 lakh request, salaried bank income, an estimated property value of ₹1 crore, and a 10-year tenure. The agent then communicates the preliminary handoff to a senior loan expert.

## Limitations

This is a Retell-configured voice-agent prototype and assignment artifact set. It is not a standalone executable application, a production deployment, an automated loan approval system, or evidence of a guaranteed offer. The call recording is kept for separate Google Drive sharing and is not included in this repository.