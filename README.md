# claude-code-openclaw-skills

A custom OpenClaw skill for running Claude Code (Anthropic) through the local `claude` CLI.

## What It Does

- Runs Claude Code in headless mode for automation and cron usage.
- Provides a wrapper (`scripts/claude_code_run.py`) to avoid non-TTY issues.
- Supports permission mode, allowed tools, and structured output.

## What We Changed from the Original

The upstream project was primarily oriented for Linux workflows. This fork/extension adapts it for Windows-based OpenClaw usage.

Key adaptations:

- Reframed usage for OpenClaw on Windows environments.
- Added Windows/OpenClaw guidance for using Git Bash wrappers where PowerShell behavior differs.
- Updated skill naming and metadata to match the OpenClaw skill structure.
- Cleaned repository references so this project is documented as an OpenClaw-focused extension.

## Quick Start

```bash
claude --version
./scripts/claude_code_run.py -p "Return only the single word OK." --permission-mode plan
```

## Example

```bash
./scripts/claude_code_run.py \
  -p "Run tests and fix failures" \
  --allowedTools "Bash,Read,Edit"
```

## License

This project is released under the MIT License.

## Acknowledgement

Thanks to `win4r/claude-code-clawdbot-skill` and its author for the original foundation. This project is an OpenClaw-focused extension built on top of that work.
