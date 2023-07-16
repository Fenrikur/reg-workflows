# reg-workflows

## Overview

A collection of GitHub workflows for use in registration software repositories.

## Usage

All workflows in this repository have declared input and output parameters with many sensible defaults.

```
name: Invoke the build-test-go workflow example

on:
  push:
    branches: [ main ]

jobs:
  call_build_test:
    permissions:
      contents: read
    uses: eurofurence/reg-workflows/workflows/build-test-go.yml@main
    with:
      base-directory: ./app
```

**IMPORTANT**: For security reasons, please remember to appropriately limit the permissions of the 
auto-provided `secrets.GITHUB_TOKEN`. If you do not specify `permissions:`, the token will have very
broad permissions. If specified, all other permissions are turned off.

## Open Issues and Ideas

We track open issues as GitHub issues on this repository once it becomes clear what exactly needs to be done.
