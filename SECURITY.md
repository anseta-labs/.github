# Security policy

This policy covers all repositories in the `anseta-labs` organization unless a repository has its own `SECURITY.md`.

## Reporting a vulnerability

Report security problems privately through GitHub:

1. Open the repository where you found the problem.
2. Go to the **Security** tab.
3. Click **Report a vulnerability**.

That opens a private report that only the maintainers can see. It is the only channel we use for security reports.

Please do not open a public issue, pull request, or discussion for a security bug. Public reports expose the problem to everyone before there is a fix.

A useful report includes:

- What the problem is and why it is a security issue.
- The package and version you tested, or the commit you looked at.
- Steps to reproduce it, or a small code sample.

## What to expect

We are a small team, so these are the commitments we can keep:

- We acknowledge your report within a few business days.
- Within about two weeks we either ship a fix or tell you our timeline for one.
- We credit you in the advisory when the fix goes out, unless you prefer otherwise.

We do not run a bug bounty and cannot offer payment for reports.

## Supported versions

Only the latest published release of each package gets security fixes. We do not backport fixes to older versions.

These packages are on 0.x version numbers. Under semantic versioning, that means breaking changes can land in a minor release, so a security fix may arrive alongside one.

## Scope

In scope:

- The published npm packages `@anseta/mcp` and `@anseta/typescript-sdk`.
- The source code in the repositories of this organization.

Out of scope:

- The hosted Anseta API at anseta.com. That is a separate service and is not covered by this policy.
- Findings that only work if the developer's own machine or accounts are already compromised.
