## Other Information

<!-- Add any additional relevant information here. -->
That name follows a common convention: <type>/<short-description>. It isn’t something Git enforces, just a habit most teams share so that branch lists are easy to read and tools can act on the names.

## The pattern
Type prefix: says what kind of change it is. It usually reuses the same words as Conventional Commits (bonus section B1), so the branch, the commit message and the PR all match.
Slash: separates the type from the description. Many tools, including VS Code, display branches grouped into folders by prefix.
Short description in kebab-case: lowercase words joined by hyphens. Say what the change does in 2 to 5 words.

Common prefixes
|Prefix|Use it for|Example|
|feat/|New functionality|feat/health-check-endpoint|
|fix/|Bug fixes|fix/empty-config-crash|
|chore/|Housekeeping that doesn’t change app behavior|chore/repo-governance|
|docs/|Documentation only|docs/local-setup-guide|
|ci/|Pipeline and workflow changes|ci/run-tests-on-pr|
|refactor/|Restructuring code without changing behavior|refactor/split-config-loader|
|test/|Adding or fixing tests|test/config-edge-cases|
|hotfix/|Urgent production fixes (more common in GitFlow teams)|hotfix/login-timeout|
|release/|Release preparation (GitFlow teams)|release/1.4.0|

Common variations
Ticket ID included: feat/PROJ-142-health-check. Jira and similar tools can then link the branch and PR to the ticket automatically.
Owner prefix: nick/feat-health-check. Some teams use this to show who owns the branch.
Your practice branch: for throwaway branches, a prefix like practice/ or spike/ (a quick experiment) signals that the branch won’t be merged.
Rules of thumb
Use only lowercase letters, numbers, hyphens and slashes. Git rejects spaces and characters like ~ ^ : ? * [ \.
Keep names short. A branch should do one thing, so a long name usually means it’s doing too much.
Delete branches after merging. You’ve already set GitHub to do that automatically.

TPM angle: ticket IDs in branch names give traceability from requirement to ticket to branch to PR to deployment, without anyone filling out a spreadsheet. That’s the kind of evidence auditors ask for, like the SAS70/SOC evidence you used to gather by hand. It’s also a quick thing to look for when you join a team: if the names are random, ask how they trace work back to tickets.
