# Profile README audit

Reviewed on 17 October 2026. Repository discovery used unauthenticated public GitHub endpoints. No private source, private repository descriptions, or employment systems were accessed.

## Findings before the rewrite

- The original README prioritizes followers, stars, stack icons, and four activity images over inspectable engineering work. Images lack alt text; one project introduces a second H1.
- CloudCampus is described as enterprise-grade with shipped features, without accessible evidence. Local repository guidance says it is being rebuilt backend-first.
- The LinkedIn link goes to the service homepage. No portfolio URL is supplied.
- Experience claims conflict: the profile says 4+ years, while the public GenAI README says six. Neither supplies a professional timeline; omit the count pending confirmation.
- The activity graph returns HTTP 402. Stats and streak images respond, but add little evidence and use a fixed dark theme. Remove all widgets under the requested redesign.

## Public evidence and selection

| Work | Evidence inspected | Editorial decision |
| --- | --- | --- |
| [SpeakBetter](https://github.com/uttamkumar37/SpeakBetter) | README; Gradle and frontend dependencies; controller/service/repository code; storage interface and R2 adapter; cleanup scheduler; integration-test source; Compose configuration | Lead with the app as a personal project in development. Highlight storage boundaries, retention, migrations, and tests. Do not claim a live deployment or working AI transcription. |
| [GenAI-Engineering](https://github.com/uttamkumar37/GenAI-Engineering) | README and tree; async provider client and circuit breaker; gateway example; property-test source; Java/Python architecture exercise | Feature as a learning lab. Link actual examples and the boundary-design exercise. Milestone directories contain placeholders, so omit capstone completion and production claims. |
| [System-Design](https://github.com/uttamkumar37/System-Design/blob/main/system-design-curriculum.md) | Public tree and 24-module curriculum, including messaging, resilience, and observability | Feature as a documented study curriculum, with technologies framed as subjects rather than implemented systems. |
| [Backend-Notes](https://github.com/uttamkumar37/Backend-Notes) | README, tree, Go notes and roadmap, backend-concepts outline | Link under learning. It currently contains introductory Java/Go exercises and roadmaps rather than a substantial backend implementation. |
| CloudCampus | User-provided context and existing local profile guidance only; anonymous GitHub requests return 404 | Keep a brief private-project status note. Include no source link, unverified feature list, architecture details, or deployment claim. |

Cloud-Platform-Engineering and Product-Building currently have title-only READMEs; Personal-Projects has no accessible Git tree. They do not add substantive evidence. The referenced ukglab and uttam.dev repositories return anonymous 404s; they cannot corroborate the profile.

## Outline and content strategy

1. Name, backend/platform positioning, concrete value proposition, and location.
2. Professional Java/Spring Boot experience, using the supplied work history without adding employers, metrics, or tenure.
3. Three public selections with a problem, approach, technology context, and explicit status; a short private CloudCampus note.
4. Direct links to storage design, retention tests, and the Java/Python design exercise, with the relevant tradeoffs explained.
5. Separate production skills, project practice, and current learning.
6. Public technical notes, verified contact destinations, and an invitation to engineering collaboration.

Use native Markdown headings and lists. Omit decorative assets and activity widgets: the profile needs no external image service, fixed colors, custom HTML, or build tooling.

## Contact and verification limits

- GitHub profile and featured public repositories respond anonymously.
- GitHub's public [social accounts endpoint](https://api.github.com/users/uttamkumar37/social_accounts) identifies `https://www.linkedin.com/in/uttamkumar37/`. LinkedIn blocks automated access with HTTP 999; profile contents could not be independently checked.
- The email address is already published in the original local README. Preserve it without claiming mailbox deliverability.
- No public portfolio URL was verified. The prospective SpeakBetter GitHub Pages address returns 404; its deployment instructions are not proof of deployment.
- Professional experience comes from the user's supplied context. The clarification supplied no dates or portfolio URL, so neither an experience count nor a portfolio link was added.
- Project code and test source were inspected, not executed. Test presence is evidence of intent and implementation, not a passing test run or coverage measurement.

## Final verification

- The README has 17 unique link targets: 13 GitHub URLs returned HTTP 200, two local heading anchors resolve, one LinkedIn destination is corroborated as described above, and one published email address passes syntax validation.
- Source inspection confirms the external `architecture-notes` heading and the retention-test line reference. Featured repositories were publicly accessible without authentication.
- A local Markdown preview using GitHub-style CSS was rendered in Chrome at 1280, 375, and 320 CSS pixels in both light and dark themes. All six configurations had no horizontal overflow, exactly one H1, ordered heading levels, and nonempty link labels.
- Screenshots of desktop and mobile layouts were visually reviewed. Text contrast measured 15.80:1 in light mode and 17.39:1 in dark mode; minimum link contrast measured 5.19:1 and 6.11:1 respectively. These measurements describe the local preview, not a published GitHub page.
- The in-app Browser tool could not connect, so preview verification used a temporary local Chrome session. Preview dependencies and artifacts stayed outside the repository. No build tooling was added.
- There are no images, fixed-width elements, custom colors, scripts, placeholders, widgets, or third-party image dependencies in the README. Image dimensions and alt text are therefore inapplicable. Spelling and wording were manually reviewed.
- The skeptical engineering review retained explicit app/lab/curriculum status labels, removed the unverified year count and CloudCampus feature claims, and kept Go and orchestration topics under current learning/focus. It makes no scale, adoption, performance, production deployment, or test-coverage claims.
- Only the README and this directly related audit document changed. Commit and push were deferred until the user explicitly requested them after reviewing the redesign.

## Final self-review

Scores are editorial judgments out of 10, not measured engineering achievements.

| Criterion | Score | Rationale |
| --- | --- | --- |
| Credibility | 9 | Public evidence is linked; professional history remains user-supplied and exact tenure is omitted. |
| Clarity | 9 | The opening identifies the work and separates production experience, project practice, and current focus. |
| Visual quality | 8 | Native hierarchy and restrained layout render consistently; no bespoke imagery or typography. |
| Technical depth | 8 | Concrete storage, lifecycle, resilience, and service-boundary evidence; limited public production evidence. |
| Maintainability | 9 | Plain Markdown and no image services; branch links and project statuses still need periodic review. |
| Accessibility | 9 | Semantic headings, descriptive links, mobile reflow, and adequate preview contrast; no live screen-reader audit. |
