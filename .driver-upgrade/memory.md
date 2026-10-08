# What we know about yugabyte/pgx

Written by earlier upgrade sessions. Every line cost a run to discover.

Treat it as a starting point, not as fact: the tree may have moved since. If
something here is wrong, correct it -- that is worth more than the upgrade
itself, because the next session inherits whatever you leave.

Add what you learn under "Learned this run". Anything above it is already
stored; only new lines are kept.

## Learned this run

- Build command: `go build ./...`
- After rebasing, internal imports in ~168 Go files needed updating from `github.com/jackc/pgx/v5` to `github.com/yugabyte/pgx/v5` because the module name is `github.com/yugabyte/pgx/v5`
- The rebase replayed 48 commits onto v5.11.0 from base commit 3ce50c079e87
- Import path changes were the main post-rebase fix needed before the build would succeed
