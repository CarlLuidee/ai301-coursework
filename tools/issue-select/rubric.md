# Rubric: is this a good first issue?

<!--
THIS IS THE PART YOU WRITE. The skill in SKILL.md executes whatever checks
you define here. It ships empty on purpose: the judgment is your work.

A filled rubric must contain:

1. At least one row in the checks table. Each row needs all four columns:
   - Check: a short name (used in the output JSON).
   - Evidence: exactly what to look at, and where. Name the source
     (repo-facts block, issue body, comment thread, or the locations in
     references/evidence-guide.md). "The repo" is not a source; "the last
     5 default-branch commit dates" is.
   - Pass condition: a condition someone else could apply and get your
     answer. Prefer thresholds with numbers ("a maintainer commented
     within 30 days") over adjectives ("maintainer is responsive").
   - Weight: `required` (a fail here rejects the issue) or `preferred`
     (never changes the verdict; a nice-to-have that helps rank the
     issues you accept).

2. A verdict rule below the table: how the check grades combine into
   accept or reject, including how `unclear` is treated. The verdict
   space is binary. If you write no rule for `unclear`, the skill treats
   it as fail.

Cover what actually kills first contributions. The lecture named four
families: the maintainer is alive, the repo is in use, the scope fits a
newcomer, and nobody else is already on it. A rubric that ignores a family
will fail eval issues designed around that family.
-->

## Checks

| Check | Evidence | Pass condition | Weight |
|---|---|---|---|
| active maintainer | last push date + last 5 default-branch commits (author), and maintainer first-response sample | Pass if EITHER: (a) the repo is not archived and at least one of the last 5 default-branch commits was authored by a human (non-bot) within 30 days of capture, OR (b) after excluding first-response-sample entries for issues opened less than 3 days before capture, more than half of the remaining entries show a maintainer response within 30 days | required |
| within scope | issue title, body, and comment history | issue describes a concrete, well-defined task with clear acceptance criteria or proposed changes, such as  bug fix, docs update, or a feature request whose design is already settled. Exclude issues with unresolved design questions, explicitly undecided details (e.g. "TBD"), or a history of repeated abandoned claims or closed-without-merging PRs signaling the approach is unsettled | required |
| not already claimed | "this issue: assignees / linked PRs" line, and Comments section | no current assignee, no open linked PR, and no comment within roughly the last 90 days where someone states they're actively working on it. A stale claim (e.g. followed by an unassignment bot, or no follow-up since) doesn't count against this | required |
| contribution policy | contribution policy | policy allows the use of AI assistance; if no policy is stated, assume AI assistance is allowed | preferred |

## Verdict rule

<!-- State how the grades above combine into accept or reject, and how
unclear is treated. Example shape (write your own): "accept if every
required check passes; preferred checks never change the verdict, they
rank accepted issues; unclear counts as fail." -->

Accept the issue if all required checks pass. Preferred checks don't change the verdict but rank accepted issues. If evidence for a required check is missing or ambiguous, default to pass unless there's a specific negative signal, such as an explicit "not accepting PRs" note, an assigned user, or a maintainer comment claiming it. Absence of proof is not proof of failure.