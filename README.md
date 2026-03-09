# Infinite Agentic Loop POC

> **Watch the Tutorial**: [Infinite Agentic Loop with Claude Code](https://youtu.be/9ipM_vDwflI)

An experimental project demonstrating Infinite Agentic Loop in a two prompt system using Claude Code.

<img src="images/infinite-claude-img.png" alt="Infinite Agentic Loop" style="max-width: 800px; width: 100%;">

## Overview

This project uses a custom Claude Code slash command (`/project:infinite`) to orchestrate multiple AI agents in parallel, generating evolving iterations of content based on specifications.

## Usage

Read `.claude/settings.json` to see the permissions and commands allowed.

Start Claude Code: `claude`

Type slash command `/project:infinite` to start the infinite agentic loop.

The infinite command takes three arguments:
```
/project:infinite <spec_file> <output_dir> <count>
```

### 4 Command Variants

#### 1. Single Generation
```bash
/project:infinite specs/invent_new_ui_v3.md src 1
```
Generate one new iteration using the UI specification.

#### 2. Small Batch (5 iterations)
```bash
/project:infinite specs/invent_new_ui_v3.md src_new 5
```
Deploy 5 parallel agents to generate 5 unique iterations simultaneously.

#### 3. Large Batch (20 iterations)  
```bash
/project:infinite specs/invent_new_ui_v3.md src_new 20
```
Generate 20 iterations in coordinated batches of 5 agents for optimal resource management.

#### 4. Infinite Mode
```bash
/project:infinite specs/invent_new_ui_v3.md infinite_src_new/ infinite
```
Continuous generation in waves until context limits are reached, with progressive sophistication.

## How It Works

1. **Specification Analysis**: Reads and understands the spec file requirements
2. **Directory Reconnaissance**: Analyzes existing iterations to determine starting point
3. **Parallel Coordination**: Deploys Sub Agents with unique creative directions
4. **Quality Assurance**: Ensures each iteration is unique and spec-compliant
5. **Wave Management**: For infinite mode, manages successive waves of agents

## Directions you can take to enhance this pattern

- Apply this to a use case of your choice.
- Build an MCP Server that enables reuse of the infinite agentic loop.
- Get the `.claude/commands/infinite.md` into your `~/.claude/commands/` directory for global use.
- Update `.claude/commands/infinite.md` to generate sets of files instead of a single file.

## Master AI Coding 
Learn to code with AI with foundational [Principles of AI Coding](https://agenticengineer.com/principled-ai-coding?y=infageloop)

Follow the [IndyDevDan youtube channel](https://www.youtube.com/@indydevdan) for more AI coding tips and tricks.

Use the best Agentic Coding tool: [Claude Code](https://docs.anthropic.com/en/docs/claude-code/overview)

## License

MIT License

Copyright (c) 2026 disler

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.