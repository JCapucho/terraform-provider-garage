---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "garage_bucket_global_alias Resource - terraform-provider-garage"
subcategory: ""
description: |-
  This resource can be used to manage Garage bucket global aliases.
---

# garage_bucket_global_alias (Resource)

This resource can be used to manage Garage bucket global aliases.

## Example Usage

```terraform
resource "garage_bucket" "website" {}

resource "garage_bucket_global_alias" "website" {
  bucket_id = garage_bucket.website.id
  alias     = "website"
}

resource "garage_bucket_global_alias" "www" {
  bucket_id = garage_bucket.website.id
  alias     = "www"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `alias` (String)
- `bucket_id` (String)

### Read-Only

- `id` (String) The ID of this resource.

