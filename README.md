# Azure Aware Managed Identity

<!-- BEGIN_TF_DOCS -->
#### Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 1.0.0 |
| <a name="requirement_azurecaf"></a> [azurecaf](#requirement\_azurecaf) | >= 1.2.16 |
| <a name="requirement_azurerm"></a> [azurerm](#requirement\_azurerm) | >=3.0.2 |

#### Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_instance_index"></a> [instance\_index](#input\_instance\_index) | Resource type index on the resource group. | `number` | n/a | yes |
| <a name="input_resource_group_name"></a> [resource\_group\_name](#input\_resource\_group\_name) | Specifies the parent resource group name. | `string` | n/a | yes |
| <a name="input_caf_prefixes"></a> [caf\_prefixes](#input\_caf\_prefixes) | Prefixes to use for caf naming. | `list(string)` | `[]` | no |
| <a name="input_custom_location"></a> [custom\_location](#input\_custom\_location) | Specifies a custom location for the resource. | `string` | `""` | no |
| <a name="input_custom_name"></a> [custom\_name](#input\_custom\_name) | Specifies a custom name for the resource. | `string` | `""` | no |
| <a name="input_custom_tags"></a> [custom\_tags](#input\_custom\_tags) | The custom tags to add on the resource. | `map(string)` | `{}` | no |
| <a name="input_description"></a> [description](#input\_description) | Resource group description. | `string` | `""` | no |
| <a name="input_name_separator"></a> [name\_separator](#input\_name\_separator) | Separator for CAF prefixes in name. | `string` | `"-"` | no |

#### Outputs

| Name | Description |
|------|-------------|
| <a name="output_client_id"></a> [client\_id](#output\_client\_id) | Client ID associated with the user assigned identity. |
| <a name="output_id"></a> [id](#output\_id) | The user assigned identity ID. |
| <a name="output_name"></a> [name](#output\_name) | User assigned identity display name. |
| <a name="output_principal_id"></a> [principal\_id](#output\_principal\_id) | Service Principal ID associated with the user assigned identity. |
| <a name="output_tenant_id"></a> [tenant\_id](#output\_tenant\_id) | Tenant ID associated with the user assigned identity. |
<!-- END_TF_DOCS -->

## Related documentation

Terraform Azure public IP documentation: [https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/user_assigned_identity](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/user_assigned_identity)

Terraform Azure CAF Naming documentation: [https://registry.terraform.io/providers/aztfmod/azurecaf/latest/docs/resources/azurecaf_name](https://registry.terraform.io/providers/aztfmod/azurecaf/latest/docs/resources/azurecaf_name)

