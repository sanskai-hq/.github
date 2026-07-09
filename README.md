# sanskai-hq/.github

Org-wide engineering **machinery**. This repo holds things every SanskAI repo shares:

- **`.github/workflows/ci-python.yml`, `ci-node.yml`** — reusable CI workflows repos call via
  `uses: sanskai-hq/.github/.github/workflows/ci-*.yml@v1.0.0`.
- **`profile/README.md`** — the org's public profile page.

## Rules for this repo (it's a single point of compromise for every deploy)
- Branch-protected `main`, required review (Dev as a second reviewer), no admin bypass.
- Release changes behind a **version tag** (`v1.0.0`, …). Repos pin the tag, never `@main`.
- Roll a workflow change out **canary-to-one-repo first**, then propagate via a version-bump PR.
- Pin all third-party actions to full commit SHAs before they guard anything real.

The engineering **standard and docs** live in **`sanskai-hq/dev-ops`**, not here.
