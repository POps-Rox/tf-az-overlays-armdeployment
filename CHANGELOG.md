# v2.0.0 - 2026-05-11

### Changed

- **BREAKING**: Bumped `azurerm` provider to `~> 4.20` across all three submodules (
  `modules/azure_arm_deployment/{tenant,resource_group,subscription}/versions.tf`).
- **BREAKING**: Raised Terraform `required_version` to `>= 1.10` (was `>= 1.9`).
- Declared `azapi ~> 2.0` in each submodule `versions.tf` for fleet alignment.
- Refreshed both `examples/{Commerical,Government}/arm_rg_vnet/versions.tf` to declare the full fleet provider stack and to drop the 4.x-incompatible `skip_provider_registration = true` argument (replacement is `resource_provider_registrations`; leaving unset preserves the safe default).
- Added `VERSION` file at `2.0.0`.

### Migration notes

- Consumers must set `ARM_SUBSCRIPTION_ID` (or `provider "azurerm" { subscription_id = ... }`) — azurerm 4.x makes this mandatory.
- The three `azurerm_*_template_deployment` resources used by this overlay have no 3.x→4.x attribute renames.

# v1.0.0 - <date>

Added
- Add Something you added
