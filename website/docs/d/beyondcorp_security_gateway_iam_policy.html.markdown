---
# ----------------------------------------------------------------------------
#
#     ***     AUTO GENERATED CODE    ***    Type: MMv1     ***
#
# ----------------------------------------------------------------------------
#
#     This file is automatically generated by Magic Modules and manual
#     changes will be clobbered when the file is regenerated.
#
#     Please read more about how to change this file in
#     .github/CONTRIBUTING.md.
#
# ----------------------------------------------------------------------------
subcategory: "BeyondCorp"
description: |-
  A datasource to retrieve the IAM policy state for BeyondCorp SecurityGateway
---


# `google_beyondcorp_security_gateway_iam_policy`
Retrieves the current IAM policy data for securitygateway


## example

```hcl
data "google_beyondcorp_security_gateway_iam_policy" "policy" {
  project = google_beyondcorp_security_gateway.example.project
  location = google_beyondcorp_security_gateway.example.location
  security_gateway_id = google_beyondcorp_security_gateway.example.security_gateway_id
}
```

## Argument Reference

The following arguments are supported:

* `location` - (Optional) Resource ID segment making up resource `name`. It identifies the resource within its parent collection as described in https://google.aip.dev/122. Must be omitted or set to `global`. Used to find the parent resource to bind the IAM policy to. If not specified,
  the value will be parsed from the identifier of the parent resource. If no location is provided in the parent identifier and no
  location is specified, it is taken from the provider configuration.

* `project` - (Optional) The ID of the project in which the resource belongs.
    If it is not provided, the project will be parsed from the identifier of the parent resource. If no project is provided in the parent identifier and no project is specified, the provider project is used.

## Attributes Reference

The attributes are exported:

* `etag` - (Computed) The etag of the IAM policy.

* `policy_data` - (Required only by `google_beyondcorp_security_gateway_iam_policy`) The policy data generated by
  a `google_iam_policy` data source.
