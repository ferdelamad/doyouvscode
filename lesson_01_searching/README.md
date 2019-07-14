# Lesson 01 - Searching

Commands used in this lesson:

| `Keybinding` | `Description`               |
| ------------ | --------------------------- |
| ⌘ P          | Go to File                  |
| ⇧ ⌘ F        | Search bar (search by word) |
| ⇧ ⌘ N        | New window/instance         |
| ⌃ R          | Workspace/project search    |
| ⇧ ⌘ X        | Show extensions             |
| ⌘ ,          | User settings               |
| ⌘K ⌘S        | Keyboard shortcuts          |

### Automated search for selection

Install the [multi command](https://marketplace.visualstudio.com/items?itemName=ryuta46.multi-command) extension.

Add the following in `settings.json`

```json
"multiCommand.commands": [
  {
    "command": "multiCommand.findInAllFiles",
    "sequence": [
      "workbench.action.findInFiles",
      "search.action.refreshSearchResults"
    ]
  }
]
```

Add the following in `keybindings.json`

```json
{
  "key": "ctrl+.",
  "command": "multiCommand.findInAllFiles"
}
```

1.- Select the word that you want to search
2.- Use the new keybinding `⌃ + .`
