# Chess MCP Server

A Model Context Protocol (MCP) server that enables AI assistants to play and analyze chess games.

## Overview

This MCP server provides chess functionality through the Model Context Protocol, allowing AI assistants like Claude to:
- Play chess games with proper move validation
- Analyze positions and suggest moves
- Track game state and history
- Support standard chess notation

## Installation

### Prerequisites

- Python 3.8 or higher
- `uvx` package runner

### Setup

Add the following configuration to your MCP settings file (typically `claude_desktop_config.json`):

```json
{
  "mcpServers": {
    "chess": {
      "command": "uvx",
      "args": [
        "--from",
        "git+https://github.com/chatkausik/Chess-mcp-server-build.git",
        "chess"
      ]
    }
  }
}
```

### Configuration File Location

- **macOS**: `~/Library/Application Support/Claude/claude_desktop_config.json`
- **Windows**: `%APPDATA%\Claude\claude_desktop_config.json`
- **Linux**: `~/.config/Claude/claude_desktop_config.json`

## Usage

Once configured, the chess server will be available to Claude through the MCP protocol. You can:

1. **Start a new game**: Ask Claude to begin a chess game
2. **Make moves**: Use standard algebraic notation (e.g., "e4", "Nf3", "O-O")
3. **Analyze positions**: Request analysis of the current board state
4. **Review game history**: View previous moves and positions

## Features

- ♟️ Full chess rule implementation
- ✅ Move validation and legal move generation
- 📊 Position evaluation and analysis
- 📝 Game history tracking
- 🎯 Support for standard chess notation
- 🔄 Game state persistence during session

## Example Interactions

```
User: Let's play chess. I'll be white.
Claude: I'll start a new game. Make your first move!

User: e4
Claude: Good opening! I'll respond with e5.

User: Analyze the position
Claude: [Provides analysis of current board state]
```

## Development

### Repository

Source code: [https://github.com/chatkausik/Chess-mcp-server-build](https://github.com/chatkausik/Chess-mcp-server-build)

### Contributing

Contributions are welcome! Please feel free to submit issues or pull requests to the GitHub repository.

## Technical Details

This server uses:
- **MCP Protocol**: Model Context Protocol for AI integration
- **Python Chess Library**: For game logic and validation
- **uvx**: For package execution and management

## Troubleshooting

If you encounter issues:

1. Ensure `uvx` is installed and accessible in your PATH
2. Verify the configuration file is in the correct location
3. Restart Claude after making configuration changes
4. Check that you have an active internet connection for initial installation

## License

Please refer to the [repository](https://github.com/chatkausik/Chess-mcp-server-build) for license information.

## Support

For bugs, feature requests, or questions, please open an issue on the [GitHub repository](https://github.com/chatkausik/Chess-mcp-server-build/issues).

---

Made with ♟️ by the chess MCP community