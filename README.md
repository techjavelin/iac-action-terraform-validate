# iac-action-terraform-validate

[![Continuous Integration | main](https://github.com/techjavelin/iac-action-terraform-validate/actions/workflows/continuous.yml/badge.svg)](https://github.com/techjavelin/iac-action-terraform-validate/actions/workflows/continuous.yml)

The `techjavelin/iac-action-terraform-validate` action is a part of the [iac-actions collection](https://github.com/search?q=org%3Atechjavelin+iac-action) created by [Tech Javelin](https://github.com/techjavelin) to make creating consistent secure infrastructure configuration management as easy as each element in your Infrastructure-as-Code projects by creating the concept of Infrastructure-as-Code-as-Code - allowing you to describe your IaC Workflows as immutable code, provide testing strategies to ensure changes to infrastructure won't break production, and create simple, repeatable processes for managing your infrastructure.

# Usage

This action can be run on the `ubuntu`, `windows`, or `macos` Github Action runners.

The default configuration will install the latest version of [Terraform](https://github.com/hashicorp/terraform) and run the fmt and validate against the project root directory, against any `.tf` files found under (recursive).

```
steps:
  - uses: techjavelin/iac-action-terraform-validate@V1
```

A specific version of `terraform` can be used
```
steps:
  - uses: techjavelin/iac-action-terraform-validate@v1
    with:
      version: '1.3.5'
```

More detailed configuration can be done using additional [Input Parameters](#Input+Parameters)

## Input Parameters

| Input | Description | Required | Default | Example |
| - | - | - | - | - |
| `terraform-dir` | Directory where `tflint` will look for your terraform files | Y | `<Project Root>` | `terraform-dir: terraform/my-environment` |
| `version` | Use a specific verison of `tflint` | N | `latest` | `version: 'v0.42.0'` |

## Outputs

| Output | Description |
| - | - |
| `init` | The output of the `init` command 
| `format` | Results of the format command
| `format_files` | List of files that were formatted
| `validate` | Results of validation

# License

[Mozilla Public License v2.0](LICENSE)

# Code of Conduct

`Coming Soon`

# Experimental Status

> By using the software in this repository (the "Software"), you acknowledge that: (1) the Software is still in development, may change, and has not been released as a commercial product by Tech Javelin Ltd and is not currently supported in any way by Tech Javelin Ltd; (2) the Software is provided on an "as-is" basis, and may include bugs, errors, or other issues; (3) the Software is NOT INTENDED FOR PRODUCTION USE, use of the Software may result in unexpected results, loss of data, or other unexpected results, and Tech Javelin Ltd disclaims any and all liability resulting from use of the Software; and (4) HashiCorp reserves all rights to make all decisions about the features, functionality and commercial release (or non-release) of the Software, at any time and without any obligation or liability whatsoever.
