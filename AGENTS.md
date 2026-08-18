# Repository instructions

## Purpose
This repository contains a GitHub Action that applies release-note labels to pull requests based on Conventional Commit types.

## Layout
- `index.js`: action implementation.
- `test/`: Mocha test suite.
- `action.yml`: action inputs and runtime definition.
- `dist/`: bundled action code generated with `@vercel/ncc`.
- `.github/workflows/`: CI, self-labeling, build, and release workflows.

## Development and validation
CI runs on Node.js 14.

- Install dependencies: `npm install`
- Run tests, coverage, and StandardJS linting: `npm test`
- Apply StandardJS fixes: `npm run fix`
- Rebuild the bundled action: `npm run build`

The build command replaces `dist/` with the bundle generated from `index.js`. Keep `package-lock.json` aligned with dependency changes. Do not check out untrusted pull request code from a `pull_request_target` workflow.
