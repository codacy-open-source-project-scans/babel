# Babel Contribution Guidelines

Welcome to Babel! These guidelines will give you a short overview over how we
handle issues and PRs in this repository. Note that they are preliminary and
still need proper phrasing - if you'd like to help - be sure to make a PR.

Please know that we do appreciate all contributions - bug reports as well as
Pull Requests.

## Setting up a development environment and running tests

After you've cloned the repository,

1. Set up a Python virtualenv (the methods vary depending on tooling and operating system)
  and activate it.
2. Install Babel in editable mode with development dependencies: `pip install -e .[dev]`
3. Run `make import-cldr` to import the CLDR database.
  This will download the CLDR database and convert it to a format that Babel can use.
4. Run `make test` to run the tests. You can also run e.g. `pytest --cov babel .` to
   run the tests with coverage reporting enabled.

You can also use [Tox][tox] to run the tests in separate virtualenvs
for all supported Python versions; a `tox.ini` configuration (which is what the CI process
uses) is included in the repository.

## On pull requests

### PR Merge Criteria

For a PR to be merged, the following statements must hold true:

- All CI services pass. (Windows build, linux build, sufficient test coverage.)
- All commits must have been reviewed and approved by a babel maintainer who is
  not the author of the PR. Commits shall comply to the "Good Commits" standards
  outlined below.

To begin contributing have a look at the open [easy issues](https://github.com/python-babel/babel/issues?q=is%3Aopen+is%3Aissue+label%3Adifficulty%2Flow)
which could be fixed.

### Correcting PRs

Rebasing PRs is preferred over merging master into the source branches again
and again cluttering our history. If a reviewer has suggestions, the commit
shall be amended so the history is not cluttered by "fixup commits".

### Writing Good Commits

Please see
https://api.coala.io/en/latest/Developers/Writing_Good_Commits.html
for guidelines on how to write good commits and proper commit messages.

[tox]: https://tox.wiki/en/latest/
