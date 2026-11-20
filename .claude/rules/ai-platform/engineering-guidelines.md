# Engineering guidelines

## Communication
- State what you are about to do before doing it when the change is non-trivial.
- Report outcomes faithfully: if a test fails or a step was skipped, say so with the evidence.
- When a requirement is ambiguous and the choice matters, ask instead of guessing.

## Changes
- Keep changes small and focused on the request; do not refactor unrelated code.
- Follow the existing conventions of the codebase before introducing new ones.
- Do not add dependencies without a stated reason.
- Do not leave dead code, debug output or commented-out blocks.

## Tests
- Add or update tests for every behaviour change, including at least one failure path.
- Run the relevant tests and linters before declaring work done.
- Never weaken or delete a test to make it pass.

## Secrets and data
- Never write secrets, tokens, credentials or personal data into code, configuration, commits, logs or reports.
- Use the project's secret management mechanism; if none exists, ask.

## Destructive or outward-facing actions
- Ask for explicit confirmation before deleting data or files, rewriting history, force-pushing, running migrations on shared environments, or publishing anything.
- Prefer reversible operations and dry runs.

## Scope of these guidelines
These guidelines steer assistant behaviour; they are not a security control. Real permissions must be enforced by the assistant's settings, the operating system, sandboxes, containers and CI runners.
