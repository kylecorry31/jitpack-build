# Jitpack Build
Triggers a build on Jitpack.

## Example
To use this following a new release, use the following:

```yaml
on:
  release:
    types: [published]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: kylecorry31/jitpack-build@1.0.0
        with:
          version: ${{ github.event.release.tag_name }}
```

## Inputs

### `version`

**Required: Yes**  
The tag or commit hash to generate a build for.

### `timeout`

**Required: No**  
**Default: `600`**  
The time in seconds to wait for the Jitpack build, defaults to 10 minutes.
