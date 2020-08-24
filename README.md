# AZURE-211 TESTING - DO NOT PUSH
# quickstart-atlassian-crowd
## Crowd Software Data Center on the AWS Cloud
`Deployment Guide:` https://aws-quickstart.github.io/quickstart-atlassian-crowd/


Use this Quick Start to deploy Crowd Data Center on the AWS Cloud.

Crowd enables you to manage users from multiple directories - Active Directory, LDAP, OpenLDAP or Microsoft Azure AD - and control application authentication permissions in one single location. Crowd Data Center is a self-managed solution that gives you high availability, performance at scale, and disaster recovery for uninterrupted access to Crowd for all your teams.

This Quick Start uses the [Atlassian Standard Infrastructure (ASI)](https://fwd.aws/xYyYy) as a foundation. You can choose to build a new ASI for your deployment or deploy Crowd into your existing ASI. You can also deploy Jira, Confluence and Bitbucket Data Center within the same ASI.

![Quick Start architecture for Crowd on AWS](/docs/images/architecture_diagram.png)

For architectural details, best practices, step-by-step instructions, and customization options, see the
[deployment guide](https://aws-quickstart.github.io/quickstart-atlassian-crowd/).

### Using the Quick Start in production environments

The fastest way to deploy Crowd Data Center with this Quick Start is directly through its [AWS Quick Start interface](https://aws.amazon.com/quickstart/architecture/crowd). However, when you do, any updates we make to the Quick Start templates will propagate directly to your deployment. These updates sometimes involve adding or removing parameters, which could introduce unexpected (and possibly breaking) changes to your deployment.

As such, on production environments, we recommend that you clone the {partner-product-name-short} Quick Start templates to a custom S3 bucket. Then, launch the templates directly from there. This lets you control when to apply our latest changes to your environment. See [Launching from a cloned Quick Start](https://aws-quickstart.github.io/quickstart-atlassian-crowd/#_launching_from_a_cloned_quick_start_recommended_for_production) for instructions. 

### Network prerequisites

You need to create the required AWS networking infrastructure
(VPC, subnets) by using the [ASI Quick Start](https://fwd.aws/xYyYy), or by deploying Crowd with a new ASI.
For details, see the [deployment guide](https://aws-quickstart.github.io/quickstart-atlassian-crowd/).

## Development notes

### Pre-commit hook

It is recommended that you install the hooks under `submodules/quickstart-atlassian-services/scripts/hooks/`; this will
ensure that the metadata tags in the templates are automatically updated on
commit. The simplest method of doing this is:

    git config --add core.hooksPath submodules/quickstart-atlassian-services/scripts/hooks/

Alternatively you can invoke
`submodules/quickstart-atlassian-services/scripts/hooks/update-tags.py`
manually.

## Atlassian support

This Quick Start's CloudFormation templates were developed by Atlassian, in collaboration with AWS. To report an issue or request a feature, you can [contact Atlassian directly](https://support.atlassian.com/contact/#/).

For additional Atlassian documentation on how to manage Quick Start deployments, see [Running Crowd in an AWS cluster](https://confluence.atlassian.com/x/9uOJOw).
