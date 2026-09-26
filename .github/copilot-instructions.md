# Repository Copilot Instructions

## Repository Overview

**uttamkumar37** is the GitHub *profile repository* (its `README.md` is displayed on the `github.com/uttamkumar37` profile page). It contains a single file, `README.md`, that introduces Uttam Kumar: role, featured project (CloudCampus), tech-stack icons, GitHub stats widgets and contact links.

## Technology Stack

- Markdown with embedded HTML (`<h1 align="center">`, `<p align="center">`, `<img>`) as rendered by GitHub
- Third-party image services referenced by URL: skillicons.dev, shields.io, github-readme-stats, github-readme-streak-stats, github-readme-activity-graph
- No code, build system, dependencies or CI.

## Repository Structure

```
README.md    the entire profile page: About Me, Tech Stack, Featured Project, GitHub Stats, Languages, Contribution Graph, Connect
```

## Architecture

None. It is a single static document. Sections are ordered: intro, About Me, Tech Stack (skillicons), Featured Project (CloudCampus), stats widgets, connect links.

## Development Commands

None. Preview the Markdown in the editor preview or on GitHub after pushing. Do not add build tooling for a one-file repo.

## Coding Guidelines

- Keep the existing structure and style: centered HTML blocks for header/badges, `---` separators, short bulleted lists.
- Use GitHub-safe HTML only (no scripts, iframes or custom CSS; GitHub strips them).
- Every image needs meaningful alt text where the existing markup allows it; keep widgets readable in both light and dark GitHub themes.
- Keep the tone professional and concise; avoid decorative emoji overload beyond the existing section-heading style.
- Keep links valid; the username used in widget URLs is `uttamkumar37`.

## Testing

None automated. Check the rendered Markdown (preview) for broken images/links. Third-party widgets can be slow or fail; do not treat that as a content error, and do not replace them without being asked.

## Security

Public repository. Never add secrets, tokens, private email addresses or phone numbers beyond what is already published. Widget URLs must not carry access tokens.

## Infrastructure / Deployment

None. GitHub renders the profile README directly from the default branch.

## Change Guidelines

1. Understand the existing content first.
2. Make the smallest coherent change.
3. Preserve the current section structure unless asked to redesign it.
4. Do not add a new third-party widget or service when existing content already covers the need.
5. Preview the rendered Markdown before considering the change complete.
6. Do not leave commented-out blocks.
7. Do not leave TODO placeholders unless explicitly requested.
8. Do not fabricate experience, skills or project status.

## Code Quality Rules

- Prefer readable, well-formed Markdown/HTML over clever markup.
- Avoid duplicate content; keep facts aligned with the `ukglab` and `uttam.dev` portfolio repositories.
- Follow existing formatting conventions (headings, separators, centered blocks).
- Avoid unrelated rewrites during focused edits.

## Git Commit Rules

- Never add a `Co-Authored-By` trailer unless I explicitly request it.
- Never add Claude, Anthropic, GitHub Copilot, OpenAI, ChatGPT, Codex, Cursor, or any AI tool as an author or co-author.
- Use only the configured Git `user.name` and `user.email`.
- Do not mention AI assistance in commit messages.
- Keep commit messages concise and professional.
- Do not commit automatically unless I explicitly ask.
- Do not push automatically unless I explicitly ask.
- Never force-push unless I explicitly request it.
- Never rewrite Git history unless I explicitly request it.

## AI Assistant Working Rules

When working in this repository:

- Inspect existing code before proposing architecture changes.
- Do not assume a feature exists without verifying it.
- Do not create fake implementations to make UI or tests appear complete.
- Do not generate random metrics, scores, or placeholder business data unless explicitly requested as test/demo data.
- Clearly separate verified behavior from assumptions.
- Prefer completing working vertical slices over creating many unfinished placeholders.
- Preserve repository conventions.
- Avoid massive rewrites unless explicitly requested.
- When fixing a bug, identify the underlying cause where practical.
- When adding functionality, consider error handling and tests.
- Never expose secrets, API keys, tokens, or credentials.
- Never hardcode secrets.

## Repository-Specific Rules (profile accuracy)

- This is a public first impression. Statements about years of experience, employers, skills and CloudCampus features must be true and current; CloudCampus is being rebuilt backend-first, so do not list features as shipped unless the maintainer confirms.
- Do not invent statistics, followers, stars or achievements; the stats widgets pull live data and must stay dynamic, not hard-coded numbers.
- Keep the skills icon list limited to technologies the maintainer actually uses.
