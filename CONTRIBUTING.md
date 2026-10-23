# Contributing to DaFitMatch

Thanks for helping improve DaFitMatch. The project is a build-free static web application using HTML, CSS, and classic JavaScript files. Contributions should preserve that workflow unless a change is discussed first.

## Before opening a pull request

- Search existing issues and pull requests for related work.
- For larger changes, open an issue to discuss the problem and proposed approach.
- Keep pull requests focused and explain the user-visible impact.

## Local setup

1. Install Python 3, or use another local static HTTP server.
2. From the repository root, start the server:

   ```powershell
   python -m http.server 8000
   ```

3. Open `http://localhost:8000/index.html` in a modern browser. The catalogue uses `fetch()`, so the pages should not be opened with `file://`.
4. For optional integrations, copy `src/config.example.js` to `src/config.js` and add your own local values. Keep credentials out of commits.

There is no build step, package manager, configured test runner, or lint command at this time. Check changes manually in the browser, including the affected page at a narrow viewport when UI is involved. Verify browser console/network errors and test both configured and fallback states for optional integrations when relevant.

## Project conventions

- Keep scripts compatible with the existing classic-script loading order and `window.DaFitMatch*` namespaces.
- Preserve the no-fabrication behavior: unavailable sign-in or try-on services should remain clearly unavailable or be labelled as demos.
- Keep profile fields and recommendation behavior consistent with `docs/ARCHITECTURE.md`.
- Update `README.md`, `docs/ARCHITECTURE.md`, and configuration documentation when behavior, data contracts, setup, or supported integrations change.
- Do not add secrets, real user photos, or private data. Do not commit `src/config.js`.
- For catalogue changes, check that referenced images and model paths exist and that the displayed details match the data.

## Pull requests

Include the purpose, a concise summary, and how you checked the change. For interface changes, add screenshots at desktop and mobile widths when practical. Note any known limitations or follow-up work. Address review feedback and keep unrelated formatting changes out of the diff.

## Reporting a bug

Use the Bug report issue template and include reproducible steps, expected and actual behavior, browser/OS details, and relevant logs with personal data and secrets removed. For security concerns, follow `SECURITY.md` instead of opening a public issue.
