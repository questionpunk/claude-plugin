# QuestionPunk for Claude

## Install from this repository

In Claude Code, run:

```text
/plugin marketplace add questionpunk/claude-plugin
/plugin install questionpunk@questionpunk
```

Use `/mcp` to sign in to your own QuestionPunk account.

This repository distributes the public QuestionPunk plugin package version 1.1.1. It contains four skills, plugin metadata, and the public OAuth MCP endpoint. No API keys or reviewer credentials are required in configuration.

Documentation: https://mcp.questionpunk.com/docs
Support: https://www.questionpunk.com/support
Privacy and terms: https://www.questionpunk.com/legal

Production connection: `https://app.questionpunk.com/api/v1` (QuestionPunk OAuth protected resource).

Claude web/Desktop users connect through a remote MCP connector using the release endpoint and their own QuestionPunk OAuth account. Use the connector settings available to your plan or administrator. The downloaded skills package does not itself create a web connector registration.

On Claude Code, unpack this package and launch `claude --plugin-dir /absolute/path/to/questionpunk`. Use `/mcp` to authenticate the QuestionPunk connection, then start the research workflow. For ongoing distribution, add the package to your approved plugin source. Skills are under `skills/`; `.claude-plugin/plugin.json` and `.mcp.json` declare the plugin and HTTP server. No Node installation is needed for the hosted server connection.

Cowork and account-synced plugins require their own supported installation flow. Record web, Desktop, Code, and Cowork separately in host QA; a Code plugin load is not evidence of consumer connector approval. The same connected account must be used for every read/write in a workflow.

Sources checked September 19, 2026: [plugin reference](https://code.claude.com/docs/en/plugins-reference), [MCP](https://code.claude.com/docs/en/mcp), [connector surfaces](https://support.claude.com/en/articles/11725091-when-to-use-desktop-and-web-connectors).

## Connection for this build

MCP endpoint: https://app.questionpunk.com/api/v1

QuestionPunk: https://app.questionpunk.com

## License

Proprietary. See the [QuestionPunk terms](https://www.questionpunk.com/legal) for the applicable terms.
