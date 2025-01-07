# Qwen Orchestrator — Multi-Agent AI Development Team for Qwen Code

**English** · [Español](docs/README.es.md) · [中文](docs/README.zh.md) · [日本語](docs/README.ja.md) · [한국어](docs/README.ko.md) · [Português](docs/README.pt.md) · [Français](docs/README.fr.md) · [العربية](docs/README.ar.md)

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-0.0.6-green.svg)](package.json)
[![Qwen Code Extension](https://img.shields.io/badge/Qwen%20Code-Extension-orange.svg)](https://github.com/QwenLM/qwen-code)
[![Agents: 24](https://img.shields.io/badge/agents-24-blue.svg)](#-agent-team-24-specialized-agents)
[![Skills: 82](https://img.shields.io/badge/skills-82-purple.svg)](#-skills-82-professional-skills)

> 🤖 **The enterprise-grade multi-agent AI orchestration extension exclusively for [Qwen Code CLI](https://github.com/QwenLM/qwen-code)**
>
> Turn your AI coding assistant into a full **software development department** — 24 specialized agents, 82 professional skills, 6 slash commands, persistent memory, and MCP tool integration.
>
> **Author:** [Omar-Obando](https://github.com/Omar-Obando) · **License:** MIT · **Version:** 0.0.6

---

## 📑 Table of Contents

- [What is Qwen Orchestrator?](#-what-is-qwen-orchestrator)
- [Quick Install](#-quick-install)
- [Quick Start](#-quick-start)
- [Key Features](#-key-features)
- [Agent Team (24 Specialized Agents)](#-agent-team-24-specialized-agents)
- [Skills (82 Professional Skills)](#-skills-82-professional-skills)
- [Commands (6 Slash Commands)](#-commands-6-slash-commands)
- [How It Works](#-how-it-works)
  - [Execution Flow](#execution-flow)
  - [User Clarity: Ask Before Building](#user-clarity-ask-before-building)
  - [Architecture Diagram](#architecture-diagram)
- [Installation Guide](#-installation-guide)
  - [Quick Install (Recommended)](#quick-install-recommended)
  - [Manual Install](#manual-install)
  - [MCP Tools Server (Optional)](#mcp-tools-server-optional)
  - [Troubleshooting](#troubleshooting)
- [Model Configuration](#-model-configuration)
- [CLI Mode Recommendations](#-cli-mode-recommendations)
- [Advanced Tools](#-advanced-tools)
  - [Inter-Agent Communication](#inter-agent-communication)
  - [Real-Time Monitoring](#real-time-monitoring)
  - [Scheduled Tasks](#scheduled-tasks)
- [Integrations](#-integrations)
  - [Context7 (Optional)](#context7-optional)
  - [MCP Memory Server](#mcp-memory-server)
  - [UI/UX Skills (Recommended)](#uiux-skills-recommended)
- [Quality Standards](#-quality-standards)
- [Project Structure](#-project-structure)
- [First Usage Examples](#-first-usage-examples)
- [Documentation](#-documentation)
- [Author](#-author)
- [Keywords](#-keywords)

---

## ⚡ What is Qwen Orchestrator?

**Qwen Orchestrator** is a powerful extension built exclusively for **[Qwen Code](https://github.com/QwenLM/qwen-code)** — the open-source AI coding CLI by Alibaba. It transforms a single AI coding assistant into a **coordinated team of 24 specialized AI agents** that work together like a professional software development department.

### Why Qwen Orchestrator?

Imagine having an entire engineering team at your fingertips: a **Commander** that orchestrates, a **Planner** that architects, **Frontend and Backend Developers** that code in parallel, a **Reviewer** that gatekeeps quality, a **QA Engineer** that tests, a **Cybersecurity Engineer** that audits vulnerabilities, a **DevOps Engineer** that deploys — and 16 more specialists, all coordinated automatically.

**No other AI coding extension provides this level of professional multi-agent orchestration.**

### Built Exclusively For

<table>
<tr>
<td width="80" align="center">

![Qwen Code](https://img.shields.io/badge/Qwen%20Code-CLI-orange?style=for-the-badge)

</td>
<td>

**[Qwen Code](https://github.com/QwenLM/qwen-code)** by [QwenLM / Alibaba](https://github.com/QwenLM) — The open-source AI-powered coding assistant CLI that supports multiple LLM providers (Qwen, DeepSeek, OpenAI, Anthropic, local models). Qwen Orchestrator is a **community-built extension** and is not affiliated with or endorsed by Alibaba.

</td>
</tr>
</table>

> ⚠️ **This extension ONLY works with [Qwen Code CLI](https://github.com/QwenLM/qwen-code)**. It is NOT a standalone tool, NOT a VS Code extension, and NOT compatible with other AI coding assistants. If you don't have Qwen Code installed, [install it first](https://github.com/QwenLM/qwen-code#installation).
>
> ⚠️ **IDE Compatibility Notice**: This extension has NOT been tested with Visual Studio, VS Code extensions, JetBrains IDEs, or any integrations outside of the Qwen Code CLI. It is designed exclusively for the Qwen Code terminal/CLI experience.

---

## 🚀 Quick Install

```bash
qwen extensions install https://github.com/Omar-Obando/qwen-orchestrator
```

That's it! The extension automatically registers all 24 agents, 82 skills, 6 commands, and the MCP Memory Server.

> 📖 See the full [Installation Guide](#-installation-guide) for manual install, MCP tools server setup, and troubleshooting.

---

## 🎯 Quick Start

Once installed, just type in your Qwen Code CLI:

```bash
/orchestrator Create a REST API for user management
/orchestrator Build a responsive e-commerce website
/plan Design a database schema for a blog
/review Check all authentication controllers
/test Run all tests in the current project
/deploy Deploy the application to production
```

The `/orchestrator` command is the main entry point. It activates the full 24-agent team with the complete professional workflow:

1. **CLARIFY** → Asks targeted questions if anything is ambiguous
2. **DISCOVER** → Scans your project, detects tech stack, reads configs
3. **PLAN** → Decomposes the mission into milestones with parallel execution groups
4. **EXECUTE** → Launches specialized agents simultaneously for max throughput
5. **VERIFY** → Reviewer + QA confirm everything works, zero regressions
6. **DELIVER** → Summary of what was built, changed, and evidence

---

## 🌟 Key Features

| Feature                    | Description                                                                                                     |
| -------------------------- | --------------------------------------------------------------------------------------------------------------- |
| **24 Specialized Agents**  | Commander, Planner, Frontend/Backend Devs, Reviewer, QA, PM, DevOps, Security, and more                         |
| **82 Professional Skills** | TDD, security audit, anti-pattern detection, design system, SQL best practices, Docker, Kubernetes, and 75 more |
| **6 Slash Commands**       | `/orchestrator`, `/orchestrate`, `/plan`, `/review`, `/test`, `/deploy`                                         |
| **Ask Before Building**    | Agents ask clarifying questions via `AskUserQuestion` before writing code                                       |
| **Parallel Execution**     | Commander delegates tasks to multiple agents simultaneously                                                     |
| **Persistent Memory**      | Knowledge Graph via MCP Memory Server stores decisions across sessions                                          |
| **Zero Model Lock-In**     | Works with Qwen, DeepSeek, OpenAI, Anthropic, or any local model                                                |
| **Multi-Language**         | TypeScript, PHP (Laravel), Python (Django), Dart (Flutter), Rust, Go, Java, C#                                  |
| **Loop Protection**        | Monitor agent detects and breaks LLM infinite loops automatically                                               |
| **Quality Gates**          | Reviewer is the ONLY agent that can approve tasks                                                               |
| **Security First**         | OWASP Top 10 compliance via security-audit skill and Reviewer agent                                             |
| **No Mockups**             | Agents are forbidden from writing stubs or placeholders                                                         |
| **Compaction Recovery**    | State persists to `.qwen-orchestrator/` — survives context window compression                                   |

---

## 👥 Agent Team (24 Specialized Agents)

| #   | Agent                     | Role                    | Superpower                                  |
| --- | ------------------------- | ----------------------- | ------------------------------------------- |
| 1   | **Commander** 🔴          | Master Orchestrator     | Parallel delegation, relentless execution   |
| 2   | **Planner** 🔵            | Research & Architecture | File-level planning, design decisions       |
| 3   | **Frontend Developer** 🔵 | UI/UX Implementation    | Components, responsive, accessible, fast    |
| 4   | **Backend Developer** 🟢  | Server-Side Logic       | APIs, auth, caching, database ops           |
| 5   | **Reviewer** 🟣           | Quality Gatekeeper      | ONLY agent that can approve tasks           |
| 6   | **QA Engineer** 🟠        | Quality Assurance       | Test strategy, edge case discovery          |
| 7   | **Project Manager** 🔵    | Delivery Management     | Scope control, risk assessment              |
| 8   | **Doc Researcher** 🟣     | Context7 Knowledge      | Live doc lookup, anti-hallucination         |
| 9   | **Tech Lead** 🟡          | Standards & Guidance    | Module completeness, CRUD verification      |
| 10  | **Database Architect** 🟢 | Data Layer Specialist   | Schema design, migration safety             |
| 11  | **Product Owner** 🟡      | Business Value          | User stories, acceptance criteria           |
| 12  | **DevOps Engineer** 🔘    | Infrastructure          | CI/CD, Docker, deployment automation        |
| 13  | **Code Quality Guard** 🌹 | Quality Sentinel        | Syntax check, lint, typecheck               |
| 14  | **Monitor** 🛡️            | Loop Guardian           | Detect/break LLM loops, runtime watchdog    |
| 15  | **SEO Specialist** 🔵     | SEO & Web Performance   | Meta tags, structured data, Core Web Vitals |
| 16  | **Tech Selector** 🟣      | Technology Advisor      | Framework/DB selection with pros/cons       |
| 17  | **Cybersecurity Eng.** 🔴 | Application Security    | OWASP, threat modeling, dependency audit    |
| 18  | **Performance Eng.** ⚡   | Speed & Scale           | Profiling, query optimization, load testing |
| 19  | **Release Manager** 🏷️    | Release & Versioning    | SemVer, changelogs, rollback planning       |
| 20  | **API Specialist** 🔗     | API & Integration       | REST/GraphQL, versioning, third-party APIs  |
| 21  | **Mobile Engineer** 📱    | Mobile Apps             | Flutter, React Native, offline-first        |
| 22  | **Localization Eng.** 🌐  | i18n/L10n               | Multi-language, RTL, cultural adaptation    |
| 23  | **Documenter** 📄         | Technical Writing       | README, API docs, ADRs, knowledge base      |
| 24  | **Skill Creator** 🛠️      | Skill Authoring         | Skill creation, documentation, testing      |

---

## 🛠️ Skills (82 Professional Skills)

### Containerization & Orchestration

| Skill                    | Purpose                                                                    |
| ------------------------ | -------------------------------------------------------------------------- |
| Docker Containerization  | Multi-stage builds, security hardening, image optimization, Docker Compose |
| Kubernetes Orchestration | Deployments, HPA, service mesh, ingress, GitOps with ArgoCD/Flux           |

### Infrastructure as Code

| Skill         | Purpose                                                             |
| ------------- | ------------------------------------------------------------------- |
| Terraform IaC | Modules, state management, workspaces, Sentinel policies, Terratest |

### CI/CD Automation

| Skill                | Purpose                                                                 |
| -------------------- | ----------------------------------------------------------------------- |
| GitHub Actions CI/CD | Workflows, matrices, environments, caching, composite actions, security |

### Caching & Performance

| Skill         | Purpose                                                                       |
| ------------- | ----------------------------------------------------------------------------- |
| Redis Caching | Data structures, caching patterns, session management, pub/sub, Lua scripting |

### API Design

| Skill              | Purpose                                                             |
| ------------------ | ------------------------------------------------------------------- |
| GraphQL API Design | Schema design, resolvers, DataLoader, pagination, Apollo Federation |

### Multi-Platform

| Skill              | Purpose                                                                             |
| ------------------ | ----------------------------------------------------------------------------------- |
| Multi-Platform Dev | Cross-platform commands, path handling, line endings, permissions, package managers |

### LLM & Agents

| Skill            | Purpose                                                          |
| ---------------- | ---------------------------------------------------------------- |
| LangGraph        | Agent workflows, state management, multi-agent systems           |
| LangChain        | LLM chains, agents, tools, memory, RAG                           |
| Qwen Agent       | Qwen-specific agent development and integration                  |
| LLM Integrations | Multi-provider LLM integration (OpenAI, Anthropic, Google, etc.) |

### Cloud Platforms

| Skill              | Purpose                                                    |
| ------------------ | ---------------------------------------------------------- |
| Vercel Deployment  | Serverless functions, edge computing, Next.js optimization |
| Cloudflare Pages   | Edge functions, global distribution, caching               |
| Cloudflare Workers | Edge computing, request/response manipulation              |
| AWS Serverless     | Lambda, API Gateway, SAM, event-driven architectures       |

### SEO

| Skill         | Purpose                                                             |
| ------------- | ------------------------------------------------------------------- |
| SEO LLM       | Optimization for ChatGPT, Perplexity, Gemini, Claude, Bing AI, Qwen |
| Technical SEO | Site speed, mobile optimization, structured data, Core Web Vitals   |

### Leadership & Architecture

| Skill                      | Purpose                                                              |
| -------------------------- | -------------------------------------------------------------------- |
| Strategic Leadership       | Team management, decision-making, stakeholder alignment              |
| Requirements Engineering   | Use cases, user stories, acceptance criteria                         |
| Microservices Architecture | Domain-driven design, service boundaries, event-driven communication |
| Technology Evaluation      | Framework/DB selection, pros/cons analysis                           |

### Product & Team

| Skill         | Purpose                                                  |
| ------------- | -------------------------------------------------------- |
| Product Owner | Backlog management, user stories, sprint planning        |
| Scrum Master  | Ceremony facilitation, team coaching, impediment removal |

### Software Development

| Skill                 | Purpose                                               |
| --------------------- | ----------------------------------------------------- |
| Testing Strategy      | Test pyramid, coverage targets, automation            |
| Security Auditor      | OWASP Top 10, vulnerability assessment, compliance    |
| DevOps Pipeline       | CI/CD design, deployment strategies, IaC              |
| Architecture Patterns | Layered, DDD, microservices, event-driven, CQRS       |
| Documentation         | README, API docs, ADRs, knowledge base                |
| Debugging             | Systematic investigation, hypothesis-driven debugging |
| Refactoring           | Code smell detection, safe transformations            |

### Security & Quality

| Skill                | Purpose                                                    |
| -------------------- | ---------------------------------------------------------- |
| Security Code Review | OWASP Top 10, vulnerability patterns, secure coding        |
| Threat Modeling      | STRIDE, DREAD, attack trees, threat identification         |
| Test Automation      | Framework design, page object patterns, parallel execution |
| Load Testing         | Load, stress, endurance, spike testing                     |
| Code Review          | OWASP + SOLID + Clean Code systematic review               |

### Database & Data

| Skill               | Purpose                                               |
| ------------------- | ----------------------------------------------------- |
| Database Design     | Schema design, relationships, indexing strategies     |
| Database Security   | Encryption, access control, audit logging, compliance |
| SQL Best Practices  | Query optimization, indexing, N+1 prevention          |
| SQL Query Assistant | Query assistance, best practices, optimization        |

### Frontend & Mobile

| Skill              | Purpose                                                     |
| ------------------ | ----------------------------------------------------------- |
| Accessibility      | WCAG 2.1 AA, semantic HTML, ARIA, keyboard navigation       |
| Design System      | Color palettes, typography, spacing, component architecture |
| Website Redesign   | URL/screenshot-based redesign, analysis workflow            |
| Flutter Web        | Responsive layouts, adaptive widgets, state management      |
| Mobile Performance | App optimization, startup time, memory usage                |
| Offline-First      | Local storage, sync, conflict resolution                    |

### Backend & APIs

| Skill                   | Purpose                                                 |
| ----------------------- | ------------------------------------------------------- |
| API Design              | RESTful standards, response envelopes, pagination       |
| API Documentation       | OpenAPI specification, Swagger, GraphQL schemas         |
| Third-Party Integration | Stripe, PayPal, AWS, Google, Twilio                     |
| Laravel                 | Eloquent ORM, Form Requests, queues, API patterns       |
| NestJS                  | Modules, guards, pipes, interceptors, request lifecycle |
| Supabase                | RLS policies, Edge Functions, auth, auto-generated APIs |

### DevOps & Infrastructure

| Skill             | Purpose                                                  |
| ----------------- | -------------------------------------------------------- |
| Disaster Recovery | Backup strategies, restore procedures, failover, RTO/RPO |
| Release Workflow  | SemVer, changelogs, staging, production, rollback        |
| Git Workflow      | Branching strategies, commit conventions, PR templates   |
| Deployment        | CI/CD, Docker, release management                        |

### LLM-Specific

| Skill               | Purpose                                                |
| ------------------- | ------------------------------------------------------ |
| Anti-Hallucination  | Source verification, evidence-based claims, validation |
| Loop Detection      | LLM loop detection, tool call loops, escape routes     |
| Context7 Docs       | Live documentation lookup via Context7 MCP             |
| Compaction Recovery | Context preservation across session compaction         |

### Project & Team

| Skill                    | Purpose                                               |
| ---------