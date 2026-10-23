# go-units.github.io

The go-units landing page (Hugo), served at <https://go-units.github.io/>.
The documentation is at <https://go-units.github.io/docs/> (repository
[go-units/docs](https://github.com/go-units/docs)).

go-units is **planned** (wave 2 of the [go-scikit roadmap](https://github.com/go-scikit/roadmap),
[PLAN.md](https://github.com/go-scikit/roadmap/blob/main/PLAN.md) and
[STATUS.md](https://github.com/go-scikit/roadmap/blob/main/STATUS.md)): the page
says what the organisation will cover (`units`, `constants`) and how each part
will be checked. No library exists and nothing is released.

The layout is the go-* family template: `layouts/index.html` and the shared
design (stylesheet, theme toggle, fork ribbon, icons), imported as the Hugo
module `github.com/go-fleettools/landingkit` pinned in `go.mod`. `[params.brand]`
in `hugo.toml` is read from the logo's gradient:

```sh
go run github.com/go-fleettools/landingkit/cmd/landingkit brand static/img/logo.svg
hugo server
```

| Workflow | What |
| --- | --- |
| `hugo.yml` | builds on pull requests; builds and deploys to Pages on `main` |
| `ci.yml` | the site builds and names every repository; `go mod tidy` keeps the landingkit requirement |
| `links.yml` | every link and image of the built site resolves |

BSD-3-Clause.
