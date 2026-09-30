# AI Software Engineering Team

An adaptive multi-agent AI software engineering system designed to plan, build, test, debug, review, and document software projects.

## Overview

The system acts as an AI software engineering team rather than a single coding assistant.

A central **Project Hub** coordinates specialized AI agents, manages project state, delegates tasks, and dynamically determines what should happen next based on the project's current needs.

The team can work within a self-contained project workspace containing user-provided resources, source code, generated files, execution results, and project history.

## AI Team

* **Architect Agent** — analyzes requirements and designs the system architecture
* **Developer Agent** — implements features and modifies project code
* **QA Agent** — generates and executes tests
* **Debugger Agent** — investigates failures and identifies root causes
* **Code Reviewer Agent** — reviews code quality, correctness, and maintainability
* **Documentation Agent** — generates and maintains project documentation

### Project Hub

The Project Hub acts as the central orchestrator.

Rather than following a fixed workflow, it evaluates the current project state and determines which agent should work next.

For example:

```text
Simple Task
Developer → QA

Complex Task
Architect → Developer → QA → Debugger
                         ↓
                     Developer
                         ↓
                        QA
                         ↓
                      Reviewer
                         ↓
                   Documentation
```

## Core Features

* Adaptive multi-agent orchestration
* Natural-language project requirements
* User-provided project resources
* Automated code generation and modification
* Automated testing and debugging
* Code review
* Documentation generation
* Self-contained project workspaces
* Structured agent communication
* Project state and task management
* Real-time project monitoring
* Project history and execution tracking
* English, Arabic, and Arabic-English code-switching
* Voice input and optional voice output

## Research Direction

The project explores adaptive multi-agent orchestration for software engineering.

A central research question is whether an adaptive team can complete software engineering tasks while reducing unnecessary agent interactions compared with fixed multi-agent workflows, without compromising software quality.

Potential evaluation metrics include:

* Task success
* Test success rate
* Bug and repair counts
* Repair success
* Agent invocations
* Tool invocations
* Number of iterations
* Execution time
* Model usage

## Architecture

```text
                         ┌─────────────────┐
                         │      User       │
                         └────────┬────────┘
                                  │
                                  ▼
                         ┌─────────────────┐
                         │   Project Hub   │
                         │  Orchestrator   │
                         └────────┬────────┘
                                  │
             ┌────────────────────┼────────────────────┐
             │                    │                    │
             ▼                    ▼                    ▼
        Architect            Developer                QA
             │                    │                    │
             └────────────────────┼────────────────────┘
                                  │
                                  ▼
                             Debugger
                                  │
                                  ▼
                              Reviewer
                                  │
                                  ▼
                          Documentation
                                  │
                                  ▼
                         Project Workspace
```

## Technology

The initial technology direction includes:

* **Backend:** Python · FastAPI
* **Database:** SQLite
* **AI Models:** Ollama
* **Frontend:** React
* **Real-Time Communication:** WebSockets / SSE
* **Version Control:** Git · GitHub

The system is designed with a provider-independent model layer so that different AI models and providers can be evaluated and swapped without redesigning the agents.

## Project Status

🚧 **In Development**

The project is currently in the initial architecture and implementation phase.

## Team

**Mohamed Mazen Elagamy**
**Lojan Essam Farouk**
