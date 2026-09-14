# Agent team

For Mona's Project Pulse dashboard, I will use a four-agent team defined under `.github/agents` and orchestrated through the GitHub Copilot CLI in a Codespace.

- Orchestrator — `Claude Opus 4.7 (copilot)`
  - Responsible for breaking the work into phases, assigning specialist tasks, coordinating parallel vs. sequential execution, and verifying the integrated result.
  - Definition: `.github/agents/orchestrator.agent.md`

- Planner — `Claude Opus 4.7 (copilot)`
  - Responsible for researching the repo, identifying constraints and edge cases, and creating an implementation plan with file ownership, dependencies, validation, and open questions.
  - Definition: `.github/agents/planner.agent.md`

- Coder — `GPT-5.5 (copilot)`
  - Responsible for implementing code, fixing bugs, and building the project logic within the files assigned by the Orchestrator, including runnable app support such as VS Code launch configuration when needed.
  - Definition: `.github/agents/coder.agent.md`

- Designer — `Gemini 3.1 Pro (copilot)`
  - Responsible for UI/UX direction, accessibility, information hierarchy, interaction flow, and polished dashboard styling for Project Pulse.
  - Definition: `.github/agents/designer.agent.md`

This custom team gives the project a clear division of labor: the Planner defines the strategy, the Orchestrator coordinates execution, the Coder implements the code, and the Designer shapes the dashboard experience. The workflow is managed using GitHub Copilot CLI from a Codespace, with the agents working together to build the dashboard in a structured, reviewable way.
