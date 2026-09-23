# Skills Deployment Index

✅ **13 Skills Ready for Deployment** — Deploy to `~/.claude/skills/`

**Last Generated**: 2026-09-23  
**Status**: Production-ready  
**Access**: `/slash-commands` from Claude Code

---

## Deployed Skills (Alphabetical)

| Skill | Command | Purpose | Tier |
|-------|---------|---------|------|
| **Allvue Compliance Architect** | `/allvue-compliance-architect` | Design compliance rule matrices, scenario tests, ratings | Tier 2 |
| **Allvue Configuration Cloner** | `/allvue-configuration-cloner` | Clone object configurations with reference adjustments | Tier 3 |
| **Allvue DataSource Decoder** | `/allvue-datasource-decoder` | Decode DataSource to SQL signature and fields | Tier 1 |
| **Allvue Object Resolver** | `/allvue-object-resolver` | Resolve any object to complete dependency chain | Tier 1 |
| **Allvue Reference Tracer** | `/allvue-reference-tracer` | Trace impact of changes on downstream objects | Tier 1 |
| **Allvue Report Generator** | `/allvue-report-generator` | Generate reports with DataSource binding and distribution | Tier 2 |
| **Allvue SOW Scope Generator** | `/allvue-sow-scope-generator` | Generate SOW with estimates, timelines, costs | Tier 3 |
| **Allvue Workflow Designer** | `/allvue-workflow-designer` | Design trade/order workflows with validation rules | Tier 2 |
| **Allvue XPath Navigator** | `/allvue-xpath-navigator` | Write XPath expressions for workflow validation | Tier 1.5 |
| **Allvue XSLT Transformer** | `/allvue-xslt-transformer` | Create XSLT transformations for data mapping | Tier 1.5 |
| **Asana Project Manager** | `/asana-project-manager` | Create, update, search, and manage tasks and projects | Integration |
| **Asana Task Update** | `/asana-task-update` | Sync meeting notes to Asana with extended actions | Integration |

---

## How to Deploy

### Option 1: Symlink (Auto-Updates)
```bash
mklink /D "%USERPROFILE%\.claude\skills" "C:\code\skills-deployed"
```

### Option 2: Copy (Snapshot)
```bash
cp -r C:\code\skills-deployed\*.md ~/.claude/skills/
```

### Option 3: Share with Coworkers
Send them the `C:\code\skills-deployed` folder, they symlink or copy to their `~/.claude/skills/`

---

## Tier Structure (Development Only)

**Development repo** organizes skills by capability level:

- **Tier 1** - Foundation (Object Resolver, Reference Tracer, DataSource Decoder)
- **Tier 1.5** - Transform (XPath Navigator, XSLT Transformer)
- **Tier 2** - Domain (Workflow Designer, Compliance Architect, Report Generator)
- **Tier 3** - Integration (Configuration Cloner, SOW Scope Generator)

**Deployment repo** is flat — all 13 skills in one directory, ready to use.

---

## Development Workflow

1. **Edit** skill in: `C:\code\skills-development\Allvue-Skills\Tier-X\NN-SKILL\NN-SKILL.md`
2. **Update** entry point: `C:\code\skills-development\Allvue-Skills\Tier-X\NN-SKILL\SKILL.md`
3. **Run deploy script**: `bash _build/deploy.sh`
4. **Test in Claude Code**: `/allvue-object-resolver` (or any skill)
5. **Verify** output in deployment repo: `C:\code\skills-deployed\`

---

## File Locations

| Purpose | Location |
|---------|----------|
| **Dev source (full docs)** | `C:\code\skills-development\Allvue-Skills\Tier-X\NN-SKILL\NN-SKILL.md` |
| **Dev entry point** | `C:\code\skills-development\Allvue-Skills\Tier-X\NN-SKILL\SKILL.md` |
| **Deployed (ready to use)** | `C:\code\skills-deployed\allvue-*.md` |
| **Claude Code runtime** | `~/.claude/skills\*.md` |

---

## Quick Reference

**For Developers (You):**
- Work in: `C:\code\skills-development`
- Structure: Organized by tier
- Run: `bash _build/deploy.sh` after changes

**For Users (Coworkers):**
- Get: `C:\code\skills-deployed`
- Deploy to: `~/.claude/skills/`
- Use: `/skill-name` in Claude Code

---

## Support

**Questions?**
- See development README in each Tier folder
- Check specific skill's SKILL.md for usage examples
- Review full documentation in NN-SKILL.md files

**Adding New Skills:**
1. Create folder: `C:\code\skills-development\Allvue-Skills\Tier-X\NN-SKILL\`
2. Add: `NN-SKILL.md` (full docs)
3. Add: `SKILL.md` (condensed entry)
4. Run: `bash _build/deploy.sh`
5. Test in Claude Code
