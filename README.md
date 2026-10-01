# GenLedge Connector

This README describes the project plan. Feature completion and deployment details remain to be confirmed.

## Partner Intro

GenLedge is an AI-powered ERP platform that uses AI agents to automate enterprise operations, including invoice processing, delivery tracking, payments, and vendor/customer interactions. Our team works with its founder and operations lead to clarify requirements and with its existing developer to extend the current prototype.

| Partner contact | Name | Email | Contact priority |
| --- | --- | --- | --- |
| Founder | To be confirmed | To be confirmed | To be confirmed |
| Operations lead | To be confirmed | To be confirmed | To be confirmed |
| Existing developer | To be confirmed | To be confirmed | To be confirmed |

Daniel is the project team's primary liaison and communicates with the partner through university email.

## Description about the project

Data and operations analysts often need to manually combine ERP records to answer questions about supplier performance, deliveries, and payments. GenLedge Connector aims to reduce this work by examining source data and a desired target dataset, proposing mappings and transformations, and preparing a pipeline for human review and execution.

The application extends an existing prototype. Approved pipelines will load analytics-ready data into a separate reporting database, helping users analyze business activity while reducing reporting queries against the operational ERP.

## Key Features

The following features define the planned MVP; implementation status must be verified before release.

- **Secure sign-in:** Access the application and manage the organization's data.
- **Data import:** Upload files or connect an organizational database to make source data available for processing.
- **Source discovery:** Inspect the discovered structure of source data, including available tables and fields.
- **AI-assisted mapping:** Generate proposed source-to-target mappings and transformations for the desired analytics dataset.
- **Mapping review:** Review and modify proposed mappings before approving a pipeline.
- **Transformation and loading:** Execute an approved pipeline to produce structured data in the target warehouse or reporting database.
- **Scheduling and monitoring:** Schedule pipeline runs and inspect their status and run history to identify failed loads.

The broader project also targets at least one meaningful customer-facing report with drill-down capability. Reporting implementation and access remain to be confirmed.

## Instructions

These steps describe the intended MVP workflow. Exact screen names, account provisioning, supported file types, and connection requirements must be confirmed against the implemented application.

1. **Access and sign in:** Open the deployed application and sign in with an authorized organizational account. The application URL and registration or administrator provisioning process are to be confirmed.
2. **Import data:** Upload a supported file or configure an authorized source database connection. Supported formats and required connection fields are to be confirmed.
3. **Inspect the source:** Review the discovered tables and fields to understand which data is available.
4. **Generate mappings:** Specify the target dataset and ask the AI agent to propose field mappings and transformations.
5. **Review and approve:** Check the proposed mappings, correct errors, and approve the pipeline configuration before execution.
6. **Run the pipeline:** Execute the approved pipeline and inspect its result. Validate the target data, including record transfer and relevant payment totals.
7. **Schedule and monitor:** Configure recurring runs when supported, then review run history and investigate failures.

**Design reference:** [Figma demo](https://www.figma.com/make/5FBkZzoaCpGV83S88IPkY1/--------CSC301-D1-Demo?p=f&t=dNeXPEpMKdHMtUZw-0). This is a design/demo reference, not a confirmed deployed application.

## Development requirements

### Planned technology stack

| Component | Technologies |
| --- | --- |
| Frontend | React, Vite, TypeScript; React Flow for the Mapping Studio |
| Backend | Node.js, TypeScript, Fastify |
| Database and ORM | PostgreSQL, Prisma |
| AI agent | LangGraph.js; Claude or OpenAI, with the provider to be decided |
| Data processing | Python |

Developers need the project repository, Node.js, Python, PostgreSQL, and authorized credentials for the selected AI provider and source/target databases. Supported operating systems, runtime versions, package managers, and exact dependencies are not specified in the planning document.

### Setup and running the application

Verified repository-specific details must be added to the following steps before this README can serve as a runnable setup guide:

1. Clone the project repository. **Repository URL: to be supplied.**
2. Install frontend, backend, and Python dependencies using the repository's dependency manifests. **Commands: to be supplied.**
3. Configure database connections, authentication, and the selected AI provider. **Environment variable names and example configuration: to be supplied.**
4. Initialize the development database using the project's Prisma configuration. **Migration and optional seed commands: to be supplied.**
5. Start the backend, data-processing components, and frontend. **Commands and local URLs: to be supplied.**
6. Verify source discovery, mapping review, pipeline execution, and target-data validation using representative test data.

Production choices involving AWS Glue, DocumentDB, S3, Redshift, Lambda, SQL/dbt, and QuickSight remain under evaluation; they are not confirmed local setup requirements.

## Deployment and Github Workflow

The team uses GitHub for source control and branches, commits, and pull requests for collaboration. Notion tracks tasks through `To Do`, `In Progress`, `Review`, and `Done`. Work is assigned during weekly meetings according to roles, dependencies, and workload.

The planning document confirms review before merging but does not specify branch names, reviewer assignments, merge ownership, or deployment tooling. The following workflow is proposed for team confirmation:

1. Create a task branch from the shared integration branch, using names such as `feature/<short-description>` or `fix/<short-description>`.
2. Implement the assigned change, coordinate changes to shared interfaces, and validate affected behavior.
3. Open a pull request back to the integration branch. At least one teammate familiar with the affected component reviews it; the designated maintainer merges after review and required checks pass.
4. Validate the integrated application end-to-end before release, including mappings, transferred records, and report totals.
5. Deploy through the process agreed with GenLedge's engineering/platform team, then verify the live workflow and pipeline status.

This proposed workflow supports review and early integration across frontend and backend work. **Integration branch, maintainer, automated checks, deployment tools/commands, hosting environment, and live verification ownership: to be confirmed.** GenLedge provides the existing prototype and infrastructure context; broader infrastructure, security, connectors, and observability remain partner responsibilities.

## Coding Standards and Guidelines

Proposed standards: use consistent formatting, descriptive names, and small, clearly scoped functions across TypeScript and Python code.
Review changes through pull requests, validate external inputs, and keep credentials outside source control; formatter and linting configurations remain to be confirmed.

## Licenses

The planning agreement permits sharing and using the software and code freely, with or without a license, for any use. A specific repository license has not yet been selected; confirm it with the partner and add a `LICENSE` file defining reuse and redistribution terms.

## Deployed URL / Access Instructions

**Deployed application URL:** To be supplied.

**Account provisioning and access requirements:** To be confirmed with GenLedge.

Until deployment is available, the [Figma demo](https://www.figma.com/make/5FBkZzoaCpGV83S88IPkY1/--------CSC301-D1-Demo?p=f&t=dNeXPEpMKdHMtUZw-0) provides a design reference. Local access instructions will be added once startup commands and development URLs are verified.

## D3 Improvement Highlight

The planning document does not record completed changes since D2. Update this section with two or three sentences identifying verified D3 improvements and the screens or steps reviewers should use to find them.
