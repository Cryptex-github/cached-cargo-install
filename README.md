# cached-cargo-install
Faster cargo install by caching it in github action cache.

## Example workflow

```yaml
name: test
on: push

jobs:
  benchmark:
    runs-on: ubuntu-latest
    steps:
      - name: Install cargo-criterion
        uses: Cryptex-github/cached-cargo-install@main
        with:
          crate-name: cargo-criterion
  
      - name: Run benchmark
        run: cargo criterion
```

## Inputs

|     Name     | Required |             Description            |
| ------------ | -------- | ---------------------------------- |
| `crate-name` |     ✓    | The name of the crate on crates.io |

*Licensed under Apache-2.0*
