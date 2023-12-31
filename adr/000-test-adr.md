# ADR-001: Adopting Architecture Decision Records

## Executive Summary

This Architecture Decision Record (ADR) establishes the use of ADRs within the
Artificial Intelligence Laboratory (AI-Lab) at Canadian Food Inspection
Agency (CFIA) for documenting key architectural decisions. An ADR is a document
designed to capture decisions across multiple projects and products and are of
such significance that they require uniform compliance from all teams involved.
We chose ADRs for their version-controlled, clear, and accessible format,
addressing issues such as repeated discussions, inconsistent approaches, and
difficulties in onboarding. The document sets the standards for ADR creation,
storage, and modification.

## Definitions

- Version control: A system that records changes to a file or set of files over
  time so that specific versions can be recalled later, like GitHub.
- Repository: A central location in which version-controlled data is stored and
  managed.
- GitHub Issue: A section on GitHub where project issues, enhancements, tasks,
  and other kinds of questions are tracked.
- GitHub Pull Request: A method of submitting contributions to an open
  development project hosted on GitHub.
- Wiki: A collaborative platform that allows for the editing of interlinked
  web pages, commonly used for documentation.
- Request for Comment (RFC): A method that enables collective deliberation
  on a particular issue or proposed feature, often formalized and version-
  controlled.
- Confluence: A collaboration software program developed by Atlassian that
  serves as an enterprise wiki and project management tool.
- Decision Log: A simple record-keeping method that logs key decisions made
  throughout the course of a project, usually lacking version control.

## Context

AI-Lab, comprised of software developers and data scientists, is dedicated to
leveraging AI technologies to address a range of challenges, both within the
organization and in external engagements. As the team and its projects have
grown, challenges have arisen in maintaining a clear and understandable history
of architectural decisions. These challenges include:

- Repeated discussions about previously made decisions: The lack of a formalized
  decision-making process means that decisions are often revisited, causing
  wasted time and effort.
- Difficulty in onboarding new team members: The absence of a single, definitive
  source for architectural decisions complicates the onboarding process.
- Inconsistent architectural approaches: Different projects or project parts
  sometimes adopt varying approaches, leading to long-term maintainability
  issues.

## Decision

After evaluating various options, we chose to implement ADRs to maintain a
version-controlled and easily accessible record of important architectural
decisions. Each ADR will detail the reasoning, background, and consequences of
significant architectural choices, not trivial decisions.

#### Example of decisions that could be addressed by ADR

- Which database engine should we use and why?
- Should we move to a microservices architecture?
- What authentication strategy should we adopt?
- How will we handle API versioning?
- What approach will we take for caching?
- Which cloud provider should we use?
- What logging and monitoring solutions will be adopted?
- Should we use containers for deployment, and if so, which orchestration tool?
- Which message broker to use for asynchronous operations?
- What is our strategy for data backup and recovery?

#### Example of decisions that should not be addressed by ADR

- What color should the login button be?
- How do we implement a specific function in code?
- What are the specific firewall rules?
- What specific libraries to use for string manipulation?
- Which individual UI components to use?
- Setting up environment variables for local development.
- Pagination limits for lists and tables.
- Algorithm to use for a single, specific task.

### Format

- Language: ADRs should be written in English for uniformity and broader reach.
  French versions should be provided eventually.
- Clarity: Aim for straightforward and simple language in the ADRs.
- Proofreading: Review each ADR for linguistic and grammatical errors before
  finalizing. Tools like Antidote can be useful.
- File Naming: ADRs will follow the naming convention XXX-tag.md, for example,
  001-ailab-using-adr.md.
  - XXX: A three-digit number to ensure ADRs are listed in numerical order.
  - tag: A descriptive tag of the decision.
- French Versions: French translations will carry the same name prefix as the
  original ADR, followed by '.fr-ca'. For example, 001-ailab-using-adr.fr-ca.md.
- Attachments: Diagrams and other attachments will carry the original ADR's
  name prefix. For example, 001-ailab-using-adr-template.md.
- Title Format: Titles should start with "ADR-XXX: ", followed by a brief
  description. Numbers should match between the file name and title.
- Sections: An ADR will include Executive Summary, Context, Decision,
  Alternatives Considered, Consequences, and References. See [ADR
  Template](./001-ailab-using-adr-template.md) for more details.

### Implicit Statuses

- PROPOSED: ADRs or modifications proposed via active GitHub pull requests and
  placed in the adr/ folder.
- ACCEPTED: ADRs merged in the main branch.
- REJECTED: GitHub pull requests that have been rejected or GitHub issues that
  led to a decision not to proceed.
- DEPRECATED: ADRs moved to the adr/archives/ folder, indicating the decision
  is void.
- SUPERSEDED: ADRs replaced by a new one and moved to adr/archives/, retaining
  their original tag but assigned a new number.
- MODIFIED: Minor changes to an existing ADR, retaining its original number and
  tag.

### Storage

- ADRs and theirs attachments will be stored in a dedicated directory within
  this [repository](https://github.com/ai-cfia/dev-rel-docs), under the folder
  adr/.
- Deprecated and superseded ADRs and their attachments will be moved to
  adr/archives/.