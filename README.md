# release-poc-config-dev

Configuration of **DEV** for the release PoC: the first stage after `main`.

- Every merge to `main` of an application repository: the release bot writes `<app>_tag = "main/<commit>"` and `<app>_digest` here directly (no pull request: DEV is for fast feedback), the workflow **Tag and deploy** tags and deploys.
- Pushes on `feature/*`, `bugfix/*`, `hotfix/*`, `scope/*` are deployed to DEV as previews without changing this file.
- Nothing is promoted from DEV. TEST gets releases only.

The whole flow: [release-poc-deployment](https://github.com/christianlehnert/release-poc-deployment#readme).
