# Versions Branch

This orphan branch tracks released versions for rancher-assets.

## Structure

`versions.yaml` contains the latest stable and prerelease tags for each chart major version.

## DO NOT EDIT MANUALLY

This file is automatically updated by GitHub Actions workflows:
- `auto-prerelease.yml` - Auto-bumps prereleases on merge to main
- `manual-release.yml` - Release Team manual version control

## Querying Versions

```bash
# Latest stable for v1
yq '.v1.stable.tag' versions.yaml

# Latest prerelease for v0
yq '.v0.prerelease.tag' versions.yaml

# When was v1 last updated?
yq '.v1.stable.updated-at' versions.yaml
```
