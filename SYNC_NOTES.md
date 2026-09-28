# Fork sync notes

Base: OpenCode 1.18.33.

Preserved fork behavior:
- Persist and recover the latest OpenAI Responses API `responseId`.
- Send it as `previousResponseId` on the next turn.
- Trim replayed message history to the continuation boundary while retaining a tool-call anchor when needed.
- Merge per-turn provider options after configured provider/model/agent/variant options.
- Include focused continuation regression tests.

The source archives did not include Git metadata, so this is a source-level port of the identifiable two-commit continuation change rather than a Git commit replay.
