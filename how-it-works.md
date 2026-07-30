# How CHLOtimizer works

Use this template to document the application architecture and data flow for contributors and advanced users.

## Overview

_Describe the problem CHLOtimizer solves and the main user workflow._

## Main components

| Component | Responsibility | Location |
| --- | --- | --- |
| Renderer | _Displays pages and collects user actions._ | `src/renderer` |
| Main process | _Runs privileged Windows operations and coordinates Electron._ | `src/main` |
| Preload bridge | _Exposes approved IPC operations to the renderer._ | `src/preload` |
| Registry and tweak data | _Defines available tweaks and their metadata._ | `tweaks` |

## User action flow

1. _The user selects a feature in the renderer._
2. _The renderer validates the request and sends an approved IPC message._
3. _The main process performs the operation with the required permissions._
4. _The result is returned to the renderer and shown to the user._

## Safety model

- _Explain administrator prompts and least-privilege decisions._
- _Describe backups, restore points, and how destructive actions are confirmed._
- _Document how downloaded updates and external resources are verified._

## Updates

_Document the public release repository, version comparison, download, and installation flow._

## Extending the application

_Explain where to add a page, IPC handler, tweak, test, or documentation page._
