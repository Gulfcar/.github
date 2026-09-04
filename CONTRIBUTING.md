# Gulf Car Contribution Guidelines

These are the organization-wide defaults. If a repository contains its own `CONTRIBUTING.md`, its repository-specific rules take precedence.

## Work tracking

Use an Issue for meaningful bugs, features, security hardening, technical debt, migrations, and operational changes. Define the problem and acceptance criteria before broad implementation when practical.

## Branches

Do not develop directly on the production/default branch unless a repository explicitly documents a controlled exception.

Use short-lived branches with clear names, for example:

- `feature/<issue>-short-name`
- `fix/<issue>-short-name`
- `security/<issue>-short-name`
- `chore/<issue>-short-name`
- `hotfix/<issue>-short-name`

Delete merged short-lived branches. Never rewrite shared branch history for cosmetic reasons.

## Pull Requests

Keep each PR focused on one concern. The PR should explain:

1. What changed?
2. Why is it needed?
3. How was it tested?
4. What are the risks?
5. How can the change be rolled back or recovered if it fails?

Resolve CI failures and review conversations before merge. Repository-specific staging/production promotion rules must be followed.

## Security and data

Never commit:

- passwords, access tokens, API keys, private keys, or `.env` files;
- production database dumps or backups;
- customer, guest, employee, or other personal-data exports;
- credentials embedded in screenshots, fixtures, logs, or examples.

If a secret is exposed, rotate/revoke it before treating source cleanup as complete. Follow the repository's `SECURITY.md` or the organization default.

## Database and deployment

Schema changes should be migration-based, reviewable, and recoverable. Backfills should be idempotent where practical. High-risk releases must document deployment order, verification, and rollback/recovery.

## Repository-specific standards

Applications should document their own runtime, test command, branch-to-environment mapping, deployment flow, and release checklist. Those repository-specific documents override this baseline when they are stricter.
