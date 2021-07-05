######Quickstart for Rancher#####

Deploy

Clone or download this repository to a local folder
Copy or rename terraform.tfvars.example to terraform.tfvars and fill in all required variables
Run terraform init
Run terraform apply
When provisioning has finished, terraform will output the URL to connect to the Rancher server. Two sets of Kubernetes configurations will also be generated:

kube_config_server.yaml contains credentials to access the RKE cluster supporting the Rancher server
kube_config_workload.yaml contains credentials to access the provisioned workload cluster
For more details on each cloud provider, refer to the documentation in their respective folders.

Remove

When you're finished exploring the Rancher server, use terraform to tear down all resources in the quickstart.

NOTE: Any resources not provisioned by the quickstart are not guaranteed to be destroyed when tearing down the quickstart. Make sure you tear down any resources you provisioned manually before running the destroy command.

Run terraform destroy -auto-approve to remove all resources without prompting for confirmation.
