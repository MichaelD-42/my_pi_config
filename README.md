# my_pi_config

My personal standard `pi` configuration — the baseline I clone when I want a fresh machine to feel like home.

Think of this repo as my agent control plane: prompts, skills, extensions, and behavior rules in one place. ⚙️

## Repo layout

- `AGENTS.md` — global behavior and coding rules
- `agents/` — specialized agent personas
- `skills/` — reusable workflow skills
- `extensions/` — custom tools/features
- `prompts/` — reusable prompt templates
- `sessions/` — local history (gitignored)

## Quick setup

```bash
# optional backup
mv ~/.pi/agent ~/.pi/agent.backup.$(date +%Y%m%d-%H%M%S)

# clone config
mkdir -p ~/.pi
git clone https://github.com/MichaelD-42/my_pi_config.git ~/.pi/agent
```

## Local-only files (gitignored)

- `auth.json`
- `settings.json`
- `sessions/`
- `.env*`
- `node_modules/`

Create local secrets after cloning:

```bash
$EDITOR ~/.pi/agent/auth.json
$EDITOR ~/.pi/agent/settings.json
```

## Agents

| Agent | Purpose |
|---|---|
| `context-builder` | Builds a solid context package before major work starts. |
| `delegate` | Routes tasks to the best specialist agent. |
| `oracle` | Gives high-level guidance for tricky decisions. |
| `planner` | Breaks goals into concrete, ordered execution steps. |
| `researcher` | Looks up external info and summarizes findings. |
| `reviewer` | Reviews output for quality, risks, and gaps. |
| `scout` | Quickly explores codebases and reports structure/patterns. |
| `worker` | Executes focused implementation tasks. |

## Extensions

| Extension | Purpose |
|---|---|
| `ask-user-question` | Adds structured one-question clarification prompts. |
| `bash-guard` | Adds safer guardrails around shell command execution. |
| `context` | Improves context gathering and packaging behavior. |
| `custom-header` | Adds custom header formatting to outputs/UI. |
| `google-image-search` | Enables Google Image search from the agent. |
| `memory` | Adds memory-style storage/retrieval behavior. |
| `subagents` | Enables delegated subagent execution workflows. |
| `video-extract` | Extracts frames/content from local or YouTube videos. |
| `web-fetch` | Fetches URLs and converts readable content to markdown. |
| `web-search` | Performs structured web search queries. |
| `youtube-search` | Searches YouTube and returns structured video metadata. |

## Skills

| Skill | Purpose |
|---|---|
| `algorithmic-art` | Creates generative/algorithmic art with code. |
| `brand-guidelines` | Applies consistent brand color and typography rules. |
| `c4-architecture` | Produces C4 architecture docs and diagrams. |
| `canvas-design` | Creates static visual designs and poster-style assets. |
| `codex` | Uses Codex CLI for deep code tasks. |
| `command-creator` | Builds reusable slash commands/workflows. |
| `commit-work` | Stages changes and crafts clean commits. |
| `crafting-effective-readmes` | Creates and improves README files by audience. |
| `daily-meeting-update` | Generates structured daily standup updates. |
| `difficult-workplace-conversations` | Prepares tough workplace conversations with structure. |
| `doc-coauthoring` | Guides structured collaborative doc writing. |
| `docx` | Creates/edits/parses Word `.docx` files. |
| `feedback-mastery` | Delivers clear, constructive feedback using frameworks. |
| `game-changing-features` | Finds high-leverage product opportunities. |
| `gemini` | Uses Gemini CLI for large-context analysis. |
| `internal-comms` | Drafts internal company communication artifacts. |
| `lesson-learned` | Extracts engineering lessons from recent work. |
| `marp-slide` | Builds polished Marp slide decks. |
| `mcp-builder` | Designs and implements MCP servers/tools. |
| `orchestrator` | Enforces top-level session orchestration discipline. |
| `pdf` | Performs end-to-end PDF operations. |
| `pptx` | Creates/edits/parses PowerPoint `.pptx` files. |
| `professional-communication` | Improves professional technical messaging. |
| `qa-test-planner` | Builds test plans, test cases, and bug reports. |
| `reddit` | Searches and reads Reddit discussions. |
| `requirements-clarity` | Clarifies ambiguous requirements before coding. |
| `retrospective` | Runs structured retrospectives after phases. |
| `session-handoff` | Creates handoff docs for session continuity. |
| `ship-learn-next` | Turns learning content into action plans. |
| `skill-creator` | Creates and iterates new skills. |
| `skill-judge` | Evaluates skill quality against best practices. |
| `stop-slop` | Removes generic AI-writing patterns from prose. |
| `test-driven-development` | Applies TDD workflow before implementation. |
| `web-to-markdown` | Converts webpages to markdown via local tooling. |
| `webapp-testing` | Tests local web apps with Playwright workflows. |
| `writing-clearly-and-concisely` | Improves writing clarity and brevity. |
| `xlsx` | Creates/edits/parses spreadsheet files. |

## Update workflow

```bash
cd ~/.pi/agent
git pull
```

## Notes

- This repo is meant to be cloned, then customized locally where needed.
- Secrets and local runtime data stay out of git by design.

## Last reviewed

2026-05-05
