# Home Credit LAP Qualification Voice Agent 🎙️

An AI-powered voice agent built using **Retell AI** for the Home Credit Loan Against Property (LAP) qualification assignment. The agent conducts a preliminary eligibility conversation, collects customer information, applies the specified eligibility criteria, and routes qualified customers to a senior loan expert.

## 📌 Project Overview

The goal of this project is to demonstrate how an AI voice agent can conduct natural, professional customer conversations while following predefined business rules.

The agent represents Home Credit and informs verified customers about a Loan Against Property offer of up to **₹75 lakh**. It performs a preliminary qualification check before handing eligible customers over to a senior loan expert.

**Platform:** Retell AI  
**Agent Name:** Priya  
**Product:** Loan Against Property (LAP)  
**Conversation Language:** English

## 🎯 Objectives

- Verify the intended customer's identity before revealing the offer.
- Explain the Loan Against Property offer.
- Collect all seven required eligibility checklist items.
- Handle natural speech, interruptions, ambiguous answers, and corrections.
- Capture information provided out of order without unnecessarily repeating questions.
- Apply disqualification and loan-transfer routing rules.
- Hand qualified customers over to a senior loan expert.

## ⚙️ Eligibility Checklist

| Checklist item | Eligibility criteria |
|---|---|
| Property type | Residential, commercial, or industrial |
| Ownership | Sole or joint ownership |
| Original documents | Original property documents must be available for verification |
| Loan amount | Maximum ₹75 lakh; requests above this require customer agreement to proceed at the maximum |
| Occupation and income | Salaried or self-employed; income must be received through a bank |
| Property market value | Capture the customer's estimated current market value; no minimum threshold is specified in the assignment |
| Repayment tenure | Between 3 and 15 years, inclusive |

## 🧠 Business Logic

### Immediate disqualification

The agent politely ends the fresh-loan qualification flow when a customer clearly fails a specified eligibility criterion:

- The property is agricultural.
- Original property documents are unavailable.
- Relevant income is received in cash.
- Requested repayment tenure is below 3 years or above 15 years.

### Loan amount limit

If a customer requests more than ₹75 lakh, the agent explains the maximum offer amount and asks whether the customer agrees to proceed with ₹75 lakh. The agent must not assume consent.

### Loan-transfer routing

If the customer mentions an existing loan on the property or requests EMI reduction, the agent directs them to a loan-transfer specialist and ends the fresh-loan flow.

### Human handoff

Once all seven checklist items have been answered and all applicable criteria are satisfied, the agent informs the customer that a senior loan expert will contact them to discuss the exact interest rate and further steps.

Preliminary qualification is not a guarantee of final loan approval.

## 💬 Conversation Handling

The system prompt instructs the agent to:

- Maintain a professional and advisory tone.
- Verify customer identity before disclosing the offer.
- Recognize common synonyms and speech-recognition errors.
- Clarify ambiguous responses without inventing information.
- Remember answers supplied out of order.
- Avoid asking questions that have already been clearly answered.
- Respect customer refusals and requests to end the call.
- Avoid inventing interest rates, fees, or unsupported product terms.

## 🏗️ Project Structure

```text
home-credit-lap-voice-agent/
├── README.md
├── .gitignore
├── prompts/
│   └── Home_Credit_LAP_System_Prompt.txt
├── transcripts/
│   └── Successful_Call_Transcript.txt
└── docs/
    └── assignment-overview.md
```

This repository contains the system prompt and supporting assignment documentation. The voice agent itself is configured and tested in Retell AI; this repository is not a standalone executable application.

## 🧪 Testing

The agent was tested using simulated customer conversations in Retell AI.

The successful test scenario included:

- Verified customer identity.
- Residential property.
- Sole ownership.
- Original property documents available.
- Loan request of ₹50 lakh.
- Salaried occupation with bank-received income.
- Estimated property market value of ₹1 crore.
- Requested repayment tenure of 10 years.
- Successful handoff to a senior loan expert.

The transcript is included as evidence of the simulated conversation.

## 📂 Project Artifacts

- **System prompt:** [prompts/Home_Credit_LAP_System_Prompt.txt](prompts/Home_Credit_LAP_System_Prompt.txt)
- **Successful call transcript:** [transcripts/Successful_Call_Transcript.txt](transcripts/Successful_Call_Transcript.txt)
- **Assignment overview:** [docs/assignment-overview.md](docs/assignment-overview.md)
- **Call recording:** The WAV recording is intended to be shared separately through Google Drive. No recording URL was provided for this repository.

## 🔒 Privacy and Security

- Do not commit API keys, passwords, access tokens, or private environment files.
- Share recordings and transcripts only through authorized links.
- Do not include real customer financial information without appropriate authorization.

## 🚀 Future Improvements

- Improve speech recognition and natural turn-taking.
- Reduce repeated clarification questions.
- Test additional scenarios, including disqualification, customer unavailability, and loan-transfer routing.
- Improve call-log analysis and evaluation of qualification accuracy.

## 👨‍💻 Implementation

Developed as part of the **Home Credit Loan Against Property Voice Agent Design** assignment using Retell AI.

The system prompt and test transcript document the implemented conversational logic and the results of a successful simulated call.

This is a Retell-configured voice-agent prototype, not a standalone executable application, an API integration, or a loan approval system.
