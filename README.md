# actions-workflows
Reusable GitHub Actions workflows

## Workflows

### [Validate Terraform in Issues](.github/workflows/validate-terraform-issues.yml)

Validates Terraform configuration blocks in GitHub issues. When users submit issues with Terraform code, this workflow automatically validates the configuration and posts a sticky comment with any errors.

```yaml
name: Validate Issues

on:
  issues:
    types: [opened, edited]

jobs:
  terraform:
    uses: terraform-linters/actions-workflows/.github/workflows/validate-terraform-issues.yml@main
    permissions:
      issues: write
```
