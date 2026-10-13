# .github

Default issue and pull request templates for the repositories of this account.

GitHub shows these templates in every repository of this account that has none of
its own. A repository's own `.github/ISSUE_TEMPLATE` folder hides all default issue
templates, and its own pull request template replaces the default one.

## Files

- `.github/pull_request_template.md`
- `.github/ISSUE_TEMPLATE/bug_report.yml`
- `.github/ISSUE_TEMPLATE/feature_request.yml`
- `.github/ISSUE_TEMPLATE/config.yml`

The set is project-neutral. No file names a project, a component list, a repository
command, or a project board. Each repository's `AGENTS.md` or README names its own
commands.

## Copies

This repository is the single source. Agents cannot see account defaults in a local
checkout, so active repositories carry byte-identical copies of the four files. Tools
that hand the set out to other repositories copy it from here too.

To change the set:

1. Change it here, in one pull request.
2. After it merges, copy the four files unchanged into each repository that carries
   them, one pull request per repository.
3. Compare the hashes with this repository:

   ```sh
   sha256sum .github/pull_request_template.md .github/ISSUE_TEMPLATE/*.yml
   ```

A repository that needs different content keeps the shared files unchanged and puts
the difference in its own `AGENTS.md` or README.
