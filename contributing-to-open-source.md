
# Contributing to open source projects

Every team at Visma, like any development organisation, relies heavily
on open source projects.  Many are maintained by volunteers who
investigate and fix bugs and security issues, publish new releases,
and keep documentation up to date, all in their spare time.

We can help them with contributions that are valuable both to Visma
and the projects, in smaller and larger ways:

- Submit useful issues when we find bugs
- Help investigate issues
- Test bug fixes
- Fix bugs
- Improve documentation
- Implement new functionality
- Review and test pull requests
- Become maintainers

The level of involvement will depend on how important the project is
to Visma and how well-supported it already is by others.  The time it
takes is of course a cost for Visma, since it will not be used to
develop new Visma-owned intellectual property (IP) directly.  But it
should be seen as an investment in the long-term health of the
product, or perhaps as the equivalent of a license fee for closed
software.


## Everyone can contribute

Contributing to open source is not limited to programmers.  Everyone
in a development team can help out with open source.  You also already
have the skills needed to contribute to open source projects, since
they are developed using the same processes and tools that we use in
our every day work: git and Github, branching, pushing code,
submitting pull requests, reviewing, testing and merging.

The rest of this document discusses the different ways you can
contribute to open source projects as a Visma employee.

The advice is also useful for extra-curricular contributions to open
source that is not directly related to what you do at Visma.  This is
a great way to learn new programming languages and frameworks.  To
help you get started many projects have issues labeled "up-for-grabs"
that are suitable for new contributors. The site
[up-for-grabs.net](https://up-for-grabs.net/) collects such issues for
a number of projects and languages.


# Issues

If you think that you've found a bug or run into some limitation or
other problem in an open source project, you can submit an issue to
the project.

But first, see if anyone else have already stumbled on the same
problem:

- Search among issues to see if it is already reported.
  - Remember to search among closed issues too, since the default search
    view on Github only searches among open issues.
  - Searching for error messages, exception texts or stacktraces can
    help locating issues for the same problem.

If this is a closed issue, you may find workarounds or find that it is
fixed in existing or upcoming releases.  If you find an open issue for
the problem you can subscribe to it to track developments.

If you don't find any issue, see if upgrading to the latest patch or
minor version helps, or even the major version, if you can.  There are
often nightly builds of the main development branch that you can try
to test too.


## Submitting issues

If it is an unreported problem, do submit an issue!  Projects often
have a template that they want you to fill in, but if not make sure to
include information that helps the maintainers reproduce and
understand the problem, e.g.:

- Version that the problem was found in
- Language/framework versions
- OS versions
- Any error messages or stack traces
  - Include them as text in code blocks, not screen shots. Text is
    searchable for others who have the same problem.
- How to reproduce the problem
  - E.g. a code example or command line.
  - Even better is a standalone minimal code project that reproduces the bug.
- Any workarounds you may have found

If you later find out that the problem was not with the project itself
but how you used it, close the issue with a comment explaining what
you did to solve it.  This will help people who have the same problem
later when they find the issue.


## Improving issues

If you find an open issue for a problem you've run into, see if you
can flesh out that issue by providing more information that can help
solve it.  If the issue already contains everything you know, you can
add your vote to how important it is by adding a `+1` emoji by
clicking the face button on the original issue report.  (Don't add
spammy "me too!" comments.)

Adding this to the issue also have the bonus that you get subscribed
to it automatically and can track any further discussions or fixes.


## Following up on issues

If you report an issue and the developers respond, make sure you
follow up and help them with any further information that you can
provide.  Issues where there's no responses to questions from the
developers tend to be marked as stale and closed after some time.

When a bug fix is proposed in a pull request have a look at it, if
possible test it, and provide feedback.


# Bug fixes

Think you can fix a bug you've found in an open source project?  Start
by reporting it as described above, and add a note that you will try
to fix it yourself.

Fixing bugs in open source is not much different than in your
Visma projects, but you have to think about some more things:

- Most projects have a `CONTRIBUTING.md` or similar file that
  describes tool pre-requisites, build and test steps, and any other
  information that is important to maintain the quality of the code.
  Read it before you start.  Sometimes this is in the `README`
  instead.

- If that document doesn't say it, try to figure out which code branch
  to work against.  Do they want fixes against `main`, `dev` or a
  release branch?

- Reference the issue ID number as `#123` in the commit messages to
  link them and the pull request to the issue.

- Follow the code style and naming standards in the project so it
  stays a consistent style, even if this is different from your own
  project's standards.

- Whenever possible add unit tests that show the bug and that the fix
  solves it.

- Sometimes you have to approve a contributor's license agreement
  before your PR can be merged, agreeing that you sign over copyright
  to the code to the project.  This shouldn't be an IP issue for bug
  fixes.

## Forking

One big difference to working on your own project is that you will not
have write permissions to the open source project repository.  You
have to fork the repository, which gives you a copy where you can
create branches and push your code to.  When finished you create a PR
that requests that it is merged back into the main repository.

[This page](https://www.dataschool.io/how-to-contribute-on-github/)
provides an excellent overview of the steps in a forked workflow and
some good practices when working with forks.


## Email addresses in commits

If you don't want to expose your Visma email address in the commits
or want to have the commits associated with your personal email
instead, you have to change the per-repository settings:

    cd some-open-source-project
    git config user.email xzyzzy@example.com

SourceTree and other graphical interfaces also let you change this.
If you forget to do this and create some commits, you can [change the
author information on them afterwards with an interactive
rebase](https://stackoverflow.com/questions/3042437/how-to-change-the-commit-author-for-one-specific-commit#3042512).

If you already have pushed the commits to your forked repository, you
will have to do a forced push to replace them.  Once a PR has been
merged you cannot change the email address later.

You can have a single Github account that is linked to both your
personal email and the Visma email.  If you contribute to open source
with your Visma email in the commits then it will be possible to link
them through your Github account to any contributions you've made on
with your personal email.  This is normally perfectly fine.  The
exception is if you have made Github contributions to questionable
repositories where that link could damage Visma (think tabloid
headlines here).  In this case you should use your personal email for
the open source contributions, or create a new Github account for
them.


# Improving documentation

There are not that many people who enjoy writing documentation for
free, so open source can be lacking in documention.  If you find
errors or missing documentation and like to patch the gap, it will be
much appreciated by the maintainers.

Most projects maintain the documentation as part of the code
repository, either as markdown files or inline code documentation
comments.  Submitting fixes to documentation thus follows the same
process as submitting a bug fix, but you don't have to create an issue
beforehand and can submit the PR directly.

Github has good support for editing markdown files directly on the
website, so you don't have to clone your forked repository to your
laptop but can work directly in the web GUI if you want.


# Implementing new functionality

If you have an idea for improvements or extensions that is general
enough to support both you and other users, start by submitting an
issue explaining it and outlining how you think that you can implement
it.  Expect discussion in the issue, as the project maintainers can
have their own plans which means that the change is not a good fit as
suggested, or suggest a better way of how to implement it.

If the maintainers agree on the idea, go ahead and implement it
following the same process as when submitting a bug.  Don't forget to
update relevant documentation too.

The new functionality cannot contain any Visma IP, as the code will
become open source too.  Get your managers approval before submitting
any code.  The contributor's agreement may also require you to assign
the copyright to the project.


# Reviewing and testing pull requests

Once you have some significant code in a project or really care about
its future direction, you may want to start to monitor the pull
requests that come in and review the ones that touch on your
interests.  QAs can help test PRs too.


# Maintaining open source projects

If you start being visible in projects by submitting code, discussing
issues and reviewing PRs, you may be asked to become a maintainer.
This typically comes with push rights to the main repository and
influence over the roadmap, but also expectations that you will
review PRs and help with fixing bugs.

It is a commitment, and you need to discuss in your team and your
manager how much time you may have to devote to this, and if you have
that time.

Think about if you have a special focus area, and make it clear to the
other maintainers if you will prioritise that and not look much on
other parts of the project.  Also be clear about if you will leave the
maintainer role if you leave the Visma project, or stay on.
