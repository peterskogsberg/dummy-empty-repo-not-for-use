# Workspace bootstrap

This directory is not the application codebase. **All XD / FES / Cypress work lives in Bitbucket:**

- **Repository:** `xxldevelopment/xxl-frontend-service`
- **Clone URL:** `https://bitbucket.org/xxldevelopment/xxl-frontend-service.git`

## Credentials (this environment)

Bitbucket tokens are available in the environment (names may vary). Prefer **`BB_TOKEN_1`** (or `BB_TOKEN_2`, `BITBUCKET_SCOPED_API_TOKEN`, `BITBUCKET_APP_TOKEN`) for HTTPS Git:

```bash
git clone "https://x-token-auth:${BB_TOKEN_1}@bitbucket.org/xxldevelopment/xxl-frontend-service.git" xxl-frontend-service
cd xxl-frontend-service
```

If plain `git clone` is blocked, use the **Bitbucket Cloud REST API** with the same token (`Authorization: Bearer <token>` or Basic with username + app password per Bitbucket docs) to read/write files and commits.

## Where to work

After cloning, use **`/workspace/xxl-frontend-service`** as the project root for lint, tests, and commits.
