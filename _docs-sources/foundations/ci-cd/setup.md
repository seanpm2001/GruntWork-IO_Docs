# Getting Started

## Prerequisites

To get started with Pipelines for Account Factory, you must have:

- Admin Access to a [Control Tower Managed AWS Account Structure](/foundations/accounts/enable-control-tower)
- A GitHub Machine User with Access to Gruntwork Libraries
- Permissions to create new GitHub Repos

## Create your Infrastructure Pipelines Repo

The `infrastructure-pipelines` repo will be your organization's point of access to AWS.  It contains a set of
GitHub actions workflows that require sensitive permissions for planning and applying infrastructure.

To create this repository in your organization:

1. Navigate to the [Gruntwork infrastructure-pipelines Template](https://github.com/gruntwork-io/infrastructure-pipelines-starter)
1. Click `Use this template`, then `Create a new repository`
1. Select your organization from the `Owner` drop-down
1. Give the repo a name (We recommend `infrastructure-pipelines`) and description
1. Make sure your settings look similar to the example below, and click `Create Repository`

![Create infrastructure-pipelines repository from template](/img/devops-foundations/pipelines/create-infra-pipelines.png)


## Create your Infrastructure Live Repo

## Initialize your Infrastructure Pipelines Repo

1. Ensure your Organization or your `infrastructure-pipelines` repo has an environment variable `GW_GITHUB_TOKEN` set to the GITHUB PAT created for your machine user
1. Within your new `infrastructure-pipelines` repo, navigate to the **Actions** tab
1. From the side panel on the left, select `Infrastructure-Pipeilnes Starter`
1. In the blue banner at the top of the table, click `Run workflow`
1. Input the requested `infrastructure-live` repository name and the Account IDs from your AWS Control Tower setup, then click `Run workflow`
1. After the workflow finishes, a PR will appear containing the necessary workflow.yml files for operating Gruntwork Pipelines. Review and Merge the PR
1. Your Pipeline is now ready for use!

## Initialize your Infrastructure Live Repo
