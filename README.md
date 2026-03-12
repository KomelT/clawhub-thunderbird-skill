# Thunderbird Skill for OpenClaw

Search and inspect local Mozilla Thunderbird mail storage directly from disk (mbox and Maildir), with filters for account, folder, sender, recipient, subject, body, unread state, and time ranges.

## ClawHub

- https://clawhub.ai/KomelT/clawhub-thunderbird-skill

## What this skill does

- Lists Thunderbird profiles
- Lists accounts inside a selected profile
- Searches local messages in `Mail/` and `ImapMail/`
- Supports filters like `--account`, `--folder`, `--query`, `--from`, `--to`, `--subject`, `--unread-only`, `--since`, `--until`
- Returns human-readable output or JSON

## Quick start

Run from the skill directory:

```powershell
python scripts/search_thunderbird.py --list-profiles
python scripts/search_thunderbird.py --profile default-release --list-accounts
python scripts/search_thunderbird.py --profile default-release --account user@example.com --folder inbox --query invoice --limit 20
```

## Main files

- `SKILL.md` - skill instructions for Codex/OpenClaw
- `scripts/search_thunderbird.py` - Thunderbird search tool
- `references/storage-layout.md` - Thunderbird on-disk layout notes
