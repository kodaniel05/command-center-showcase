# Future Improvements

## Product Experience

- Add project groups for workstreams such as portfolio, experiments, dashboards, and client-safe demos.
- Add saved dashboard views and filters.
- Add keyboard shortcuts for common project actions.
- Improve empty states for first-time setup.
- Add a screenshot review workflow that highlights possible sensitive content before export.

## Runtime and Observability

- Add richer launch diagnostics for missing dependencies, invalid package managers, and framework-specific failures.
- Add log search, filters, severity labels, and export.
- Add health-check profiles for static sites, APIs, dashboards, and scripts.
- Add dependency freshness and security summaries.
- Add project uptime and launch success metrics.

## Blueprint Studio

- Add export to Markdown, PDF, or project brief format.
- Add saved blueprint search.
- Add comparison between multiple architecture options.
- Add risk, effort, and milestone estimates.
- Add optional LLM-assisted refinement with explicit user review before saving.

## Portfolio Workflow

- Add a showcase generator that creates safe public docs from selected project metadata.
- Add screenshot sets for README, case study, and recruiter review.
- Add release-note drafting for public project updates.
- Add "privacy checklist" gates before publishing any public artifact.

## Security and Privacy

- Add automatic redaction suggestions for local paths, names, URLs, tokens, and private data.
- Add stricter secret scanning before exporting docs or screenshots.
- Add configurable allowlists for fields that may appear in public artifacts.
- Add a remote mode only after authentication, authorization, audit logging, and process-execution controls are designed.

## Deployment

- Keep local mode as the primary workflow.
- Explore optional single-user authenticated deployment for trusted devices.
- Consider database-backed persistence only if multi-device sync becomes important.
- Add backup and restore for project registry data.
