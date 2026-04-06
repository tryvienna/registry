# Vienna Official Registry

Shareable content for [Vienna](https://github.com/tryvienna) — plugins, quick actions, skills, and more.

## Structure

```
registry.json                  # Registry metadata
plugins/
  _index.json                  # Plugin definitions (all external GitHub refs)
  _defaults.json               # Default enabled plugin IDs
quick-actions/
  _index.json                  # Quick action definitions (array)
  _defaults.json               # Default enabled quick action IDs
skills/
  _index.json                  # Skill definitions (inline + external)
  _defaults.json               # Default enabled skill IDs
  commit/SKILL.md              # Inline skill content
  plugin-dev/SKILL.md
  review-pr/SKILL.md
```

## Plugins

All plugins are hosted in their own repositories and referenced externally:

| Plugin | Repository |
|--------|-----------|
| Weather | [tryvienna/weather-plugin](https://github.com/tryvienna/weather-plugin) |
| GitHub | [tryvienna/github-plugin](https://github.com/tryvienna/github-plugin) |
| Asana | [tryvienna/asana-plugin](https://github.com/tryvienna/asana-plugin) |
| Linear | [tryvienna/linear-plugin](https://github.com/tryvienna/linear-plugin) |
| Google Workspace | [tryvienna/google-workspace-plugin](https://github.com/tryvienna/google-workspace-plugin) |
| Quick Actions | [tryvienna/quick-actions-plugin](https://github.com/tryvienna/quick-actions-plugin) |
| Mixpanel | [tryvienna/mixpanel-plugin](https://github.com/tryvienna/mixpanel-plugin) |
| Vienna Onboarding | [tryvienna/vienna-onboarding-plugin](https://github.com/tryvienna/vienna-onboarding-plugin) |
| Claude Status | [tryvienna/claude-status-plugin](https://github.com/tryvienna/claude-status-plugin) |

## Quick Actions

Quick actions are pre-built prompts that appear in the Vienna workstream composer. Each action has multiple options users can choose from.

### Schema

Each entry in `quick-actions/_index.json`:

```json
{
  "id": "unique-id",
  "label": "Display label",
  "icon": "emoji",
  "description": "Short description",
  "author": { "name": "Author Name" },
  "tags": ["tag1", "tag2"],
  "options": [
    {
      "id": "option-id",
      "label": "Option display text",
      "prompt": "The actual prompt sent to the agent"
    }
  ]
}
```

## Adding this registry

This is the default official registry — it's automatically added when you first use Vienna. To manually add it:

**URL:** `https://github.com/tryvienna/registry.git`
