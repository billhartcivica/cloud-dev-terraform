These scripts create an EC2 instance via Terraform, using a wrapper script (create)
to parse script arguments as creation parameters in the 'create.tf' YAML file.

The 'kill' script destroys the instance created using the 'create' script.

The AMI used in this example is pre-baked to an extent, with xrdp/vnc already
installed, along with some development tools. A customised base install can be made
by using a standard AMI and amending the 'remote-exec' section to include the 
customised tools required.
 
terraform apply - builds infrastructure for all *.tf files in the current folder.
terraform apply -input=false -auto-approve - builds inf for all *.tf files without a 'yes' confirmation.
terraform destroy - tears down insf for all *.tf files in current folder.
