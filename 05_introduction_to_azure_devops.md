# Introduction to Azure DevOps

## Overview

Microsoft Azure DevOps provides an end-to-end DevOps toolchain for developing and deploying software. It also integrates with most leading tools on the market and is advantageous for orchestrating a DevOps toolchain. 

Azure DevOps provides services for software development teams to plan work, collaborate on code implementation, and build and deploy software products. Azure DevOps supports a collaborative culture and methodologies that bring together software developers, project managers, and contributors to develop software.

## Lesson Outcomes

By the end of this lesson, you will be able to:

1. Understand the core concept and purpose of Azure DevOps.
3. Identify the key benefits of using Azure DevOps for software development and delivery.
4. Explore and explain the features and tools offered by Azure DevOps.


With Azure DevOps, there are various integrated components that you can access via your web browser or integrated development environment (IDE). Depending on your project and team’s requirements, you may need to use some or all of the components, including Azure Boards, Azure Repos, Azure Pipelines, Azure Test Plans, and Azure Artifacts.

You can use Azure DevOps either on the cloud as a software-as-a-service platform utilizing Azure DevOps Services or as an on-premise tool with the Azure DevOps Server.

## AZURE DevOps SERVICES VS. AZURE DevOps SERVER

**Azure DevOps Services** and **Azure DevOps Server** offer the same DevOps features with some difference:

➤ **Azure DevOps Services**: You can access the software-as-a-service offering for Azure DevOps through the Internet. This web-based service has a service-level agreement of at least 99.9 percent uptime, making it reliable. Azure DevOps services are also globally distributed.

➤ **Azure DevOps Server**: Azure DevOps Server’s backing foundation is a customizable SQL server backend. If your organization embraces this version, you can access the on-premise offering over your internal network. This option is crucial for organizations that want all their data only on their own networks for business reasons

### Differences Between Azure DevOps Services and Azure DevOps Server

The differences between these two Azure DevOps offerings can be grouped into the following:

➤ Scoping

➤ Authentication

➤ User access management

➤ Data protection

#### Scoping

In _Azure DevOps Services_, scoping happens by organizations and projects. Organizations in Azure DevOps Services have URLs, and this is where everyone’s collaboration journey starts. These organizations contain their group of projects. Each project can be developed and supported by the different teams in the organization, and team members need to operate in the project environment only.

With _Azure DevOps Server_, scoping happens by deployments, project collections, and projects. In straightforward terms, a deployment is a server. Project collections are containers that exist in deployments. These containers are for security, administration, and physical database boundaries. They’re also used to group related projects. Finally, projects encapsulate the different parts of individual software projects, including source code, work items, and more

#### Authentication
Azure Active Directory is an identity and access management service.

In _Azure DevOps Services_, authentication happens over the Internet. Authentication happens with your Microsoft account credentials or Azure Active Directory credentials, depending on your organization’s setup. You can also set up Azure Active Directory to require various features such as multifactor authentication, IP address restrictions, and more.

With _Azure DevOps Server_, authentication happens on an intranet server. You authenticate with Windows Authentication and your Active Directory domain credentials. This process is transparent.

#### User Access Management
Beyond authentication, authorization exists to enforce that users have access to resources. This process happens by assigning roles and access levels to users. For example, a user with an Admin role will have permission to do more than a user with a Contributor role.

In _Azure DevOps Services_, each user has an access level, and they revalidate anytime they sign in. These users interact with resources only at the level specified, and that interaction happens on the Azure cloud.

In _Azure DevOps Server_, users have access levels, but everything happens from the primary system. Once the access level is specified, in addition to authentication, authorization occurs on the intranet server.

#### Data Protection
In _Azure DevOps Services_, all your data, including projects, source codes, and plans, exist on Azure. Projects in Azure DevOps Services are safe and secure.

In _Azure DevOps Server_, all your data exists on the on-premise servers your organization uses, and administrators control everything.

### Similarities Between Azure DevOps Services and Azure DevOps Server

Although the cloud and on-premise offerings for Azure DevOps have some differences, they share some similarities as well.

#### Features

The cloud and on-premise offerings for Azure DevOps use the same components for code builds and releases, source code control, tasks management, test plans, and artifact administration.

#### Analytics and Reporting
Azure DevOps Services and Azure DevOps Server offer numerous tools that give you perspicuity into the activity and improvement of your software projects. Some of those tools include the following:

➤ Dashboards and lightweight charts exist in both the cloud and on-premises platforms. These tools aid in data visualization for various projects.

➤ Power BI is an interactive tool for visualizing data created by Microsoft, concentrated on business intelligence. Power BI integration helps teams to get analytics data into Power BI reports. With this, you will be able to analyze and visualize data from Power BI.

➤ OData support makes it easy for teams to instantly query the analytics service through the browser. Your product team can use the query result JSON as they want.You can generate queries that span many projects or your entire organization.

#### Process Customization
Both tools use the inheritance process model to customize their work-tracking experience. These customizations can happen instantly on the user interface or programmatically by calling the REST API endpoints.

### AZURE DevOps FEATURES
The following are the Azure DevOps features:

➤ **Azure Boards:** Software development teams can use the interactive and configurable tools in Azure Boards for managing their software projects. It delivers various features, including support for agile and scrum, customizable dashboards, and reporting. As your business grows, you can scale these tools.

➤ **Azure Repos:** Azure Repos is a collection of version control and source code management tools in the Azure DevOps toolset. Version control tools are applications that help you track changes you make in your code in real time. As you update your code, you tell the version control tool to take a snapshot of your files. The version control tool saves that snapshot, and you can retrieve it later when needed.

➤ **Azure Pipelines:** Azure Pipelines instantly builds and tests code to make them available to others. It combines CI and CD to test, build, and deploy your code to any target or destination.

➤ **Azure Test Plans:** Azure Test Plans is a test management platform with all the abilities required for different testing styles and gathering feedback from stakeholders. Some testing styles include planned manual testing, user acceptance testing, and exploratory testing.

➤ **Azure Artifacts:** Azure Artifacts allows software developers to share their code effectively and handle all their packaged code from one place. With Azure Artifacts, developers can publish packages to their feeds and share them within the same team, across multiple product teams or organizations, and even publicly.

➤ **Visual Studio Marketplace:** You can download extensions for Azure DevOps from the Visual Studio Marketplace. These extensions are created by Microsoft, in collaboration with the tech community. They are add-ons that customize and advance your team’s venture with Azure DevOps. They can expand different parts of the DevOps toolchain, from managing work items to code integration and testing, pipeline builds and software releases, and team synergy

### BENEFITS OF AZURE DevOps
The following are the benefits of Azure DevOps:

➤ **Flexibility:** You don’t have to use the entire Azure DevOps suite. It is attainable to adopt each of the services independently and merge them with your existing toolchain and process.

➤ **Platform agnostic:** Azure DevOps works with various operating systems (Linux, macOS, and Windows) and programming languages.

➤ **Cloud agnostic:** Azure DevOps supports continuous delivery to other cloud providers.


## Suggested Reading
[Azure DevOps Documentation](https://learn.microsoft.com/en-us/azure/devops/user-guide/what-is-azure-devops?view=azure-devops&toc=/azure/devops/get-started/toc.json)
