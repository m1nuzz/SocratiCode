# OpenHands SocratiCode Plugin

## Overview

This plugin integrates SocratiCode with OpenHands, providing codebase intelligence capabilities including semantic search, dependency graph analysis, and symbol-level impact analysis for AI assistants.

## Features

- **Codebase Indexing**: Index your entire codebase for semantic search
- **Dependency Graph Analysis**: Visualize and analyze code dependencies
- **Symbol-Level Impact Analysis**: Determine blast radius of code changes
- **Interactive Graph Explorer**: Browse code relationships visually
- **Context Artifact Exploration**: Search architecture documentation and schemas
- **MCP Server Integration**: Works with any MCP-compatible host

## Installation

1. Install the plugin from the OpenHands plugin marketplace
2. Configure the plugin settings as needed (see Configuration section)
3. Index your workspace using the `SocratiCode: Index current workspace` command

## Configuration

### Settings

Configure these settings in your OpenHands configuration:

```json
{
  "socraticode.command": "npx",
  "socraticode.args": ["-y", "socraticode"],
  "socraticode.env": {},
  "socraticode.statusBar": true
}
```

### Environment Variables

For non-sensitive configuration, use environment variables:

- `QDRANT_MODE`: Set to `external` to use external Qdrant instance
- `QDRANT_URL`: URL for external Qdrant instance
- `EMBEDDING_PROVIDER`: Select embedding provider

For sensitive data like API keys, use OS environment variables or a local `.env` file.

## Usage

### Commands

- `SocratiCode: Index current workspace` - Index the current workspace
- `SocratiCode: Open interactive graph` - Open the interactive graph explorer
- `SocratiCode: Refresh indexed projects` - Refresh the list of indexed projects
- `SocratiCode: Show output / logs` - View plugin logs and output

### AI Assistant Integration

Ask your AI assistant to use SocratiCode tools for:
- Semantic code search
- Dependency analysis
- Impact analysis (blast radius)
- Architecture exploration

## Development

### Requirements

- Node.js >= 18.0.0
- OpenHands compatible host

### Building

```bash
cd extension
npm install
npm run compile
```

### Testing

```bash
npm test
```

## License

AGPL-3.0-only

## Support

- [GitHub Issues](https://github.com/giancarloerra/socraticode/issues)
- [Documentation](https://github.com/giancarloerra/socratiode#readme)
- [Discussions](https://github.com/giancarloerra/socraticode/discussions)