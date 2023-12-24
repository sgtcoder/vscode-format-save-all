# sgtcoder.vscode-format-save-all README

## Features

### formatall.doFormat
> 1. Looks up files based on configuration options (`formatall.search.include` and `formatall.search.exclude`)
> 2. Opens the retrieved files, and performs the `editor.action.formatDocument` command on each of them.

### formatall.doSave
> 1. Looks up files based on configuration options (`formatall.search.include` and `formatall.search.exclude`)
> 2. Opens the retrieved files, and performs the `workbench.action.files.save` command on each of them.

## Requirements
> File formatting must be set up for all file types that you include.

## Extension Settings
> This extension contributes the following settings:

> * `formatall.search.include`: A selector to choose the files to include in the formatting
> * `formatall.search.exclude`: A selector to choose the files which should not be formatted
> * `formatall.quantity`: How many files should be processed per batch