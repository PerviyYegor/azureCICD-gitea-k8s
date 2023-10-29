# azureCICD-gitea-k8s

This repository contains the necessary files for setting up an Azure Pipeline that tracks changes in a private repository. The private repository contains the source code for an application called Gitea. Below, we provide a brief description of Gitea and include a link to the original repository.

## Gitea

Gitea is a lightweight, self-hosted Git service that provides a platform for code hosting, collaboration, and version control. It offers a wide range of features, including repository management, issue tracking, code reviews, and more. Gitea empowers development teams to efficiently manage their source code and streamline their workflow.

Original Gitea Repository: [Link to Gitea Repository](https://github.com/go-gitea/gitea)

# Azure DevOps Pipeline Setup

The configuration of the Azure DevOps pipeline was performed manually, without the use of Terraform. However, the deployment of the testing environment, specifically a Kubernetes cluster in Azure Kubernetes Service (AKS), is described in the `./terraform-config` directory using Terraform.

## Key Components

### should-be-in-gitea-repo

This directory contains a file that the Azure DevOps pipeline should reference to enable automated builds and deployments of the Gitea application container in AKS.

### k8s-app-config

In the `k8s-app-config` directory, we have defined the Kubernetes cluster configuration necessary for running the Gitea application within its own container in the cluster.

### azureDevOpsAnsibleAgent-config

The `azureDevOpsAnsibleAgent-config` directory contains a manifest for automatically configuring a machine with Oracle 9.2 Linux distribution. This configuration is essential for the machine to serve as an agent in the Azure DevOps pipeline, facilitating the build of the Gitea container.

This repository serves as a comprehensive guide for setting up an end-to-end development and deployment pipeline for the Gitea application using Azure DevOps, AKS, Terraform, and Kubernetes.

For further details on specific files, directories, and setup procedures, please refer to the corresponding sections in this repository.
