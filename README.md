# Branch Thinking

An MCP server that implements branch-based thought navigation, with support for:
- Multiple branches of thought
- Branch navigation (list, focus, history)
- Cross-references between related thoughts
- Insight generation from key points
- Branch priority tracking

This is based on the `sequential-thinking` tool available here:
https://github.com/modelcontextprotocol/servers/tree/main/src/sequentialthinking

<a href="https://glama.ai/mcp/servers/x9ovk2l35q"><img width="380" height="200" src="https://glama.ai/mcp/servers/x9ovk2l35q/badge" alt="Branch Thinking Server MCP server" /></a>

## Features

- **Branch Management**: Create and navigate between different lines of thought
- **Cross References**: Link related thoughts across branches with typed relationships
- **Insights**: Automatically generate insights from key points in thoughts
- **Priority Tracking**: Track branch priorities based on confidence and connections

## Commands

- `list`: Show all branches with their current status
- `focus [branchId]`: Switch focus to a specific branch
- `history [branchId?]`: Show the history of thoughts in a branch

## Installation
Place this project in your custom MCP tool directory.

```bash
npm install
npm run build 
```

Add to your `claude_desktop_config.json`:
```json
"branch-thinking": {
  "command": "node",
  "args": [
    "/your-custom-mcp-dir-here/branch-thinking/dist/index.js"
  ]
}
```

## Tips
Claude often will not use tools unless explicitly prompted to do so.

If you want to use this tool without being prompted, add to either your Claude Profile Settings (or a system prompt) something like so:


_If I ask you to "think step by step," "think before you respond," or "use chain of thought," that means use the branch-thinking tool. Don't hesitate to use the branch-thinking tool on your own if you think your response would benefit from multiple steps._

## Credits
I can't pretend that I wrote most of this code. Most of it was generated by Claude. The concept was my own, and so were testing, fixes, and implementation. 
