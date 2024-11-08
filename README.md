# Infrastructure

All infrastructure resources for this project are provisioned using **Terraform**, managed through **GitHub Actions** workflows to ensure consistent and automated deployment. The **S3 Bucket** serves as the main storage and hosting solution for the frontend of the application.

## Infrastructure Components

### Terraform
- **Purpose**: Terraform is used as the Infrastructure as Code (IaC) tool to define and deploy all AWS resources, ensuring consistency across environments.
- **Configuration**: Terraform templates manage the configuration and deployment of resources like the S3 bucket for static website hosting, IAM roles, and policies.
- **Benefits**: Using Terraform allows easy version control, reuse, and automated management of infrastructure resources.

### GitHub Actions Workflow
The CI/CD pipeline for infrastructure is automated through GitHub Actions, providing continuous deployment capabilities for the Terraform-managed resources.

- **Terraform Workflow**: A GitHub Actions workflow is configured to automatically apply infrastructure updates when changes are pushed to the infrastructure repository.
- **Deployment Trigger**: When updates to the Terraform templates are committed, the workflow triggers a plan and apply action in Terraform, ensuring that all changes are deployed to AWS without manual intervention.

### S3 Bucket
- **Purpose**: The S3 bucket serves as the storage and hosting location for the frontend files (HTML, CSS, JavaScript) for the resume website.
- **Configuration**: Configured for static website hosting, with a bucket policy to allow public access. This enables the website to be directly accessible over the internet.
- **Integration**: Managed through Terraform, ensuring the bucket is consistently configured with the correct policies and settings during each deployment cycle.
