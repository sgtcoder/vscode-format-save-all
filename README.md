# VSCode Format Save All Readme #

> - **Extension ID:** sgtcoder.vscode-format-save-all
> - **Last Revised:** 2023-12-26

# Overview #
> Opens every file that matches the lookup parameters, and applies the formatting action to them and saves.
> File formatting must be set up for all file types that you include.

# Features #
> There are currently 2 features `formatall.doFormat` and `formatall.doSave`.

## formatall.doFormat ##
> Runs the format action on all documents. This does not run the other formatters that get ran when you save.

1. Looks up files based on configuration options (`formatall.search.include` and `formatall.search.exclude`)
2. Opens the retrieved files, and performs the `editor.action.formatDocument` command on each of them.

## formatall.doSave ##
> Runs the save action on all documents. This runs all actions that are set on save (including format if that is enabled on save).

1. Looks up files based on configuration options (`formatall.search.include` and `formatall.search.exclude`)
2. Opens the retrieved files, and performs the `workbench.action.files.save` command on each of them.

# Extension Settings #
> This extension contributes the following settings:

- `formatall.search.include`: A selector to choose the files to include in the formatting
- `formatall.search.exclude`: A selector to choose the files which should not be formatted
- `formatall.quantity`: How many files should be processed per batch

# Keyboard Shortcuts #
> You can define shortcuts to run the actions.

```
{
    "key": "ctrl+alt+f",
    "command": "formatall.doFormat"
},
{
    "key": "ctrl+alt+s",
    "command": "formatall.doSave"
}
```