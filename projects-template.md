# Create a templated project

In order to streamline the creation of projects, Adobe Developer Console provides templates that you can use to get up and running quickly.

This guide outlines the steps necessary to create a project using a template. 

If you do not wish to use a template and would like to create a blank project, please follow the steps in the [blank project guide](blank-project.md).

## Select organization

Before creating a project, ensure that you are working in the correct organization. To view and select an organization, use the organization switcher located in the top-right corner of the console.

![Organization switcher in console](images/switch-organizations.png)

## Quick start

To create a new project, select **Create project from template** from the _Quick start_ menu on the _Home_ screen.

![](images/create-project-from-template.png)

## Select template type

When the _Browse Templates_ dialog opens, you will be able to select a template type.

Currently three is one template type available: Adobe Custom Applications. This template supports you in creating a project that generates an Adobe Custom Application. 

> **Note:** Additional templates will be released in the future to support the streamlining of other workflows and creation of applications.

![](images/browse-templates.png)

## Set up templated project

After a template has been selected, it is time to set up the project.

The following sections provide detailed information and best practices for setting up a new templated project.

> **Note:** Please pay special attention to the [App Name](#app-name) as this value cannot be changed once project set up is complete.

![](images/set-up-templated-project.png)

### Project title

A project title is generated automatically ("Project 01"), but you can change the title by deleting the auto-generated title and providing a new one. 

This project title is internal only and can be changed later if required.

It is recommended that if you are working in collaboration with multiple developers, you provide a project title that is meaningful and makes the project easy to distinguish from other projects in the organization.

![](images/templated-project-title.png)

### App Name

The app name is the public-facing name of the application and is used for setting up environments and **cannot be changed once the project is created**. It is important to consider the name of the application as it cannot be altered beyond the set up screen.

**MISSING: Best Practices for App Names**

![](images/templated-project-app-name.png)

### Workspaces

Templated projects include multiple workspaces, which can be thought of as individual working sub-folders for each developer on the project. Workspaces are where you will connect services and get the credential details needed to connect to Adobe APIs.

Two workspaces are provided automatically: Production and Stage. These workspaces cannot be edited or deleted. 

Since most custom applications are created with the intent of being distributed, the Production workspace is the workspace that will be used for the submission and distribution flow. This means that the application that will be used by end-users is that which is built in the Production workspace. When you are ready to deploy your app, submit the Production workspace for approval.

You can create additional workspaces for each individual developer working on the project. These workspaces are editable and can be added or deleted as needed.

![](images/templated-project-workspaces.png)

### Adobe Runtime

When setting up a new project, you can automatically include Runtime with each workspace. Runtime is a powerful, serverless way to quickly deploy custom code to respond to events and execute functions right in the cloud, allowing you to orchestrate custom workflows that meet your unique business needs.

When the "Include Runtime with each workspace" checkbox is checked, each workspace that is created is automatically provision with a unique Runtime namespace allowing each developer to work within their own Runtime environment.  

> **Note:** Most use cases require the use of Runtime, therefore the checkbox is checked by default.

Notes on including Runtime in workspaces:
  * If you deselect the checkbox and do not opt for automatic inclusion of Runtime, you can enable it later. The downside is that you will need enable it manually for each individual workspace. You cannot auto-include Runtime for all workspaces after the initial set up is complete.
  * You can manually remove Runtime from individual workspaces later if you determine that Runtime is not needed.
  * Example where Runtime may not be needed: If you are building an application that is UI-only, you may not require Runtime.

To learn more about Adobe Runtime, visit the [Runtime documentation](https://www.adobe.io/apis/experienceplatform/runtime/docs.html)

### Save the project

With all of the set up details complete, you can select **Save** to save your project. This opens the project overview, showing the details of your newly created project.

From the project overview you can view and select all available workspaces, as well as see the status, template, last modified date, created date, and description for the project.

![](images/project-overview.png)

## Select a workspace

Now that your templated project is set up, you can begin to develop against it by adding services such as APIs and events. To begin development, select the workspace you wish to work in.

The _Workspace Overview_ appears, showing information regarding the selected workspace as well as any _Products & services_ added to the project. 

> **Note:** If you selected to "Include Runtime with each workspace" during set up, you will see the unique Runtime namespace for the workspace listed here.

![](images/workspace-get-started.png)

## Next Steps

To begin adding services, you can use the _+ Add Service_ button in the left navigation or select one of the quick start buttons (_Add API_ or _Add Event_)
under "Get started with your new workspace". 

For detailed information on working with services, please read the [services documentation](add-services.md).