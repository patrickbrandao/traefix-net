# traefix-net

Fork of [golang/net](https://github.com/golang/net) maintained for [Traefix](https://github.com/patrickbrandao/traefix),
the fork of Traefik with connection and request fingerprinting.

- The module path stays `golang.org/x/net`: Traefix uses this fork through a `replace` directive in its `go.mod`.
- Branch `traefix`: the upstream release in use, plus the Traefix changes, each in its own commit whose
  message ends with "(Traefix)".
- Tags `<upstream version>-traefix.<n>`, for example `v0.62.0-traefix.1`: `<upstream version>` is the upstream
  release the branch is based on, `<n>` counts the Traefix releases on that base.
- Moving to a new upstream release: rebase the Traefix commits on the new upstream tag, run the tests,
  tag `<new version>-traefix.1`, and update the `replace` and the `require` of Traefix together.
- The Traefix changes that make sense upstream are proposed there, so that the fork shrinks.
