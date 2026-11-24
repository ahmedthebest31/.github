# `.github` — Centralized Configuration for `ahmedthebest31`

This repository hosts reusable GitHub Actions workflows and account-wide community health files shared across the `ahmedthebest31` organization of repositories.

## Contents

- `.github/workflows/validate-fastlane.yml` — reusable workflow (`workflow_call`) that validates Fastlane supply metadata and IzzyOnDroid-specific constraints for Android apps.
- `.github/FUNDING.yml` — account-wide sponsorship links (PayPal + InstaPay).

## Usage

Reference the reusable workflow from any Android repository:

```yaml
jobs:
  validate:
    uses: ahmedthebest31/.github/.github/workflows/validate-fastlane.yml@main
```

Pass an optional `fastlane_dir` input to override the default `fastlane/metadata/android` path.