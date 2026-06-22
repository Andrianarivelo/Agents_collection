# Agents_collection

A curated set of Claude Code subagents for scientists.

Most agents are drawn from
[VoltAgent/awesome-claude-code-subagents](https://github.com/VoltAgent/awesome-claude-code-subagents)
and the official `code-simplifier` plugin. `qt-ui-specialist` is a custom agent
written for PySide6 / PyQt5 / pyqtgraph desktop work.

## Install

Clone (or copy the `.md` files) into your Claude Code user agents directory so
they are available across every project on the machine.

**Windows (PowerShell):**
```powershell
git clone https://github.com/Andrianarivelo/Agents_collection.git "$env:USERPROFILE\.claude\agents"
```

**macOS / Linux:**
```bash
git clone https://github.com/Andrianarivelo/Agents_collection.git ~/.claude/agents
```

Reload Claude Code (or run `/agents`) to confirm they register. For a
project-specific subset, copy individual files into `<project>/.claude/agents/`
instead, which overrides the user-level version inside that project.

## Agents

### Core development (daily drivers)
| Agent | Purpose |
|---|---|
| `python-pro` | Type-safe, production-ready Python. |
| `qt-ui-specialist` | PySide6 / PyQt5 / pyqtgraph desktop GUIs, threading, packaging. |
| `code-reviewer` | Quality and security review of diffs. |
| `code-simplifier` | Light, behavior-preserving polish on recently changed code. |
| `refactoring-specialist` | Deeper structural cleanup without changing behavior. |
| `debugger` | Root-cause analysis of failures and stack traces. |
| `test-automator` | Build and extend automated test suites. |
| `code-commenter` | Adds clear docstrings and explanatory comments without changing behavior. |

### Languages
| Agent | Purpose |
|---|---|
| `rust-engineer` | Memory safety, ownership, zero-cost abstractions, async. |
| `cpp-pro` | Modern C++20/23, templates, zero-overhead abstractions. |

### Data, ML and research
| Agent | Purpose |
|---|---|
| `data-scientist` | Statistical analysis and predictive modeling. |
| `data-engineer` | Data pipelines, ETL/ELT, data infrastructure. |
| `reinforcement-learning-engineer` | RL environments, policy gradients, reward design. |
| `performance-engineer` | Find and remove performance bottlenecks. |
| `scientific-literature-researcher` | Evidence-grounded answers from research papers. |
| `scientific-figure-designer` | Nature-style, colorblind-safe publication figures with statistical annotation and vector export. |

### Project support
| Agent | Purpose |
|---|---|
| `build-engineer` | Build performance and packaging. |
| `dependency-manager` | Audit dependencies, resolve conflicts, automate updates. |
| `git-workflow-manager` | Branching strategy and merge management. |
| `documentation-engineer` | Documentation systems and developer docs. |
| `readme-generator` | Repository-accurate README generation. |

## Format

Each agent is a Markdown file with YAML frontmatter (`name`, `description`,
optional `tools` and `model`) followed by the agent's system prompt. Claude Code
selects an agent by matching a request against its `description`, or you can
invoke one explicitly by name.
