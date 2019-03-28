Satorix Terraform buildpack
===========================

Use [Terraform](https://www.terraform.io/) in a buildpack compatible app.

Requires
--------

The Terraform config must implement a non-local [backend](https://www.terraform.io/docs/backends/index.html), because otherwise state will be lost between runs. The default local backend saves state in the filesystem which is emphemeral.

Usage
-----

Add the buildpack to a `.buildpacks` configuration in the root of the application directory to install `terraform` for the application to utilize.

Configuration
-------------

* `TERRAFORM_BIN_URL` set the source URL for the terraform binary
  * Defaults to 64-bit Linux binary for Heroku runtime
  * Expects a `*.zip` file as [distributed by Hashicorp](https://www.terraform.io/downloads.html)
