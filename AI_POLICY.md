# AI Usage Policy

AI tools (Claude, Copilot, Cursor, ChatGPT, etc.) are **allowed** in this repository.
Using them without understanding the result is **not**.

## The core rule

> **You are the author of everything you submit.**
> If you cannot explain a line, you may not submit it.

The tool you used doesn't matter. You are fully responsible for correctness, design,
tests, security and licensing of every change you open.

## 1. Disclose AI usage

Every pull request must state how AI was used, in the PR template:

- **None**: written by you.
- **Assisted**: AI helped with autocomplete, small snippets, explanations or review, and you wrote or rewrote the change.
- **Generated**: AI wrote substantial parts of the change, and you reviewed and verified them.

"Assisted" and "Generated" are both fine. **Not disclosing is the violation.**
Keep AI co-author trailers in commits (for example `Co-Authored-By: Claude ...`). Do not strip them.

## 2. Understand before you submit

- Read every line of the diff before you open the PR.
- In the PR description, explain in **your own words**:
  - **Why**: the problem, and the issue it links to.
  - **What**: the approach you chose, and why it fits *this* codebase.
  - **How you tested it**: commands you ran and what you checked.
- Reviewers may ask you to explain any part of the change. If you can't, the PR will be closed.

## 3. Respect the repository

- Follow the existing architecture, conventions and libraries. Don't add new dependencies,
  patterns or reformatting unless the issue asks for them.
- Keep PRs **small and focused**: one issue per PR. PRs over ~400 changed lines (not counting
  generated files or lockfiles) need agreement on an issue first.
- Don't open "drive-by" PRs that rename, reformat or "improve" code nobody asked about.
- Run the tests, linter and build locally before you push. "CI will tell me" is not testing.

## 4. Communicate as yourself

- Write review replies, issue comments and discussions **yourself**. Don't paste reviewer
  questions into an AI and paste back the answer.
- Bug reports and security reports must be **reproduced by you**, with real steps and real output.
  Unverified AI-generated reports will be closed without discussion.

## 5. Security and confidentiality

- Use only AI tools that the organization has approved for this codebase.
- Never paste secrets, credentials, customer data or private code into tools that aren't approved.
- Don't submit code you suspect was copied from a source with an incompatible license.

## 6. Enforcement

| Situation | What happens |
|---|---|
| Template incomplete, or AI disclosure missing | Automated check fails; the PR can't merge |
| Contributor can't explain the change in review | PR closed, with a link to this policy |
| Undisclosed AI use, or a stripped AI trailer | PR closed, and a warning |
| Repeated violations | Contribution rights restricted, at the maintainers' discretion |

Maintainers may close any PR that looks like low-effort AI output, without a line-by-line review.
Reviewer time is the scarcest resource on this project.

---
*Questions about this policy? Open a discussion or contact the maintainers.*
