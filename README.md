# wipac-dev-project-action
GitHub Action Package for Automating GitHub Projects

## Overview

Adds Issues and/or Projects to a GitHub Project on `issues`/`pull_request` events.

## Example Usage
```
name: Add PR/Issue to Project

on:
  issues:
    types:
      - opened
      - labeled
  pull_request:
    types:
      - opened
      - labeled
      
jobs:
  add-to-project:
    runs-on: ubuntu-latest
    steps:
      - uses: WIPACrepo/wipac-dev-project-action@v###
        with:
          github_token: ${{ secrets.ORG_PROJECT_TOKEN }}
          organization: WIPACrepo
          project_number: 6
```
