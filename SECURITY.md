# Security Policy

This repository is a public showcase. Sensitive implementation details are intentionally omitted. Security is a priority for internal development and operations.

---

## Supported Versions

- **Active development branch:** `main`  
- **Releases:** Security fixes are applied to the latest stable release only.

---

## Reporting a Vulnerability

- **Do not disclose publicly:** Please avoid posting sensitive information in public Issues or PRs.  
- **Private contact:** Report suspected vulnerabilities directly to the maintainers.

- **Preferred method:**  
  - **Email:** Electronicbester@gmail.com  
  - **Subject:** Arc Agentic Trading – Vulnerability Report  
  - **Include:**  
    - **Summary:** What you found and where.  
    - **Impact:** Potential risk or affected components.  
    - **Reproduction:** Minimal steps or proof-of-concept (no keys/logs).  
    - **Environment:** Versions, network, and configuration context (redacted).

> If email is unavailable, open a private issue and mark it for maintainers only. Avoid sharing credentials, API tokens, or logs containing secrets.

---

## Handling of Reports

- **Acknowledgement:** We aim to respond within 5 business days.  
- **Triage:** Severity and scope are assessed; reproduction is performed in an isolated environment.  
- **Remediation:** Fixes are prepared, reviewed, and released promptly.  
- **Disclosure:** Coordinated disclosure with the reporter. A brief changelog note is published after a fix.

---

## Secrets and Credentials

- **Never commit secrets:**  
  - Private keys, API tokens, wallet IDs, endpoints must not be stored in the repository.  
- **Environment variables:**  
  - Use local `.env` files or secure vaults; do not push `.env` or similar files.  
- **Rotation:**  
  - Rotate credentials immediately if exposure is suspected; audit access logs.

---

## Dependencies and Supply Chain

- **Lockfiles:** Maintain deterministic builds (e.g., `package-lock.json`/`pnpm-lock.yaml`).  
- **Updates:** Apply security patches regularly; monitor advisories (npm, GitHub Dependabot).  
- **Verification:** Prefer pinned versions, signed releases where possible.

---

## Secure Development Practices

- **Least privilege:** Contracts and wallets should enforce allowlists, daily caps, and kill-switches.  
- **Separation of concerns:** Off-chain planning (AI) and on-chain execution must remain isolated with strict validation on-chain.  
- **Validation:** Enforce slippage bounds, venue allowlists, and budget caps on-chain.  
- **Logging and audit:** Hash AI inputs/outputs off-chain; use on-chain events for traceability; store audit trails securely.

---

## Incident Response

- **Containment:** Disable external integrations and pause execution (kill-switch) if abnormal behavior is detected.  
- **Investigation:** Review recent deployments, wallet policies, audit logs, and dependency changes.  
- **Recovery:** Patch, rotate credentials, and re-enable services gradually with monitoring.  
- **Post-mortem:** Document root cause and preventive actions in internal docs.

---

## Notes

- Public docs are intentionally abstracted; internal documentation contains exact procedures.  
- Vulnerability reports should be sent to **Electronicbester@gmail.com**.
