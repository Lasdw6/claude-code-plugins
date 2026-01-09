# Claude Code Plugins Marketplace

A curated collection of Claude Code plugins to enhance your coding workflow.

## Available Plugins

### Claude Notes
**Persistent Design Intent Layer**

Maintains file-level design notes that prevent accidental violations of design intent, assumptions, and intentional shortcuts across LLM sessions.

**Features:**
- 📝 Persistent design notes stored in `.claude/notes/`
- 🔒 Frozen section protection (blocks modifications to critical code)
- ⚠️ Assumption violation warnings
- 🎯 Interactive `/note` command for managing notes
- 📦 Version control friendly (JSON storage)
- 🔄 Note evolution through Claude-proposed updates

**Repository:** [Lasdw6/Claude-notes](https://github.com/Lasdw6/Claude-notes)

## Installation

### Add This Marketplace

```bash
/plugin marketplace add Lasdw6/claude-code-plugins
```

### Install Claude Notes

```bash
/plugin install claude-notes@Lasdw6-claude-code-plugins
```

### Verify Installation

```bash
/note help
```

## Usage Example - Claude Notes

1. **Create a design note:**
   ```bash
   /note create src/components/Button.tsx
   ```

2. **When Claude edits the file:**
   - Hook automatically loads note
   - Injects design intent into context
   - Requires acknowledgment: "I acknowledge the design intent constraints..."
   - Blocks if frozen sections violated

3. **View/manage notes:**
   ```bash
   /note view src/components/Button.tsx
   /note list
   /note migrate old.ts new.ts
   ```

## Contributing

Want to add your plugin to this marketplace?

1. Create your plugin following [Claude Code plugin structure](https://code.claude.com/docs/en/plugins)
2. Open an issue or PR with your plugin details
3. Include:
   - Plugin name and description
   - Repository URL
   - Version number
   - Brief feature list

## About

This marketplace is maintained by the Claude Code community to share useful plugins and extensions.

## License

Individual plugins may have their own licenses. Check each plugin's repository for details.
