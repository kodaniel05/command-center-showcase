# Engineering Decisions

## Documentation-Only Public Repository

The public repository is intentionally not a runnable clone. It exists to communicate product quality, architecture, feature scope, and engineering judgment without publishing private implementation details.

This protects:

- Private source code.
- Local paths and personal workspace structure.
- Secrets and environment variables.
- Proprietary implementation logic.
- Any client or personal data that could appear in a real local dashboard.

## Local-First Architecture

Command Center is optimized for one trusted developer machine. This keeps the product focused on the actual workflow: launching local projects, opening local URLs, capturing local screenshots, and tracking local runtime state.

A hosted version would require a different threat model and stronger access controls.

## Next.js and TypeScript

Next.js provides a single framework for dashboard UI and server-side route handlers. TypeScript adds stronger contracts around project records, runtime state, and user actions.

This stack is appropriate because the product blends frontend interface work with local backend coordination.

## Schema Validation

Structured validation is used for project records and inputs so the system can reject malformed data early. This matters because local automation can fail in confusing ways if paths, commands, ports, or metadata are invalid.

## Separate Runtime State from Project Metadata

Project metadata is durable. Runtime state is temporary.

Keeping those concepts separate makes the system easier to reason about. A project's name, command, and port can persist, while process IDs, launch logs, and health-check timestamps can change constantly.

## Activity Logging

Activity events make the tool easier to debug and use. Instead of wondering whether a project started, failed, opened, or captured a screenshot, the user can review a timeline of important events.

## Screenshot Metadata

Screenshots are treated as first-class product metadata. A good preview helps identify a project faster than a name alone, especially when managing several visual apps.

The public showcase uses placeholder screenshot references so real screenshots can be curated and redacted before publishing.

## Blueprint Studio as Planning Automation

Blueprint Studio was added because a project command center is not only about current apps. It also supports the next build. Structured planning reduces blank-page friction and helps standardize early technical thinking.

## Privacy and IP Boundaries

The showcase is designed around a clear boundary: explain what was built and why, but do not provide the complete working implementation.

Public artifacts should be safe to share with recruiters, while the private repository remains the source of truth for code.

## Tradeoffs

- Local-first design is fast and practical, but not suitable for public hosting without additional security work.
- Documentation-only publishing protects private code, but reviewers cannot run the app from this repository.
- Structured local persistence is simple, but a remote or multi-device version would need a stronger database and auth layer.
- Screenshot placeholders keep the repository safe by default, but polished screenshots still need to be added manually.
