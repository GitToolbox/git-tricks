<!-- markdownlint-disable -->
<p align="center">
    <a href="https://github.com/GitToolbox/">
        <img src="https://cdn.wolfsoftware.com/assets/images/github/organisations/gittoolbox/black-and-white-circle-256.png" alt="GitToolbox logo" />
    </a>
    <br />
    <a href="https://github.com/GitToolbox/git-tricks/actions/workflows/cicd.yml">
        <img src="https://img.shields.io/github/actions/workflow/status/GitToolbox/git-tricks/cicd.yml?branch=master&label=build%20status&style=for-the-badge" alt="Github Build Status" />
    </a>
    <a href="https://github.com/GitToolbox/git-tricks/blob/master/LICENSE.md">
        <img src="https://img.shields.io/github/license/GitToolbox/git-tricks?color=blue&label=License&style=for-the-badge" alt="License">
    </a>
    <a href="https://github.com/GitToolbox/git-tricks">
        <img src="https://img.shields.io/github/created-at/GitToolbox/git-tricks?color=blue&label=Created&style=for-the-badge" alt="Created">
    </a>
    <br />
    <a href="https://github.com/GitToolbox/git-tricks/releases/latest">
        <img src="https://img.shields.io/github/v/release/GitToolbox/git-tricks?color=blue&label=Latest%20Release&style=for-the-badge" alt="Release">
    </a>
    <a href="https://github.com/GitToolbox/git-tricks/releases/latest">
        <img src="https://img.shields.io/github/release-date/GitToolbox/git-tricks?color=blue&label=Released&style=for-the-badge" alt="Released">
    </a>
    <a href="https://github.com/GitToolbox/git-tricks/releases/latest">
        <img src="https://img.shields.io/github/commits-since/GitToolbox/git-tricks/latest.svg?color=blue&style=for-the-badge" alt="Commits since release">
    </a>
    <br />
    <a href="https://github.com/GitToolbox/git-tricks/blob/master/.github/CODE_OF_CONDUCT.md">
        <img src="https://img.shields.io/badge/Code%20of%20Conduct-blue?style=for-the-badge" />
    </a>
    <a href="https://github.com/GitToolbox/git-tricks/blob/master/.github/CONTRIBUTING.md">
        <img src="https://img.shields.io/badge/Contributing-blue?style=for-the-badge" />
    </a>
    <a href="https://github.com/GitToolbox/git-tricks/blob/master/.github/SECURITY.md">
        <img src="https://img.shields.io/badge/Report%20Security%20Concern-blue?style=for-the-badge" />
    </a>
    <a href="https://github.com/GitToolbox/git-tricks/issues">
        <img src="https://img.shields.io/badge/Get%20Support-blue?style=for-the-badge" />
    </a>
</p>

## Overview

This is a collection of tips and tricks to level up your git usage.

### Get the default branch for a given repository

```shell
git remote show origin | grep 'HEAD' | cut -d':' -f2 | sed -e 's/^ *//g' -e 's/ *$//g'
```

### Get the latest tag from a repository URL

```shell
git -c versionsort.suffix=- ls-remote --tags --sort=v:refname https://github.com/GitHooksToolbox/prompt-default-branch-commit-deprecated '*.*.*' | awk -F/ '/refs\/tags\// {print $3}' | tail -n1
```

<br />
<p align="right"><a href="https://wolfsoftware.com/"><img src="https://img.shields.io/badge/Created%20by%20Wolf%20on%20behalf%20of%20Wolf%20Software-blue?style=for-the-badge" /></a></p>
