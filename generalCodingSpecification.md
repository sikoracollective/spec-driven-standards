# General Coding Specification

## Scope
- Implement only what was asked. Do not invent features or change unrelated code.
- Ask for clarification when requirements are unclear.
- Do not break public APIs or existing behavior unless requested.
- When guidance in this document conflicts, follow Scope unless the user asks otherwise.

## Simplicity
- Prefer clear, straightforward code over clever or over-engineered solutions.
- Avoid duplicate or copy-and-pasted code whenever possible.
- Create reusable methods when it makes sense.
- Remove unused code and large commented-out blocks introduced by your changes.

## Patterns
- Use design patterns when they make future features easier to add.
- Prefer the project's existing libraries, structure, and idioms over inventing new ones.
- Reuse established patterns in the codebase before introducing alternatives.

## Classes
- Prefer one class per file.
- Multiple classes in one file are allowed only when they clearly belong together and splitting them would hurt clarity.

## Naming and Style
- Follow the naming and style conventions for the language and project.
- Match the existing style in the codebase when modifying or extending it.

## Tooling
- Respect the project's linters, formatters, and type checkers.
- Do not introduce new violations.

## Dependencies
- Justify any new dependency before adding it.
- Prefer the standard library or libraries already in use when they meet the need.
- Prefer the latest version of any third-party code.

## Security
- Keep security in mind while writing code. Fix issues as you find them.
- If a security review is requested, list all issues and their severity.
- Research third-party libraries for known vulnerabilities.
- If vulnerabilities are found, tell the user about them and their severity.
- Never hardcode credentials, API keys, tokens, or other secrets in source code.
- Use environment variables or a secrets manager for sensitive values.
- Never commit secrets to version control.
- Validate and sanitize all external input, including APIs, forms, and CLI arguments.
- Reject or safely handle invalid input rather than trusting it.

## Hardening
- Hardening means reducing attack surface and strengthening defenses beyond basic correctness.
- If a hardening review is requested, list all issues and their severity.

## Error Handling
- Prefer explicit error handling over silent failures.
- Do not swallow exceptions without handling or logging them.
- Surface useful error messages that help diagnose the problem without exposing sensitive details.

## Resource Management
- Close files, connections, and other resources reliably using the language's preferred approach, such as try/finally or defer.

## Concurrency
- When writing concurrent code, avoid race conditions and unsafe shared state.

## Performance
- Avoid obvious inefficiencies when writing or changing code.
- Do not over-optimize without a clear reason or measured need.

## Logging
- Add logging where it makes sense.
- Follow the best practices for the language when writing log statements.
- Use the standard logging tools for the language.
- Do not log personally identifiable information.
- Log levels
    - Use the correct logging level when the logging tool supports it.
    - If the logging tool has no log levels, prefix messages with one of the following, followed by a space: FATAL, ERROR, WARN, INFO, or DEBUG.
    - Capitalize log level words.

## Documentation
- Add comments while generating the code.
- Format comments according to the best practices for the language.
