# DevOps Team Guide

- [Introduction](#introduction)
- [DevOps Concepts](#devops-concepts)
  - [Backlogs](#backlogs)
  - [Azure Boards](#azure-boards)
  -	[Continuous Integration and Continuous Delivery](#continuous-integration-and-continuous-delivery)
  -	[Pipelines](#pipelines)
  -	[Test Plans](#test-plans)
  -	[Artifacts](#artifacts)
  -	[Queries](#queries)
  -	[Dashboard](#dashboard)
-	[Team Expectations and Processes](#team-expectations-and-processes)
  -	[Work Items](#work-items)
  -	[Branch Policies](#branch-policies)
  -	[Linking Work Items to Repos](#linking-work-items-to-repos)
  -	[Pull Requests](#pull-requests)
  -	[Version Control](#version-control)
  -	[Post-Deployment](#post-deployment)
    -	[Pipeline Deletions](#pipeline-deletions)

# Introduction

DevOps is a set of practices that combines software development (Dev) and IT operations (Ops) to enable organizations to deliver applications and services at a high velocity. Hence, the scope of DevOps is not limited to just development. It emphasizes collaboration, automation, and continuous improvement throughout the entire software development cycle.
The AOS team uses DevOps as a way to manage the project and its development. We are also using Agile, which is an iterative and incremental approach to software development. It allows you to break down large projects into smaller, manageable tasks called user stories and work on them in short iterations called sprints.
With DevOps, we can automate the deployment and delivery of Power BI reports, ensuring faster and more reliable releases. [Organization name] has a One Project Agile approach, which means that all projects throughout the organization are under a single project, separated as ‘teams’.

# DevOps Concepts

## Backlogs

The backlog is a dynamic and prioritized list of work items that need to be completed to achieve the goals of a project. It serves as a centralized repository for all the tasks, enhancements, and bugs that we have identified and plan to address.
The backlog can be thought of as a queue of work waiting to be addressed. It represents the uncompleted work yet to be planned, developed, tested, and deployed. The items in the backlog can come from various sources, including product owners, stakeholders, team members, or client feedback.

## Azure Boards

A common way to visualize the backlog is by using Azure Boards. Azure Boards are visual dashboards that help us track and manage our work items. Work items can be tasks, user stories, bugs, or any other units of work. Boards provide a clear overview of what needs to be done, who is responsible for it, and the progress being made. We can organize our work items into columns, such as “New”, “Active”, “Resolved”, or “Closed”. The items can be dragged and dropped to their appropriate columns.

## Continuous Integration and Continuous Delivery

Continuous Integration (CI) involves developers integrating their code into a shared repository frequently. This triggers an automated build and test process, ensuring that changes are validated as quickly as possible. Continuous Delivery (CD) takes CI a step further by automating the deployment process, enabling us to release new features to production swiftly and reliably.

## Pipelines

Pipeline development allows you to define, manage, and automate the steps involved in building, testing, and deploying our applications. By creating a well-designed pipeline, we can ensure consistent, repeatable processes and reduce the risk of error. Pipelines are a series of automated steps that enable us to build, test, and deploy our applications. They define the flow of changes from the repository to the target environment. Pipelines can include various stages, such as building the code, running tests, creating artifacts, and deploying to production.

## Test Plans

Test plans help us ensure the quality and reliability of our applications. They outline the test cases, scenarios, and steps to be performed to validate our software. By executing these tests as part of our pipeline, we can catch bugs early, prevent regressions, and deliver a more stable product.

## Artifacts

Artifacts are the output of our pipeline process. They can be binaries, executables, libraries, or any other files generated during the build and packaging stages. Artifacts are stored in a central repository, making them accessible for deployment and further testing. Having a well-organized artifact repository allows us to easily retrieve and deploy specific versions of our applications.

## Queries

Queries can be created and shared with team members. 

## Dashboard

In the Overview section, where Dashboards can be selected, one has been created for the team:
This can allow you to view tasks assigned to you and will provide a more streamlined view.

# Team Expectations and Processes

## Work Items

Work items can be single entities that remain unlinked to Epics, User Stories, or Features. To create a work item, you can navigate to the Boards and select backlog or work items, then select the + New Work Item or click the plus (+) sign next to the Epic, Feature, or User Story.
Every item needs a concise and clear title, a clear description, and acceptance criteria, if available. Acceptance Criteria are specific conditions or requirements that the item must meet in order to be accepted and can be completed in list form. They serve as guidelines to determine whether the work has been successfully completed and meets the requirements and expectations.

Example: Acceptance Criteria for a user registration:
  •	The user should be able to create a new account using a valid email address and password
  •	Upon successful registration, the user should receive a confirmation email
  •	The user should not be able to register with an existing email address

## Branch Policies

Every branch we are responsible for developing should have a branch policy, which consists of 2 mandatory reviewers, in order to push to repository’s main branch. In addition, the branch policy dictates that the work must be linked to an open work item. Pushing to the main branch will often close the related work item, but the work item can be re-opened by the user again, if necessary.

The standard for branch naming is for the developer to create a branch name with their first name and the feature they are working on, i.e. your-first-name/feature-branch-name. Once development in a branch is complete and is no longer in use, it is recommended to delete your feature branch after merging successfully to main. 

## Linking Work Items to Repos

There are two methods of linking work items to repositories: 

1. Using Visual Studio Code (VS Code), or
2. From DevOps

In VS Code, you can link work items by adding the work item number to the commit in the format of #work-item-number and a description of what was changed. In DevOps, the work item number can be located to the left of the item’s title. The commit comment must begin with the hashtag (#) symbol, followed by the work item number, without spaces in between, then a space to add the remainder of the description, e.g. #12345 Added a button.
In DevOps, you must navigate to your current work item and select the ‘Add Link’ under the Development section. Under ‘Link Type’, you will be able to choose from Code or Build related types, including, but not limited to, branches and commits. 

## Pull Requests

Pull requests let the team know about the changes you have pushed to a branch in a repository. To open a pull request, navigate to the intended repository and select the appropriate branch, i.e. main, then select Create a pull request.
 
Once selected, you will be required to confirm the source and target branches, write a title for your commit, a description, add 2 mandatory reviewers from the team, then link the necessary work item.

When the required reviewers have reviewed the code, they may provide feedback or approve the changes. All comments must be resolved in order to complete the pull request.

A pull request can be set to be completed automatically when all required reviewers have approved the changes.

## Version Control

We utilize Git, a distributed version control system (DVCS). Changes to a repository can be viewed in the History tab for any branch in DevOps.  

## Post-Deployment

### Pipeline Deletions

Upon the successful deployment of your pipeline, it is recommended you delete your pipelines. Deletion of pipelines ensure that pipelines which are no longer in use are not creating clutter, reducing security due to the unused or forgotten pipelines that may have vulnerable configurations, reducing maintenance overhead, allowing for easier auditing and compliance, and reinforcing efficient CI/CD workflows. 


