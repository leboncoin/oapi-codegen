# `oapi-codegen` — Release fork

This repository is a fork of [`github.com/oapi-codegen/oapi-codegen`](https://github.com/oapi-codegen/oapi-codegen).

Its sole purpose is to trigger a GitHub Actions release workflow on every tag, which pre-builds the `oapi-codegen` binary for multiple platforms and publishes the resulting artifacts as a GitHub release.

For documentation, usage, and everything else, refer to the [official project README](https://github.com/oapi-codegen/oapi-codegen/blob/main/README.md).

## Keeping up with upstream releases

Each time a new release is published on the upstream repository:

1. Merge the upstream release tag into the `main` branch of this repository:
   ```bash
   git fetch upstream
   git merge v1.x.y
   git push origin main
   ```
2. Create and push the corresponding tag:
   ```bash
   git tag v1.x.y
   git push origin v1.x.y
   ```

The release workflow will trigger automatically and produce pre-built binaries for all supported platforms.
