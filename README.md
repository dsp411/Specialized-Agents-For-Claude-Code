# Specialized-Agents-For-Claude-Code (AGENCY AGENTS)

A complete AI agency at your fingertips - From frontend wizards to Reddit community ninjas, from whimsy injectors to reality checkers. Each agent is a specialized expert with personality, processes, and proven deliverables.

# What Is This?
The Agency is a massive, open-source collection of 209 AI agent personalities, sorted into 15 departments. Each agent is not just a generic prompt template — it has a defined role, a unique personality, a communication style, specific workflows, and real deliverables with code examples.

Think of it like an org chart for AI. Instead of chatting with one overworked AI, you install this repo and now you have an entire force of specialised sub-agents. A Frontend Developer. A Growth Hacker. A Penetration Tester. Even a Whimsy Injector (that’s a real one).

It works natively with Claude Code, Cursor, GitHub Copilot, Antigravity (Gemini), Gemini CLI, Aider, Windsurf, OpenCode, Kimi Code, Codex, and more.
The 15 Departments (Full Breakdown)
Here’s every department and the number of agents inside each one:

#
Department
Agents
Key Roles

1
Engineering

30
Frontend Dev, Backend Architect, AI Engineer, DevOps, SRE, Prompt Engineer, Data Engineer

2
Design

9
UI Designer, UX Researcher, Brand Guardian, Whimsy Injector, Image Prompt Engineer

3
Marketing

35
Growth Hacker, SEO, Content Creator, TikTok Strategist, Instagram Curator, LinkedIn Creator

4
Sales

10
Outbound Strategist, Discovery Coach, Deal Strategist, Sales Engineer, Pipeline Analyst

5
Paid Media

7
PPC Strategist, Search Query Analyst, Paid Media Auditor, Tracking Specialist, Creative Strategist

6
Product

5
Sprint Prioritizer, Trend Researcher, Feedback Synthesizer, Behavioral Nudge Engine, PM

7
Project Mgmt

7
Studio Producer, Project Shepherd, Experiment Tracker, Meeting Notes Specialist

8
Testing

8
Evidence Collector, Reality Checker, Performance Benchmarker, API Tester, Accessibility Auditor

9
Security

10
Security Architect, AppSec Engineer, Penetration Tester, Incident Responder, Compliance Auditor

10
Support

6
Support Responder, Analytics Reporter, Finance Tracker, Infrastructure Maintainer

11
Spatial Computing

6
XR Interface Architect, visionOS Engineer, WebXR Developer, macOS Metal Engineer

12
Specialized

47
MCP Builder, Workflow Architect, Salesforce Architect, Business Strategist, Customer Service

13
Finance

5
Bookkeeper, Financial Analyst, FP&A Analyst, Investment Researcher, Tax Strategist

14
Game Dev

18
Game Designer, Level Designer, Unity/Unreal/Godot/Blender/Roblox specialists

15
Academic

5
Anthropologist, Geographer, Historian, Narratologist, Psychologist



⚠️ Total: 209 agents, all free, all open source under the MIT license.

Prerequisites
Before you start, make sure you have the following installed on your machine:

Tool
Why You Need It
Install / Check
Git
To clone the repo from GitHub
git --version
Bash / Terminal
Run install scripts (Mac/Linux terminal or Git Bash on Windows)
Built-in on Mac/Linux
An AI Coding Tool
Claude Code, Cursor, Antigravity, Copilot, Gemini CLI, Aider, Windsurf, etc.
At least one installed

⚠️ Windows users: Use Git Bash, WSL, or any Unix-like terminal. The install scripts are bash-based.
Step-by-Step Installation
Step 1: Clone the Repository
Open your terminal and run:
git clone https://github.com/msitarzewski/agency-agents.git
cd agency-agents

This downloads all 209 agent markdown files and the install scripts to your machine.
Step 2: Choose Your Install Method
You have three options depending on what tool you use:

Option A — Claude Code (Recommended)
Agents are native markdown files. No conversion needed. Just run:
./scripts/install.sh --tool claude-code
This copies all agent .md files to:
~/.claude/agents/

To install only specific departments (faster, lighter):
./scripts/install.sh --tool claude-code --division engineering,security
./scripts/install.sh --tool claude-code --division marketing,sales

Option B — Cursor
Agents are converted to .mdc rule files:
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool cursor
This creates rule files in:
.cursor/rules/
Cursor auto-detects them in your project directory.

Option C — Antigravity (Gemini)
Each agent becomes a skill:
./scripts/install.sh --tool antigravity
Skills are installed to:
~/.gemini/antigravity/skills/agency-<slug>/

Option D — Interactive Installer (Multi-Tool)
If you use multiple tools, the interactive installer auto-detects everything:
./scripts/install.sh
This opens a checkbox UI that scans your system and lets you pick exactly which tools to install for. It detects Claude Code, Cursor, Copilot, Antigravity, and more automatically.

All Supported Tools (Complete List)
The repo supports 12 AI coding tools. Here’s the full list with their install commands:

Tool
Install Command
Agent Location
Claude Code
./scripts/install.sh --tool claude-code
~/.claude/agents/
GitHub Copilot
./scripts/install.sh --tool copilot
~/.github/agents/ + ~/.copilot/agents/
Antigravity
./scripts/install.sh --tool antigravity
~/.gemini/antigravity/skills/
Gemini CLI
./scripts/install.sh --tool gemini-cli
~/.gemini/extensions/agency-agents/
OpenCode
./scripts/install.sh --tool opencode
.opencode/agents/
Cursor
./scripts/install.sh --tool cursor
.cursor/rules/
Aider
./scripts/install.sh --tool aider
./CONVENTIONS.md
Windsurf
./scripts/install.sh --tool windsurf
./.windsurfrules
OpenClaw
./scripts/install.sh --tool openclaw
~/.openclaw/agency-agents/
Qwen Code
./scripts/install.sh --tool qwen
.qwen/agents/
Kimi Code
./scripts/install.sh --tool kimi
~/.config/kimi/agents/
Codex
./scripts/install.sh --tool codex
~/.codex/agents/


⚠️ Some tools (Gemini CLI, OpenClaw, Qwen, Kimi, Codex) need a conversion step first: run ./scripts/convert.sh --tool <tool-name> before install.
Advanced Install Options
Install Only Specific Departments
Don’t need all 15 divisions? Pick only what you want:
./scripts/install.sh --tool claude-code --division engineering,security
./scripts/install.sh --tool cursor --division marketing,sales,product
Install Only Specific Agents
Want just a handful of agents? Specify them by name:
./scripts/install.sh --tool cursor --agent frontend-developer,ui-designer
List All Available Teams
See every team and how many agents are in each:
./scripts/install.sh --list teams
Dry Run (Preview Without Installing)
Check what would be installed without actually doing it:
./scripts/install.sh --tool opencode --division engineering --dry-run
Parallel Install (Faster on Multi-Core Machines)
Use the --parallel flag to speed up installation:
./scripts/convert.sh --parallel
./scripts/install.sh --no-interactive --parallel
./scripts/install.sh --no-interactive --parallel --jobs 8
Non-Interactive (CI/Automation)
For scripts and CI pipelines:
./scripts/install.sh --no-interactive --tool all

How to Use the Agents
Activating Agents in Claude Code
Once installed, just reference any agent by name in your Claude Code session:

Use the Frontend Developer agent to review this component.

Activate Backend Architect mode and help me design this API.

Use the Security Architect agent to threat-model this system.

Claude Code will pick up the agent’s personality, expertise, workflows, and deliverable patterns from the installed .md file automatically.
Activating Agents in Cursor
Rules are auto-applied when Cursor detects them in your project. Reference them explicitly:
Use the @security-engineer rules to review this code.
Activating Agents in Antigravity (Gemini)
Reference agents as skills:
@agency-frontend-developer review this React component
Multi-Agent Orchestration
The repo includes an Agents Orchestrator in the Specialized division. This agent coordinates multiple sub-agents for complex projects. Example scenario:

Building a startup MVP? Use Frontend Dev + Backend Architect + Growth Hacker + Rapid Prototyper + Reality Checker.
Marketing campaign launch? Use Content Creator + Twitter Engager + Instagram Curator + Reddit Community Builder + Analytics Reporter.
Enterprise feature? Use Senior PM + Senior Developer + UI Designer + Experiment Tracker + Evidence Collector + Reality Checker.
What Each Agent File Contains
Every agent .md file is a complete personality spec with these sections:

Identity & Memory: The agent’s name, personality traits, communication style, and voice.
Core Mission: What the agent does and its primary objectives.
Critical Rules: Domain-specific rules the agent follows (e.g., security best practices for the Security Architect).
Technical Deliverables: Real code examples, templates, and output formats the agent produces.
Workflow Process: Step-by-step workflows the agent follows for common tasks.
Success Metrics: Measurable outcomes and quality standards.
Communication Style: How the agent talks, responds, and interacts.

This is what makes The Agency different from a prompt library. These aren’t one-off prompts — they’re full agent systems with depth.
Top 10 Agents to Try First
If you’re not sure where to start, these are the most universally useful ones:

#
Agent
What It Does
1
Frontend Developer
React/Vue/Angular, pixel-perfect UIs, Core Web Vitals optimisation, component design
2
Backend Architect
API design, database architecture, microservices, scalability patterns
3
Code Reviewer
Constructive code review, security checks, maintainability, PR reviews
4
Growth Hacker
User acquisition, viral loops, conversion optimisation, rapid experimentation
5
SEO Specialist
Technical SEO, content strategy, link building, organic growth
6
Security Architect
Threat modeling, secure-by-design, trust boundaries, defense-in-depth
7
Prompt Engineer
LLM prompt design, optimisation, turning vague instructions into reliable AI behaviours
8
Product Manager
Discovery, PRDs, roadmap planning, GTM, outcome measurement
9
Content Creator
Multi-platform content, editorial calendars, copywriting, brand storytelling
10
Reality Checker
Evidence-based certification, quality gates, production readiness checks


Repo Folder Structure
Here’s what the cloned repo looks like on your machine:

agency-agents/
├── academic/            ← Anthropologist, Historian, Psychologist, etc.
├── design/              ← UI Designer, UX Researcher, Brand Guardian, etc.
├── engineering/          ← Frontend Dev, Backend Architect, AI Engineer, etc.
├── finance/             ← Bookkeeper, Financial Analyst, Tax Strategist, etc.
├── game-development/    ← Unity, Unreal, Godot, Blender, Roblox agents
├── integrations/        ← Tool-specific generated files (Cursor, Aider, etc.)
├── marketing/           ← Growth Hacker, SEO, Content Creator, etc.
├── paid-media/          ← PPC Strategist, Search Query Analyst, etc.
├── product/             ← Sprint Prioritizer, Trend Researcher, PM, etc.
├── project-management/  ← Studio Producer, Project Shepherd, etc.
├── sales/               ← Outbound Strategist, Deal Strategist, etc.
├── scripts/             ← install.sh, convert.sh (the magic)
├── security/            ← Security Architect, Pen Tester, etc.
├── spatial-computing/   ← XR, visionOS, WebXR agents
├── specialized/         ← MCP Builder, Workflow Architect, etc.
├── support/             ← Analytics Reporter, Finance Tracker, etc.
└── testing/             ← Reality Checker, API Tester, etc.
Real-World Workflow Examples
Workflow 1: Code Review Pipeline
Use three agents together for a production-ready review:

Code Reviewer — runs first pass on your PR (style, bugs, maintainability)
Security Architect — scans for threat vectors, injection points, auth issues
Reality Checker — final production readiness sign-off
Workflow 2: Landing Page Build
Full-stack agent team for a launch page:

UI Designer — design system, colour palette, component library
Frontend Developer — builds the React components
SEO Specialist — meta tags, schema markup, page speed audit
Content Creator — all copy, headlines, CTAs
Workflow 3: B2B Outreach Campaign
Sales + Marketing agents working in parallel:

Outbound Strategist — ICP targeting, signal-based prospecting
LinkedIn Content Creator — thought leadership posts, professional audience building
Email Marketing Strategist — lifecycle email sequences, segmentation
Discovery Coach — prep for discovery calls, qualifying opportunities
Troubleshooting
"Permission denied" when running install.sh
Make the script executable first:
chmod +x ./scripts/install.sh
chmod +x ./scripts/convert.sh
Agents not showing up in Claude Code
Check they were copied to the right folder:
ls ~/.claude/agents/
If the folder is empty, re-run the install command. If the folder doesn’t exist, create it manually first:
mkdir -p ~/.claude/agents/
OpenCode only registers ~119 agents
This is a known upstream bug. The workaround is to install only specific divisions:
./scripts/install.sh --tool opencode --division engineering,security
Conversion fails for some tools
Make sure you run convert.sh BEFORE install.sh for tools that need it:
./scripts/convert.sh --tool gemini-cli
./scripts/install.sh --tool gemini-cli
Windows-Specific Issues
The install scripts are bash-based. On Windows, use one of these:
Git Bash (comes with Git for Windows)
WSL (Windows Subsystem for Linux)
Any Unix-like terminal (MinGW, Cygwin)
Keeping It Updated
The repo is actively maintained (326+ commits). To update your local copy:

cd agency-agents
git pull origin main

Then re-run the install script for your tool to pick up any new or updated agents:
./scripts/install.sh --tool claude-code
Contributing Your Own Agents
The repo is open source and welcomes contributions. To add a new agent:

Fork the repository on GitHub
Create a new .md file in the appropriate department folder
Follow the agent template structure (Identity, Core Mission, Critical Rules, Deliverables, Workflow, Metrics)
Submit a Pull Request

Quick Reference Cheat Sheet
Save this page. These are the commands you’ll use most:

What You Want to Do
Command
Clone the repo
git clone https://github.com/msitarzewski/agency-agents.git
Install for Claude Code
./scripts/install.sh --tool claude-code
Install for Cursor
./scripts/install.sh --tool cursor
Install for Antigravity
./scripts/install.sh --tool antigravity
Install for Copilot
./scripts/install.sh --tool copilot
Interactive installer
./scripts/install.sh
Install specific departments
--division engineering,security
Install specific agents
--agent frontend-developer,ui-designer
List all teams
./scripts/install.sh --list teams
Preview without installing
--dry-run
Update to latest
cd agency-agents && git pull origin main
Convert for other tools
./scripts/convert.sh --tool <name>
Parallel (faster)
Add --parallel to any command

