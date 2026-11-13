# QuestionPunk for Claude

Connect Claude to [QuestionPunk](https://www.questionpunk.com) to create, edit and publish surveys and AI interviews, and read responses and reports, from a chat.

QuestionPunk is a survey and research platform with a built-in AI interviewer. Respondents answer by text or voice, and the AI asks follow-up questions on open answers, in 130+ languages for text and 25 for voice. The free plan includes unlimited surveys and responses and 3,000 AI credits a month.

## What Claude can do with it

- Draft a survey from a research goal, or start from a template
- Add and edit questions, including 0 to 10 NPS scales, and set display logic
- Set up an AI interview, by text or voice, from a goal or a discussion guide
- Make a potluck sign-up, RSVP, sign-up sheet or find-a-time poll from a template
- Make a scored quiz, or a "how well do you know me" quiz for friends
- Bring in an existing questionnaire, or a Google Forms, Typeform, Microsoft Forms, SurveyMonkey or Qualtrics link, with its wording kept
- Publish when you approve, and get the link to send to respondents
- Read responses, reports and cross-tabs for studies your account can access

## Connect

The server is hosted. Sign in with your own QuestionPunk account; no API key goes in your configuration.

- Endpoint: `https://app.questionpunk.com/api/v1` (Streamable HTTP, OAuth with dynamic client registration)
- Official MCP Registry name: `io.github.questionpunk/questionpunk` (entry in `server.json`)
- Claude web and Desktop: add a custom connector with the endpoint above, then sign in.
- Claude Code: `claude mcp add --transport http questionpunk https://app.questionpunk.com/api/v1`, then run `/mcp` to sign in.

### Install this plugin in Claude Code

The plugin adds eight skills on top of the connection: create, review, manage and analyze a study; set up an AI interview; group forms (potluck, RSVP, sign-up sheet, find-a-time poll); quizzes; and importing an existing questionnaire:

```text
/plugin marketplace add questionpunk/claude-plugin
/plugin install questionpunk@questionpunk
```

Then use `/mcp` to sign in to your QuestionPunk account. Before you sign in, Claude can still draft a survey and hand you a link that opens it in QuestionPunk with no account: the plugin's second server, `questionpunk-start` (`https://mcp.questionpunk.com/start`), needs no sign-in and only makes that link. Skills are in `skills/`; `.claude-plugin/plugin.json` and `.mcp.json` declare the plugin and the HTTP server. This is plugin package version 1.2.0.

## Links

- Setup guide and troubleshooting: https://mcp.questionpunk.com/docs
- Support: https://www.questionpunk.com/support
- Privacy and terms: https://www.questionpunk.com/legal

## License

Proprietary. See the [QuestionPunk terms](https://www.questionpunk.com/legal).
