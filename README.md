# Weather MCP Server

This project is a Model Context Protocol (MCP) server that provides weather information.

## Features

- Get current weather forecast for a specific latitude and longitude.
- Get active weather alerts for a US state.

## Setup

1. **Install dependencies:**
   ```bash
   pnpm install
   ```

2. **Build the server:**
   ```bash
   pnpm run build
   ```

## Running the Server

This server is designed to be run by an MCP client, such as Claude for Desktop.

To configure Claude for Desktop (or a similar MCP client) to use this server, you'll need to point it to the built server. The typical configuration would involve specifying:
- **Command**: `node`
- **Arguments**: `["/ABSOLUTE/PATH/TO/YOUR/PROJECT/mcptest/build/index.js"]`

Replace `/ABSOLUTE/PATH/TO/YOUR/PROJECT/` with the actual absolute path to the `mcptest` directory on your system.

For example, if your project is in `/Users/bohe/Desktop/mcptest`, the argument would be `["/Users/bohe/Desktop/mcptest/build/index.js"]`.

Refer to your MCP client's documentation for specific instructions on how to add and configure an MCP server.

## Development

- Source code is in the `src` directory.
- The main server logic is in `src/index.ts`.
- Build output is in the `build` directory.

## MCP Configuration

The `.vscode/mcp.json` file is provided for VS Code to recognize and potentially debug this MCP server.
