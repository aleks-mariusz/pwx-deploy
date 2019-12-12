# Portworx Demo / Testing Deployment

This repo provides a number of Terraform templates for deploying various container-orchestrators (CO's), with Portworx pre-installed (unless otherwise specified).

## Common Pre-requisites

All deployments require the following:

You need the following packages on your workstation

- Terraform
- aws-cli
- Ansible

Next, make sure you have your AWS credentials set and an SSH key-pair already existing in the required AWS regions.

Finally, consult the documentation in the scheduler-specific subdir in this repo for any additional requirements.

## Available Deployments

The following are the demo environments now deployable from this repo:

1. [deploy](./kubernetes/) Portworx on one or two K8s clusters (for the latter, with [cluster-pairing established](https://docs.portworx.com/portworx-install-with-kubernetes/migration/kubemotion/#generate-and-apply-a-clusterpair-spec) - suitable for a standard Kubernetes demo.
2. [deploy](./kubernetes/px-metro/) Portworx (as PX-Metro) on two Kubernetes clusters (using a single Portworx stretch-cluster)
3. [deploy](./openshift/) Portworx on single OpenShift 3.11 deployment, with Portworx pre-installed and the dashboard / service catalogue
4. [deploy](./swarm/) Portworx on single Swarm cluster with Portworx pre-installed
5. [deploy](./rancher/) single Rancher cluster - Portworx _not_ pre-installed
