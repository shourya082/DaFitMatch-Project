# Security policy

DaFitMatch is a static browser application. It has no project-owned API server or server-side account database. Optional integrations may send data to third-party services when configured.

## Reporting a vulnerability

Please do not disclose suspected vulnerabilities in a public issue. If GitHub Private Vulnerability Reporting is enabled for this repository, use **Security → Report a vulnerability**. Otherwise, contact the repository owner through the contact options on their GitHub profile and request a private channel. Do not include real user photos, access tokens, or other sensitive data in an initial report.

Please include the affected page or file, the impact, steps to reproduce, and any relevant browser or deployment details. The maintainers will acknowledge reports as soon as practical and coordinate next steps and disclosure with the reporter.

## Data handling notes

- Style and fit profiles are stored in the visitor's browser `localStorage`.
- Google Identity Services is optional and client-side; this repository does not implement server-side token verification.
- A configured try-on provider may receive a selected photo and request details. Review that provider's privacy practices before enabling it.
- Never commit `src/config.js`, provider tokens, personal data, or real user photos.