# Gulf Car Security Policy

This is the default policy for Gulf Car repositories that do not provide a repository-specific `SECURITY.md`.

## Reporting a vulnerability

Do **not** open a normal Issue containing an exploit path, credential, token, private key, sensitive personal data, or other information that materially increases exploitability.

Use the repository's private GitHub security reporting/advisory mechanism when enabled. Otherwise report the issue to the repository administrators through an approved private company channel.

Provide only the minimum information needed to identify the affected repository/version in any non-private discussion. Keep reproduction details and secrets in the approved private channel.

## If a credential or secret is exposed

1. Revoke or rotate it immediately.
2. Stop or restrict the affected integration if continued use creates risk.
3. Remove the secret from tracked configuration/code.
4. Assess Git history, logs, artifacts, and downstream systems separately.
5. Document remediation without copying the secret into Issues or Pull Requests.

Deleting a secret from the latest commit does not make an already exposed credential safe.

## Security review expectations

Changes involving authentication, authorization, sessions, CSRF, uploads, webhooks, messaging, payments, personal data, exports, database access, external integrations, CI/CD, or deployment should receive explicit security consideration and testing appropriate to their risk.
