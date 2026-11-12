# Guide for AI-assisted project review

This overview provides context, but it does not contain the application source. A complete technical review requires authorized access to the private repository:

`https://github.com/nicoprog4/tokenchain-web3-ticketing`

## Suggested review approach

1. Read the root README, the project documentation, and the current Git history before proposing changes.
2. Map each user-facing flow across the frontend, API, persistence layer, background tasks, and external integrations.
3. Compare documented behavior with the current implementation and tests. Treat test-network configuration and mock integrations as non-production.
4. Identify assumptions and missing evidence explicitly; distinguish confirmed defects from questions and improvement ideas.
5. Prioritize findings by user impact, security, data integrity, and likelihood. Include file paths, relevant code locations, and a reproducible test or verification step.
6. Propose small, reviewable changes and run the narrowest relevant tests before broader suites.

## Important constraints

- Do not infer that a feature is production-ready just because its module, screen, or configuration exists.
- Do not expose `.env` files, API credentials, private keys, personal data, or test-account credentials in reports or prompts.
- Do not deploy contracts, move funds, or change live service configuration as part of a code review.
- Treat payment callbacks, authentication, QR validation, resale, and blockchain transaction handling as high-impact areas that need careful end-to-end verification.
- Ask the project owner before making changes that alter product behavior, data retention, or deployment choices.

## Useful output from a review

- A short description of the behavior verified.
- Findings ranked by severity and confidence, with exact locations and evidence.
- Gaps where the available code or tests do not establish expected behavior.
- A proposed implementation order with dependencies and targeted validation commands.
