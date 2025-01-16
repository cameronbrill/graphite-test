[![Go Report Card](https://goreportcard.com/badge/github.com/cameronbrill/go-project-template)](https://goreportcard.com/report/github.com/cameronbrill/go-project-template)
[![GoDoc](https://godoc.org/github.com/cameronbrill/go-project-template?status.svg)](https://godoc.org/github.com/cameronbrill/go-project-template)

# graphite demo (record zoom)
demoing graphite.dev to my team.


### steps
- open [#11](https://github.com/cameronbrill/graphite-demo/pull/11) and [#12](https://github.com/cameronbrill/graphite-demo/pull/12) in graphite
- open [#8](https://github.com/cameronbrill/graphite-demo/pull/8), [#9](https://github.com/cameronbrill/graphite-demo/pull/9), [#10](https://github.com/cameronbrill/graphite-demo/pull/10) in graphite
- open [#7](https://github.com/cameronbrill/graphite-demo/pull/7), merge it
- update the graphite PRs:
```
gt co update-two
gt sync
gt restack
* resolve conflicts *
gt s
```
- observe merge conflicts are gone on both graphite PRs.

- update the vanilla PRs:
```
git checkout update-one-point-five
git rebase main
* resolve conflicts *
git push --force
git checkout update-two-point-five
git rebase update-two-point-five
* resolve conflicts again *
git push --force
```
- observe merge conflicts are gone on the two regular PRs
