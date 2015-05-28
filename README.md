# Tsuru Terraform

## Requirements

You need Terraform >= 0.5.0, e.g. `brew install terraform`.

You need an SSH key. The private key needs to be chmod to 600.

You need the cloud provider credentials. These will be entered on the command line.

### Extra requirements for GCE provisioning

The terraform provider for GCE requires access to an 'account.json' file - this is available from GCE's web interface in the 'credentials' section.

Please note, for our team this is currently shared as it's not clear that we can create multiple accounts. If you are on the team please obtain the credentials from someone else. There is a [story in our backlog](https://www.pivotaltracker.com/n/projects/1275640/stories/93990946) to address this.

## Notes

Change into one of the provider sub-directories before executing `terraform` commands.

For usage, refer to the [Terraform CLI doc](https://www.terraform.io/docs/commands/index.html).

To create your own environment, you need to pass a variable of the name you want to give it, e.g. `terraform apply -var env=my-new-environment`.

We have found that `terraform destroy` doesn't work reliably. Possible cause [this issue](https://github.com/hashicorp/terraform/issues/1203). Workaround is to delete manually via the console.

