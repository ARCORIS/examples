<div align="center">

# ARCORIS Examples

**Runnable scenarios, baselines, labs, and reference environments for the ARCORIS ecosystem.**

[![Start Here](https://img.shields.io/badge/Start-Examples%20Index-0F766E?style=flat)](docs/index.md)
[![Runnable Scenarios](https://img.shields.io/badge/Scope-Scenarios%20%26%20Baselines-1D4ED8?style=flat)](https://github.com/ARCORIS/examples)

[Core Platform](https://github.com/ARCORIS/arcoris) · [Docs](https://github.com/ARCORIS/docs) · [Handbook](https://github.com/ARCORIS/handbook) · [Community](https://github.com/ARCORIS/community) · [Enhancements](https://github.com/ARCORIS/enhancements)

Local Development · Cluster Scenarios · Adapters · Observability · Security · Failure Labs · Shared Assets

**Overview:** [Purpose](#purpose) · [Start here](#start-here) · [Intended audiences](#intended-audiences)

**Scope:** [What belongs here](#what-belongs-here) · [What does not belong here](#what-does-not-belong-here) · [Source of truth](#source-of-truth-policy)

**Structure:** [Repository map](#repository-map) · [Examples map](#examples-map) · [Example principles](#example-principles)

**Repository:** [Contributing](#contribution-expectations) · [Repository status](#repository-status)

</div>

---

## Purpose

This repository is the **runnable examples and scenario repository** for ARCORIS.

It exists to provide concrete, executable, and inspectable material that helps readers and contributors run local baselines, explore cluster layouts, validate integrations, exercise observability and security setups, and reproduce failure-oriented scenarios.

This repository is not the canonical home for stable public system explanation, engineering operating rules, or technical decision history. It is the canonical home for **runnable scenarios, baseline environments, labs, shared example assets, and example-specific guidance**.

## Start here

Use the [Examples Index](docs/index.md) as the primary entry point for example navigation, reading order, and scenario-based access paths.

The index should direct readers to overview material, conventions, tutorials, and scenario catalogs for local development, cluster layouts, adapters, observability, security, and failure-oriented labs.

## What belongs here

Use this repository for material that demonstrates **how ARCORIS can be run, explored, validated, or exercised in practice**.

Typical content includes:

- minimal local baselines for getting started quickly;
- cluster scenarios for development, high availability, and multi-node layouts;
- adapter-focused examples for supported broker and queue integrations;
- observability scenarios for logs, metrics, tracing, dashboards, alerts, and supporting assets;
- security scenarios for access control, mTLS, hardened deployments, and secrets integration;
- failure and chaos labs for backpressure, degradation, outages, partitions, recovery, and rollback practice;
- reusable shared assets such as manifests, dashboards, scripts, images, compose files, and test data;
- templates and metadata used to keep scenarios structured, portable, and reviewable.

This repository should answer questions such as:

- how do I run ARCORIS locally;
- what does a baseline cluster layout look like;
- how do I try a specific adapter or integration;
- how do I explore observability and security setups;
- how can I reproduce or study failure-oriented behavior in a controlled example.

## What does not belong here

This repository must not absorb responsibilities that belong elsewhere.

The following should live outside this repository:

- canonical public system explanation, stable architecture narratives, and user-facing conceptual guidance;
- engineering and documentation operating rules, review discipline, and standards that apply across repositories;
- major technical proposals, accepted decisions, and enhancement lifecycle tracking;
- governance, ownership, roles, meetings, and community coordination;
- implementation-near technical documentation that belongs next to source code.

If an artifact is primarily demonstrative, runnable, reproducible, or tutorial-oriented, it belongs here. If it explains the stable system, governs how work is done, records why a major change was accepted, or documents code-near behavior, it should remain in the repository that owns that responsibility.

## Repository map

ARCORIS uses multiple repositories with different responsibilities. This repository is only one layer of that system.

### Core platform

| Repository | Role |
| --- | --- |
| [Core Platform](https://github.com/ARCORIS/arcoris/blob/main/README.md) | Main code repository for the platform |

### Documentation ecosystem

| Repository | Role |
| --- | --- |
| [Docs](https://github.com/ARCORIS/docs/blob/main/README.md) | Public documentation and canonical system explanation |
| [Handbook](https://github.com/ARCORIS/handbook/blob/main/README.md) | Engineering and documentation operating rules |
| [Community](https://github.com/ARCORIS/community/blob/main/README.md) | Governance, roles, coordination, and contributor growth |
| [Enhancements](https://github.com/ARCORIS/enhancements/blob/main/README.md) | Major proposals, accepted changes, and decision history |
| Examples (this repository) | Runnable scenarios, baselines, labs, and shared example assets |

This repository should provide executable learning and validation material without taking over the stable responsibilities of the repositories that own explanation, operating rules, governance, change history, or implementation detail.

## Examples map

The repository is organized around a small set of durable, reader-facing entry points and runnable scenario spaces.

### User-facing entry points

| Section | Role |
| --- | --- |
| [Overview](docs/overview/index.md) | Mission, scope, example boundaries, example types, repository mapping, and support or stability levels |
| [Catalog](docs/catalog/index.md) | Scenario catalogs for local development, cluster layouts, adapters, observability, security, and failure labs |
| [Conventions](docs/conventions/index.md) | Structure standards, metadata rules, portability guidance, validation requirements, and safety or cleanup rules |
| [Tutorials](docs/tutorials/index.md) | Getting started, how to run scenarios, and how to interpret example results |
| [Examples Index](docs/index.md) | Primary entry point into the full examples documentation set |

### Runnable scenario spaces

| Scenario space | Role |
| --- | --- |
| [Local Baselines](scenarios/local/) | Minimal local environments for fast startup, single-node evaluation, and development workflows |
| [Cluster Baselines](scenarios/cluster/) | Multi-node, high-availability, and environment-level deployment scenarios |
| [Adapter Integrations](scenarios/adapters/) | Runnable scenarios for broker and queue adapters, including mixed-integration layouts |
| [Observability Stacks](scenarios/observability/) | Example environments for logs, metrics, tracing, dashboards, alerts, and end-to-end visibility |
| [Security Baselines](scenarios/security/) | Reference scenarios for access control, mTLS, hardened deployment, and secrets integration |
| [Failure and Chaos Labs](scenarios/failure-labs/) | Controlled labs for degradation, outages, partitions, recovery, rollback, and resilience testing |

### Shared assets and templates

| Space | Role |
| --- | --- |
| [Shared Assets](shared/) | Common manifests, scripts, dashboards, alerts, compose assets, images, and test data reused across multiple scenarios |
| [Scenario Templates](templates/) | Standard templates for new scenarios, labs, and example metadata |
| [Archived Examples](archive/) | Deprecated and experimental example material retained separately from the active scenario set |

## Intended audiences

This repository serves several audiences:

- **new users and evaluators** who need something runnable instead of only conceptual explanation;
- **contributors** who need reference scenarios for local development, validation, and experimentation;
- **operators and integrators** who need practical environment examples and configuration baselines;
- **reviewers and maintainers** who need reproducible labs to validate behavior, integrations, and failure handling;
- **future readers** who need concrete artifacts to complement system documentation.

Because these audiences differ, the repository should optimize for **runnability, clarity, portability, and scenario discoverability**.

## Source-of-truth policy

This repository should hold the canonical set of **official runnable examples and scenario baselines** for ARCORIS.

That means:

- approved example scenarios should live here;
- shared example assets should be maintained here when they are reused across scenarios;
- example conventions, support levels, and validation requirements should be discoverable here;
- deprecated and experimental example material should remain clearly separated from the active baseline set.

If a topic exists in multiple forms, the boundary is simple:

- **runnable scenario, baseline environment, lab, shared example asset, or example tutorial** -> [Examples](https://github.com/ARCORIS/examples)
- **stable public system explanation** -> [Docs](https://github.com/ARCORIS/docs)
- **operating rules, writing policy, review discipline, and standards** -> [Handbook](https://github.com/ARCORIS/handbook)
- **governance and coordination** -> [Community](https://github.com/ARCORIS/community)
- **major proposal, accepted decision, or change history** -> [Enhancements](https://github.com/ARCORIS/enhancements)
- **implementation-near technical detail** -> [Core Platform](https://github.com/ARCORIS/arcoris)

Examples may illustrate the system, but they must not replace the canonical conceptual, architectural, or policy documentation that belongs elsewhere.

## Example principles

Material in this repository should follow a small set of strict principles:

- **Examples must be runnable or clearly labeled when they are not.**
- **Scenarios must be discoverable.** Readers should be able to find the right example by goal, environment, or domain.
- **Support level must be explicit.** Stable, experimental, and deprecated material should not be mixed.
- **Shared assets should reduce duplication.** Common manifests, scripts, dashboards, and data should be reused where appropriate.
- **Safety matters.** Cleanup rules, portability guidance, validation requirements, and failure-lab boundaries should be documented clearly.
- **Repository boundaries must hold.** Examples should not become a substitute for Docs, Handbook, Community, Enhancements, or code-near technical documentation.
- **Docs-as-code rigor.** Scenarios, metadata, templates, and supporting guidance should be reviewable, versioned, and maintainable like source code.

## Contribution expectations

A good change in this repository usually does one or more of the following:

- introduces a runnable scenario with clear purpose, metadata, and validation expectations;
- improves the usability, portability, or safety of an existing example;
- adds shared assets that reduce duplication across multiple scenarios;
- strengthens tutorial guidance for running or interpreting examples;
- clarifies support level, archive status, or scenario categorization;
- removes stale, broken, misleading, or unsupported example material.

Changes should not move canonical system documentation, operating rules, governance material, proposal history, or implementation-near technical documentation into this repository.

## Repository status

This repository already reflects the core domains of example responsibility: reader-facing guidance under `docs/`, runnable scenario spaces under `scenarios/`, shared assets under `shared/`, templates for new material, and archive space for deprecated or experimental records.

The current structure also supports a strong split between **how to find and understand examples** and **where the runnable material actually lives**.

As the repository evolves, catalogs, support-level rules, scenario metadata, portability guidance, and validation discipline should continue to reinforce this repository’s role as the canonical home for official ARCORIS example material.
