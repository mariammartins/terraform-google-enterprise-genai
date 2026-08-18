# Glossary

Defined terms in the documentation for Terraform Google Enterprise GenAI are capitalized and have specific meaning within the domain of knowledge.

## Terraform Service Account
The email for the privileged service account used to deploy the GenAI infrastructure. This service account must have the necessary permissions to create projects, configure organization policies, and manage resources across the ML platform. It is provided as an input variable (`terraform_service_account`) to the module.

## Harness
A Terraform configuration within the `examples/standalone/` directory responsible for creating the prerequisite projects (Seed, KMS, Logging, Machine Learning, Service Catalog, and Artifact Publishing) and the VPC network. The harness provisions the base resources that the root module consumes.

## Seed Project
Seed Project created by the harness in `examples/standalone/` to host the GCS bucket used to store the Terraform Remote State of the deployment.

## Terraform Remote State Data Source
A Terraform Data Source that retrieves output values from a remote [Backend Configuration](https://www.terraform.io/language/settings/backends/configuration).

## Service Catalog
A collection of opinionated Terraform modules (BigQuery, Cloud Storage, Vertex AI Workbench) published to a Cloud Storage bucket via a Cloud Build pipeline. Data scientists consume these modules to provision pre-approved resources within the ML project.

## Artifact Publishing
A Cloud Build pipeline configured to build and publish custom Docker images to Artifact Registry. These images are used by ML workloads such as Vertex AI Pipelines and training jobs.

