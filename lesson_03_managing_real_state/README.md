# Lesson 03 - Manage your realstate

Commands used in this lesson:

| `Keybinding` | `Description`   |
| ------------ | --------------- |
| ⌘ B          | Toggle side bar |

### Toggle both side bar and activity bar

You will need [multi command](https://marketplace.visualstudio.com/items?itemName=ryuta46.multi-command) extension. We already installed this extension in lesson one.

Add the following in `settings.json` inside the `multiCommand.commands` array:

```json
{
  "command": "multiCommand.toogleBars",
  "sequence": [
    "workbench.action.toggleSidebarVisibility",
    "workbench.action.toggleActivityBarVisibility"
  ]
}
```

Add the following in `keybindings.json`

```json
{
  "key": "cmd+b",
  "command": "multiCommand.toogleBars"
}
```

Now you can toggle both bars using `⌘ B`.

### Customize your colums

In `settings.json` you toggle any of the three columns that are shown by default.

Set on/off the display of line numbers:
`"editor.lineNumbers": "off"`

Set on/off the code folding feature:
`"editor.folding": false`

Set on/off the debugger:
`"editor.glyphMargin": false`
