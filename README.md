# GenLedge Connector

GenLedge Connector is a CSC301 planning repository for an agentic data pipeline that prepares enterprise ERP records for analytics. It is useful to the GenLedge partner, teaching team, and future implementation team because it records the product problem, target users, MVP stories, architecture, team responsibilities, risks, and supporting evidence in one reviewable place.

The repository shows how a human reviewer would supervise an AI agent that proposes source-to-target mappings and transformations before data is loaded into a reporting database. The current checkout is a planning deliverable, so it provides the product specification and media assets rather than a runnable application.

## Tech Stack And Why Chosen

- **Markdown** documents the product plan in a format that is easy to review in GitHub and update through pull requests.
- **Mermaid** expresses the system architecture directly beside the written design, keeping the diagram versioned with the plan.
- **CSV** stores the enrolled team roster in a simple, portable data shape.
- **PNG and JPEG** assets provide evidence for user-story communication and team-building activities.
- **Git and GitHub pull requests** provide change history, review requests, and a shared record of planning decisions.
- **Planned product stack:** React, Vite, TypeScript, React Flow, Node.js, Fastify, PostgreSQL, Prisma, LangGraph.js, Claude or OpenAI APIs, and Python. These technologies are documented in `deliverables/D1/planning.md`; implementation code is not yet part of this repository.

## Repository Contents

- `deliverables/D1/planning.md` - the product and architecture plan, including Q1-Q14, MVP user stories, roles, risks, and mitigations.
- `deliverables/D1/` - the finalized plan's supporting images and mockup note.
- `deliverables/team/` - the team roster, stakeholder notes, and meeting information.
- `deliverables/D2/`, `deliverables/D2_R/`, and `deliverables/D3/` - later deliverable templates and reports.
- `readme-template.md` - the course README reference template.

## Install And Bootstrap

No package installation, database setup, or environment variables are required for this planning-only checkout. Bootstrap from source with Git:

```bash
git clone https://github.com/DanielZ818/1-GenLedge-AI.git
cd 1-GenLedge-AI
```

Open `deliverables/D1/planning.md` in GitHub or a Markdown viewer with Mermaid support.

## Day-To-Day Use

1. Update the relevant question or section in `deliverables/D1/planning.md` as the product decisions change.
2. Keep supporting images beside the plan so relative links continue to render.
3. Update the team files under `deliverables/team/` when roster or meeting information changes.
4. Use a branch and pull request for each focused documentation change, then request review from the team.

## Commands And Options

This repository has no executable application or command-line entrypoint yet, so it has no application flags or runtime options. The documented workflow is file review through GitHub and a Markdown viewer.

## Deployment And Access

There is no deployed application or runtime access URL in this planning phase. Product references are linked from the plan, including the pipeline visualization, GenLedge platform diagram, and Figma mockup.

## License And Sharing

The planning document records that the team may share the project code and documentation freely. A repository license has not yet been selected with the partner.
