# Architecture Documentation

## Overview
This Self-Verify implements Stress Test Advisor to improve approval rate for Banking & Finance use cases.

## Components
1. **Transfer Intake**: Collect, validate and normalize cases from Payment Hub; attach a runId and timestamp for traceability.
2. **Generate**: Execute generate phase for the Self-Verify pattern: persist interim state, enforce guardrails, and emit structured JSON results.
3. **Verify**: Execute verify phase for the Self-Verify pattern: persist interim state, enforce guardrails, and emit structured JSON results.
4. **Portfolio Check**: Portfolio Check across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
5. **Sanctions Screening**: Sanctions Screening across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
6. **Underwriting**: Underwriting across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
7. **Regulatory Report**: Assemble final payload with status, artifacts, KPIs and audit trail; store to Fraud Platform; return response JSON for the client.

## Data Flow
- Input: Transfer Intake
- Processing: 7 sequential steps
- Output: Regulatory Report
