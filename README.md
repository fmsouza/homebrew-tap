# fmsouza/homebrew-tap

Homebrew formulae for [lanekeep](https://github.com/fmsouza/lanekeep) — deterministic,
AST-based architectural conformance checking.

```sh
brew install fmsouza/tap/lanekeep
```

## What is here

| Formula | |
| --- | --- |
| `lanekeep` | The CLI. macOS on Apple silicon, Linux on x86-64 and arm64. |

**No Intel macOS build.** lanekeep does not ship a prebuilt binary for it, so the formula does
not claim one — a download that 404s reads as Homebrew being broken rather than as a platform
that was never built. On an Intel Mac, install from source instead:

```sh
cargo install lanekeep-cli
```

## How this is maintained

`Formula/lanekeep.rb` is **generated**, not written. Every lanekeep release regenerates it from
that release's own `SHA256SUMS` and pushes it here, so the checksums in the formula are the
same ones a user verifies a download against.

Edits by hand will be overwritten by the next release. The generator lives at
[`scripts/build-homebrew-formula.sh`](https://github.com/fmsouza/lanekeep/blob/main/scripts/build-homebrew-formula.sh)
and is covered by tests in the main repository.
