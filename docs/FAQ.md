# Frequently Asked Questions

## Why am I encountering a low quota with projects created via Terraform Google Enterprise GenAI?

When you deploy the Terraform Google Enterprise GenAI with a Service Account, the project quota will be based on the reputation of your service account rather than your user identity. In many cases, this quota is initially low.

We recommend that you request 50 additional projects for the service account being used to deploy.
You can use the [Request Project Quota Increase](https://support.google.com/code/contact/project_quota_increase) form to request the quota increase.
In the support form, for **Email addresses that will be used to create projects**, use the `terraform_service_account` address provided in the module's input variables.
If you see other quota errors, see the [Quota documentation](https://cloud.google.com/docs/quota).
