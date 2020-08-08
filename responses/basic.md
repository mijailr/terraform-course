## Creating your first configuration file

This step assumes you have docker for desktop and VS Code Studio installed and running in your local machine. I can recommend [VS Code Studio](https://code.visualstudio.com/) with the official [Terraform Plugin](https://marketplace.visualstudio.com/items?itemName=HashiCorp.terraform).

### Understandig the HCL language

For defining terraform configuration we will use a language called __Hashicorp Configuration Language__ (HCL for short) is like an enriched `JSON`. But the configuration files can be written on `JSON` as well, and recently on `Python` and `TypeScript` with the [Cloud Development Kit](https://www.hashicorp.com/blog/cdk-for-terraform-enabling-python-and-typescript-support/).


### Defining our provider

First of all we need to specify the `provider` to run our terraform configuration, the provider is a terraform plugin used to make the API calls required to provision the infrastructure. Since terraform 0.12 is recommended to specify the provider version since the release schedule of `terraform` is different of the `providers` and newly released versions can be incompatible with your current configuration. To specify the version of your provider you can use the keyword `version` inside the provider block.

```hcl
# file: provider.tf

provider "docker" {
  version = "~> 2.7"
}
```

Please commit your `provider.tf` file and close this issue to continue.
