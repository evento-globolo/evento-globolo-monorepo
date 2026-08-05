# evento-globolo-monorepo (superseded)

> This repository is frozen. The canonical source of truth is [`evgl-monorepo`](https://github.com/evento-globolo/evgl-monorepo).

The organization was bootstrapped with both short-name and full-name scaffolds. The short repository is the canonical implementation and composition authority. This repository remains available only for history and provenance; its generated repository catalog is not authoritative.

## Migrate

- Open issues, pull requests, releases, and new work in `evento-globolo/evgl-monorepo`.
- Use the canonical monorepo's `.zpkg.toml`, dependency graph, and `.zed-submodules.tsv` classifications.
- Point any retained submodule at the corresponding short-name repository.
- Prefer Zed packages for dependencies and use:

  ```bash
  git submodule update --init --recursive
  zed install --git-submodules
  ```

Do not source the same repository through both Zed and a gitlink. Use `zed overtake --git-submodules` only for deliberate, reviewed migration of submodules into Zed dependencies.

No source or lock-history file is removed by this consolidation. Git history remains intact; genuinely unique changes should be ported to the canonical monorepo in a reviewed PR before an organization administrator archives this repository.
