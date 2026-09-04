# Global Instructions

These instructions apply to all sessions unless project-specific instructions override them.

## Communication

- Be concise and direct.
- Prefer actionable answers over long explanations.
- Ask clarifying questions only when needed to avoid wrong work.
- Clearly list changed files when making edits.
- If intending to downgrade any dependencies, explain why and ask for confirmation first.

## Coding Workflow

- Read relevant existing files before editing.
- Make small, targeted changes.
- Preserve existing project style, naming, and conventions.
- Prefer simple, maintainable solutions over clever ones.
- Run relevant checks or tests after code changes when practical.

## File Size and Refactoring

- Keep source files under 500 lines unless there is a clear reason not to.
- If a file grows near or beyond 500 lines, consider refactoring reusable logic into separate files.
- Extract cohesive helpers, components, types, or modules when doing so improves readability or reuse.
- Do not split files mechanically; avoid refactors that make the code harder to follow.
- Generated files, lockfiles, vendored code, snapshots, and large data/config files may exceed 500 lines when appropriate.

## JSX File Hygiene

- Do not add utility/helper functions in `.tsx` files that render JSX.
- JSX files should only contain:
    - imports
    - types/interfaces for props
    - the component(s) themselves
    - minimal constants directly tied to rendering
- Any non-trivial logic must be extracted to separate function files or shared util files based on context.
- If new helper logic is needed while editing a JSX file, create/update a separate module and import it.
- Treat this as mandatory, not preference.

## Safety

- Do not run destructive commands unless explicitly approved.
- Do not expose secrets, tokens, credentials, or private keys.
- Prefer non-destructive inspection commands before making changes.
- After each change, if there is a script called `check-style` it should be run to ensure code style is correct.

## Tool Use

- Use file-reading tools to inspect files instead of shelling out to `cat`.
- Use fast search tools like `rg`/`find` when locating code.
- Prefer precise edits over full rewrites unless a rewrite is simpler and safer.
