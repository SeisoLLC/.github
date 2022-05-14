# Guidelines for contributing to Seiso software projects

## Expectations

At Seiso, all changes to git repositories are reviewed, regardless of the size or impact.  When you are [contributing](#how-to-contribute) or
[reviewing](#how-to-review) contributions at Seiso, we have three overarching guidelines:

1. PRs blocking other work should be meaningfully reviewed within 2 business days.
1. All other PRs should be reviewed within at least 5 business days.
1. [Be respectful](https://testing.googleblog.com/2019/11/code-health-respectful-reviews-useful.html).

### How to contribute

To submit a change for inclusion, please do the following:

* Review the license for the target repo and ensure your contribution fits within the license terms, often in `LICENSE.md`.
* If there is a GitHub issue already created for your change, ensure it is assigned to yourself and [properly
  link](https://docs.github.com/en/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue) any pull requests.
* If your change could be considered significant, it is a good idea to start a discussion and get consensus on the basic design first.
* When beginning development, ensure you have a fully updated branch.
* If you have work in progress but you'd like to submit it for review, open a pull request but mark it as draft.
  * Pull requests should be small to facilitate easier review. Sometimes this will result in small, incremental improvements to land a single large
    feature.
* If the "how" or "why" of your changes may be unclear during review, preemptively open a comment on that line of code in the PR, explaining your
  reasoning.
* Ensure that all tests are passing, and if your code is introducing a new feature, include test coverage for that feature.
* Code changes must be accompanied by the appropriate documentation updates or additions.

### How to review

Consider the following when reviewing a PR:

* Does PR clearly state how its contribution relates to a particular feature, issue, or bug?
* Does the code do what the PR claims it does?
* Has the code introduced new, unwelcome behavior or dependencies?
* Could the code be written to be more readable?
* Could the code be written to be more modular/reusable without adding unneeded complexity?
* Are tests passing, and is there sufficient test coverage (i.e. do the tests cover the fixed bug or newly introduced feature(s))?

All conversations should be reviewed and resolved, and all checkboxes should be checked or discussed (i.e. noting that you don't consider them a
requirement for approval or that your approval is conditional on outstanding tasks being completed) prior to completing your review.

Some PRs may change functionality which isn't tested during that PR's tests, like a CI specific change that is only run on commits to `main`. These
should be tested manually in as close to the CI environment as possible (Consider running it in the same docker image that CI uses, render any
generated code, etc.). Changes which do not exhibit this behavior may optionally be tested locally by the reviewer, but it is not required. The PR
author should indicate explicitly if they expect the reviewer to perform local testing.

By default, the author of a PR should be the one to merge it (either by enabling auto-merge, or manually). After completing your review, make sure to
approve the GitHub PR, as well as any related Wrike approval workflows or tasks, but **refrain from merging the commit** unless the PR author
instructs you otherwise.
