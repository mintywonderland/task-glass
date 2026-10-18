# Security Policy

## Supported scope

This repository is an early-stage, client-only prototype. It currently stores task data in the browser's `localStorage`. It does not currently implement authentication, a remote API, Cloudflare D1, or server-side access controls.

## Important limitations

- Anyone with access to the same browser profile may be able to inspect or modify locally stored tasks.
- Clearing browser storage can permanently remove tasks.
- Do not store passwords, authentication tokens, confidential business information, or other sensitive data in task content.
- Do not assume tasks are encrypted, backed up, or synchronized between devices.

## Reporting a vulnerability

Please do not publish credentials, personal data, or exploit details in a public issue. Contact the repository owner privately through GitHub's available private contact channels.

## Development rules

- Never commit API keys, OAuth client secrets, session secrets, or Cloudflare API tokens.
- Server-side authorization must be enforced on every protected endpoint; hiding UI controls is not authorization.
- Validate and limit user input on the server before adding remote persistence.
- Use secure, HttpOnly, SameSite cookies for server-managed sessions where appropriate; avoid storing session secrets in localStorage.
- Add dependency and workflow permissions only when needed.
