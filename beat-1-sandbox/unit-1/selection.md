# Unit 1 — Issue Selection

Path: `beat-1-sandbox/unit-1/selection.md`

Record of the issue carried into Unit 2, and of the evaluation runs that produced
`eval-run.txt`. This file is graded at the path above; a copy kept anywhere else in
the repository is not read.

Complete every labelled field below. Each is graded on its own; content placed under the
wrong label is not graded.

---

## Selected issue

**Issue link**

[The individual Path Review issue page. A link to the repository or the issue list
does not satisfy this field.]

https://github.com/codepath/pathreview-ai301-fa26-s1/issues/1

**Verdict output**

[Your skill's live-mode output for this issue, pasted verbatim and ending with the
fenced JSON verdict block. A summary does not satisfy this field.]

**The verdict must record `accept` for this issue.** Choose an issue your own skill
accepts. If your skill rejects every candidate you try, that is a signal about your
rubric rather than about the issues: revise it and re-run — retries are unlimited and a
partial re-run costs about $0.20 — or run the skill on different candidates. Output
recording `reject` for the issue you chose earns no credit for this field.

```
All three are in scope (codepath/pathreview-ai301-fa26-s1). Evidence gathered live from the GitHub API on 2026-09-20.

Shared repo facts: not archived; last push 2026-09-16 (4 days ago); all 5 most recent main commits authored by a human, Aburke225 (Collaborator); repo is 410 KB Python; docs/CONTRIBUTING.md and the PR template state CI/test/xfail requirements but say nothing restricting AI assistance; the repo has zero pull requests of any state.

Ranked read-out — all three accepted

1. #1 — Duplicate embeddings on re-ingest (best fit): a Python bug with the root cause already named (_check_skip() passes the string "IngestedSource" to db_session.query() instead of the model class), and the fix requires reading across ingestion/pipeline.py and core/models/ingested_source.py — exactly the multi-file-codebase analysis you want practice at, at a bounded 4–6 hour size.
2. #4 — Parse GitHub Actions workflows for CI/CD skills: also multi-file Python (new ingestion/parsers/workflow_parser.py plus skill_extractor.py) and leans on your Docker/CI familiarity, but it is the largest and least prescribed of the three (6–10 hours, tier-3, skill list given only by example).
3. #6 — Hybrid retriever keyword indexing / BM25 normalization: crisply specified and Python, but confined to one file (rag/retriever/hybrid.py) and the most domain-specific (BM25 scoring), so it exercises the multi-file skill you named least.

Per-check: active maintainer passes for all three on condition (a). within scope passes for all three — #1 and #6 are bug reports with stated root causes, #4 is a feature whose approach, new file, and integration point are already named with no TBDs or debate in the thread. not already claimed passes for all three — no assignees, no linked PRs, no comments at all. contribution policy (preferred) passes for all three by silence.
```

---

## Eval iterations

Quote source text directly in each field below. Paraphrase does not satisfy them.

**Run history**

[The agreement score of each run you did, in order. A single run is a complete answer if
only one run occurred. **The last score in your list must match the agreement line in the
`eval-run.txt` you committed** — that file is the record of your final run.]

**Issue analysis**

[One scored issue, identified by id (`issue-01` through `issue-20`; the `calib-`
issues are not scored). State your rubric's decision, the gold label, and the
reasoning that produced your rubric's result.]

**Check rationale**

[One check from the `rubric.md` uploaded to `tools/issue-select/`, quoted as it is
currently written, with the reasoning behind its current form.]

**Trade-offs**

[What the quoted check gives up. Any one of these is a complete answer: an issue whose
result it changes, a canary you re-ran with `--only`, a case you accept it will miss, or a
stated reason nothing changed elsewhere. "Nothing changed, and here is how I know" earns
the point in full when the reason follows.]

---

## Selection rationale

Graded on whether all three are answered, in your own words. Not on how good the
reasoning is, and not on length — a short honest answer to each earns the full marks.
This is also the basis for the claim comment you write in Unit 2.

**Selection rationale**

[Answer all three:

1. The issue's fit to your interests and to the time available.
2. What the verdict identified correctly, and what you weighed that the rubric could
   not.
3. The anticipated difficulty in claiming it.]

---

Related paths: `eval-run.txt` in this directory; your skill's files in
`tools/issue-select/`.
