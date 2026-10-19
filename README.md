# hitan-group defaults

- **Issue forms** (Bug, Feature, Spec) and the **pull request checklist** used by every repository in hitan-group that has none of its own.
- **The board workflow** (`.github/workflows/board.yml`): the company board moves by itself from what really happens in GitHub, so progress is always truthful.

## How a card moves

| What happens | Card moves to | Written down |
|---|---|---|
| Issue opened (Spec form: label `spec`) | Ideas (Spec: needs approval) | comment on the issue |
| Pull request opened with `Closes #12` in its description | In review | comment on the issue |
| Merged and deployed (push to main) | **Live**, with **Deployed at** | comment on the issue + the [Deploy log](https://github.com/hitan-group/.github-private/issues/1) |
| Repositories that release by version (SEO Assist): merged | Testing | comment on the issue |
| ...then a GitHub release is published | **Live**, with **Deployed at** | comment + Deploy log |
| Issue closed by hand | stays where it is (closing is not shipping) | Last update on the card |

Every comment carries the date and time in Pakistan, who did it, and the commit or version.
Members have read only access to the board, so a card can only move through real work.

## Add it to a repository

1. Repository secret `BOARD_TOKEN` (Settings, Secrets and variables, Actions): the company board token.
2. Add `.github/workflows/board.yml`:

```yaml
name: Company board
on:
  issues: { types: [opened, reopened, closed] }
  pull_request: { types: [opened, reopened, ready_for_review, closed] }
  push: { branches: [main] }
  release: { types: [published] }
concurrency: { group: board-${{ github.repository }}, cancel-in-progress: false }
jobs:
  board:
    uses: hitan-group/.github/.github/workflows/board.yml@main
    with:
      product: Posting tool      # the board's Product name
      deploy_mode: merge         # merge: a push to main is the deploy; release: a published release is
    secrets:
      BOARD_TOKEN: ${{ secrets.BOARD_TOKEN }}
```
