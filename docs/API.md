# API Documentation

## Endpoints
### Transfer Intake
- **Description**: Collect, validate and normalize cases from Payment Hub; attach a runId and timestamp for traceability.
- **Type**: Processing

### Generate
- **Description**: Execute generate phase for the Self-Verify pattern: persist interim state, enforce guardrails, and emit structured JSON results.
- **Type**: Processing

### Verify
- **Description**: Execute verify phase for the Self-Verify pattern: persist interim state, enforce guardrails, and emit structured JSON results.
- **Type**: Processing

### Portfolio Check
- **Description**: Portfolio Check across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
- **Type**: Processing

### Sanctions Screening
- **Description**: Sanctions Screening across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
- **Type**: Processing

### Underwriting
- **Description**: Underwriting across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
- **Type**: Processing

### Regulatory Report
- **Description**: Assemble final payload with status, artifacts, KPIs and audit trail; store to Fraud Platform; return response JSON for the client.
- **Type**: Processing
