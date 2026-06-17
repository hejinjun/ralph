# Ralph Scripts Directory

This directory contains the core scripts and instructions for the Ralph autonomous coding agent system.

## Files

### `ralph.sh`
The main orchestration script that runs Ralph iterations. It supports both `amp` and `claude` tools for autonomous agent execution.

**Usage:**
```bash
./ralph.sh [--tool amp|claude] [max_iterations]
```

**Examples:**
```bash
# Run with amp tool (default), max 10 iterations
./ralph.sh

# Run with claude tool, max 15 iterations
./ralph.sh --tool claude 15

# Run with specific tool using flag syntax
./ralph.sh --tool=claude 20
```

### `CLAUDE.md`
Instructions for Claude-based autonomous agents. Provides detailed guidance on task execution, quality checks, and progress reporting.

**Key sections:**
- Task workflow and implementation steps
- Progress report formatting
- Pattern consolidation for codebase learnings
- CLAUDE.md file updates for knowledge preservation
- Quality requirements and browser testing

### `prompt.md`
Instructions for Amp-based autonomous agents. Similar to CLAUDE.md but tailored for the Amp tool with thread URL tracking.

**Key features:**
- Ampcode thread integration for progress tracking
- Pattern consolidation for reusable code patterns
- AGENTS.md file updates for knowledge preservation
- Browser testing requirements for frontend stories

## Source

These files were sourced from the original Ralph implementation at:
[github.com/snarktank/ralph](https://github.com/snarktank/ralph)

They serve as the foundational instructions and tooling for running autonomous agent iterations on software projects.

## Integration

The `ralph.sh` script:
1. Reads project requirements from `prd.json`
2. Tracks progress in `progress.txt`
3. Maintains branch-specific archives
4. Executes agent instructions via either `prompt.md` (amp) or `CLAUDE.md` (claude)

For detailed setup and usage, refer to the main README in the repository root.
