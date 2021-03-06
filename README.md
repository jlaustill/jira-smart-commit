# JIRA Smart Commits
[![Stable Version](https://img.shields.io/npm/v/jira-smart-commit.svg)](https://www.npmjs.com/package/jira-smart-commit)
[![Build Status](https://travis-ci.org/jessedobbelaere/jira-smart-commit.svg?branch=master)](https://travis-ci.org/jessedobbelaere/jira-smart-commit)
[![MIT license](http://img.shields.io/badge/license-MIT-brightgreen.svg)](http://opensource.org/licenses/MIT)
[![Downloads](https://img.shields.io/npm/dt/jira-smart-commit.svg)](https://www.npmjs.com/package/jira-smart-commit)

A Node.js git hook script to prefix commits automatically with the JIRA ticket, based on a branch name.

## Usage

### Installation
1. Install [Husky](https://www.npmjs.com/package/husky) in your project to configure Git hooks easily
    ```
    npm install --save-dev husky
    ```
2. Install this package in your project:
    ```
    npm install --save-dev jira-smart-commit
    ```
3. Configure scripts in `package.json`. The script expects his first argument to be the JIRA tag of the project.
    ```
    "commitmsg": "jira-smart-commit SPAN"
    ```
4. Do your git commits like usual. If the branch was prefixed with a JIRA tag, your commit message will get prefixed with
the same tag.

```
Branch: TAG-411-husky-git-hooks
Commit message: "Add git hooks to project" → "TAG-411 Add git hooks to project"
```
