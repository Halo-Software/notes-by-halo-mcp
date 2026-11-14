# Notes by Halo — MCP Server Bundle (notes-by-halo-mcp)

This is a **distribution-only** repository. It publishes the `.mcpb` bundle of the
MCP server that belongs to the **Notes by Halo** desktop app, so that AI clients
and the official MCP Registry can find and fetch it.

The bundle is a **companion accessory for people who use the Notes by Halo
desktop app**. It is not a standalone notes product: your notes live in the app,
stored as plain Markdown (`.md`) files in a folder you choose. The app's source
code is developed privately and is not in this repository.

- App and downloads: https://notes.gethalo.software
- Setup guide (including manual configuration): https://notes.gethalo.software/mcp.html
- Official MCP Registry name: `io.github.Halo-Software/notes-by-halo-mcp`

## What the MCP server does

The server runs locally on your machine (stdio, no cloud copy of your notes) and
gives AI clients such as Claude Desktop and Cursor eight tools over your own
Markdown notes:

- `list_notes` — list all notes with metadata and task summaries
- `get_note` — read a note's full Markdown, metadata, and tasks
- `create_note` — create a new note
- `update_note` — update a note's body and/or color
- `delete_note` — delete a note
- `search_notes` — full-text search across notes
- `list_tasks` — list task checkboxes across all notes
- `toggle_task` — check or uncheck a task in a note

## Install (Claude Desktop)

1. Download `notes-by-halo-mcp-1.1.0.mcpb` from this repository's
   [Releases](https://github.com/Halo-Software/notes-by-halo-mcp/releases) page.
2. Drag and drop the file into Claude Desktop.
3. Optionally point it at your Notes by Halo storage directory. If you leave it
   blank, your default Notes by Halo storage is detected automatically.
4. Restart Claude Desktop.

## Requirements

- Node.js (the bundle runs the server with `node`)
- The Notes by Halo desktop app is the main product this bundle accompanies;
  installing the app already enables the same MCP server through its About
  screen. This bundle simply makes setup for Claude Desktop easier.

## Contents of this repository

- `README.md` — this file
- `server.json` — metadata for the official MCP Registry
- `NOTICE.md` — rights and licensing stance
- The `.mcpb` bundle itself is attached to each GitHub Release (it is not
  committed to the repository history).

## License

All rights reserved. See [NOTICE.md](NOTICE.md).
