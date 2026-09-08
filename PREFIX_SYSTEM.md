
## Prefix Command System

This build includes a per-server prefix system.

- `/setprefix prefix:<prefix>` is **Administrator only**.
- Default prefix is `?` (or the `prefix` value in `config.json` if set).
- Example: `/setprefix prefix:question` makes `question ban`, `question kick`, `question serverinfo`, etc. work.
- Example: `/setprefix prefix:+` makes `+ban`, `+kick`, `+serverinfo`, etc. work.
- The prefix is stored per server in `src/data/prefixes.json`.
- A literal `/` also always works as a text prefix (e.g. `/ban`), unless a server's configured prefix is itself `/`.
- Prefix commands reuse the existing command files, so existing command permission checks are retained.
- Mentions such as `@User`, `@Role`, and `#channel` are supported for common option types.
- Uploaded attachments are supported for Attachment options.
- Quoted text is supported, e.g. `?say "hello world"`.
- Slash commands continue to work normally.
- `/setprefix` itself remains a slash command so an administrator can always change the prefix.
