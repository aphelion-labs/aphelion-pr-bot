# aphelion-pr-bot

PR reviewer bot for [aphelion](https://github.com/aphelion-labs/aphelion). It reviews pull requests on the Claude API with a small set of reviewer personas, picks the two most relevant personas per pull request, and posts each verdict as a review comment and a check run. It never approves or requests changes; the repository owner decides what merges.

**Status: not started.** The MVP is specified in the first issue of this repository. Design decisions for the bot are recorded in the product repository under `docs/decisions/0011-pr-reviewer-bot.md`.

## Scope

- Runs in GitHub Actions on GitHub-hosted runners, callable from the product repository as a reusable workflow.
- Posts with a GitHub App token or a personal access token, never the default `GITHUB_TOKEN`, so that its reviews can trigger the product repository's responder workflow.
- Reviews only same-repository, non-draft pull requests.

## License

Apache-2.0, see LICENSE.
