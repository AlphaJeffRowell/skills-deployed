# Skills Deployment Repository

**Purpose:** Ready-to-deploy skills for Claude Code. Share with coworkers.

## Quick Start

### Option 1: Symlink (Recommended — Auto-Updates)

```bash
# Windows CMD
mklink /D "%USERPROFILE%\.claude\skills" "C:\Repo\skills-deployed"

# OR Bash
ln -s "C:/Repo/skills-deployed" ~/.claude/skills
```

Then in Claude Code:
```
/allvue-object-resolver
/asana-task-update
```

### Option 2: Copy (Snapshot)

```bash
cp -r C:\Repo\skills-deployed\*.md ~/.claude\skills\
```

## What's Included

**13 Production-Ready Skills:**

- **Allvue Foundation** (Tier 1): Object Resolver, Reference Tracer, DataSource Decoder
- **Allvue Transform** (Tier 1.5): XPath Navigator, XSLT Transformer
- **Allvue Domain** (Tier 2): Workflow Designer, Compliance Architect, Report Generator
- **Allvue Integration** (Tier 3): Configuration Cloner, SOW Scope Generator
- **Asana**: Project Manager, Task Update

**See DEPLOYMENT-INDEX.md for full list and commands.**

## File Structure

```
skills-deployed/
├── allvue-*.md           (11 condensed skill files)
├── asana-*.md            (2 condensed skill files)
├── DEPLOYMENT-INDEX.md   (Master reference)
└── README.md             (This file)
```

## How to Use

1. **Deploy to Claude Code** (see Quick Start above)
2. **Open Claude Code** (desktop or web app)
3. **Type slash command**: `/allvue-object-resolver` or `/asana-task-update`
4. **Follow prompts** for inputs and outputs

## Updating Skills

Skills are deployed from the development repo.

**For Developers:**
1. Edit skill in: `C:\Repo\skills-development\Allvue-Skills\Tier-X\NN-SKILL\`
2. Run: `bash _build/deploy.sh`
3. This repo updates automatically

**For Users:**
1. Pull latest changes: `git pull`
2. Redeploy to Claude Code: Copy or resync symlink
3. Done!

## Troubleshooting

| Issue | Solution |
|-------|----------|
| **Skills not showing in Claude Code** | Restart Claude Code; verify symlink/copy to `~/.claude/skills/` |
| **Old skill version** | Pull latest: `git pull`; restart Claude Code |
| **Symlink doesn't work** | Use copy method: `cp -r *.md ~/.claude/skills/` |
| **Permission denied** | Run as administrator; or use copy instead of symlink |

## For Sharing with Coworkers

1. **Give them this folder** or a git clone link
2. **They symlink or copy** to their `~/.claude/skills/`
3. **They're done** — skills available in Claude Code

No confusion about structure, no complex setup. Just flat .md files.

## Documentation

- **DEPLOYMENT-INDEX.md** — Complete skill reference
- Each skill's `.md` file — Full documentation and examples
- **Development repo** — Source code (`C:\Repo\skills-development`)

## Version Info

- **Deployed**: 2026-09-23
- **Source**: C:\code\skills-development
- **Status**: Production-ready
- **Git**: Tracked with full history

---

**Questions?** See DEPLOYMENT-INDEX.md or check the development repo README.
