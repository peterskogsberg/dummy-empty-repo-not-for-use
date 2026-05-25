# Workspace bootstrap

This directory is not the application codebase. **XD / frontend work targets Bitbucket:**

- **Repository:** `xxldevelopment/xxl-frontend-service`
- **Clone URL:** `https://bitbucket.org/xxldevelopment/xxl-frontend-service.git`

## Credentials (this environment)

Use HTTPS Git with a Bitbucket app password or access token. Prefer **`BB_TOKEN_1`** when present:

```bash
git clone "https://x-token-auth:${BB_TOKEN_1}@bitbucket.org/xxldevelopment/xxl-frontend-service.git" xxl-frontend-service
cd xxl-frontend-service
```

After cloning, use that directory as the project root for lint, tests, and commits.

## XD-19415 (capitalize sub-category links)

If `yarn typecheck` fails after adding `textTransform: "capitalize"` to `ProductListNavigation` link styles, MUI’s `styled("a")(object)` typing may reject extra keys once `interactionFeedbackForStyledMui` is spread into the same object. **Fix:** pass base styles and `textTransform` as separate style arguments:

```tsx
export const StyledLink = styled("a")(LinkStyle, {
  textTransform: "capitalize",
});
```

See Bitbucket branch `feature/XD-19415` (commits through `b1ad53c`).
