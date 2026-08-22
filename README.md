
<div align="center">

# Gitweaver

**All of Git. Nothing hidden.**

A desktop Git client that drives the same `git` you would type yourself — and
shows you every command it runs. Nothing is reimplemented, so nothing behaves
differently here than it does in your terminal.

[**Download**](https://github.com/codertapsu/gitweaver-release/releases/latest) ·
[Features](#features) ·
[Installation](#installation) ·
[Requirements](#requirements)

![Latest release](https://img.shields.io/github/v/release/codertapsu/gitweaver-release?display_name=tag&sort=semver&style=flat-square&label=latest%20release&color=555)

</div>

---

## Overview

Most Git GUIs offer a safe subset and hide the rest. Gitweaver takes the other
position: the whole of Git is available, and the exact invocation behind every
button is on screen while it runs. When something goes wrong you are told what
happened in a sentence — and the full command, verbatim, is one click away.

It is a native desktop application, not a browser in a window. Your repository
never leaves your machine, and there is no account to make.

## Features

- **A console, in the window.** Anything Gitweaver has no button for is one
  command away: type it, see exactly what Git printed, and see the exit code.
  Suggestions complete what you type in grey from what you last ran. It runs
  `git` and nothing else — never a shell — so the punctuation in a commit
  message is punctuation.
- **See the conflict coming.** Gitweaver asks Git which files a merge _would_
  conflict on, before you start it — so you find out while you can still choose,
  not from the middle of a merge you did not want.
- **Diffs that read like changes.** Side-by-side or inline, syntax-coloured, with
  the changed _words_ picked out inside a changed line rather than leaving you two
  long lines and a spot-the-difference puzzle. Moved blocks are marked as moved
  rather than reported as a deletion and an unrelated addition. Images diff as
  images.
- **Take a change with you, or throw part of it away.** Copy any diff as a
  patch, or save it as a `.patch` file. Discard a single hunk, or only the
  lines you picked, and the rest of the file is left alone.
- **Find a file by typing part of its name.** Fuzzy, ranked, over the whole
  repository at any revision.
- **Find a string anywhere in the working tree.** Plain text or a regular
  expression, grouped by file, and one click lands on the line. When there are
  more matches than it will show, it says so rather than quietly stopping.
- **Everything by name.** One keystroke opens a palette over the views, the sync
  actions, your branches, and the settings — so nothing you can do is buried in a
  menu you have to remember the shape of.
- **History as a graph.** Every branch and merge drawn as lanes, built to stay
  smooth at a hundred thousand commits.
- **Blame, line history, and file churn.** Who last touched each line; the
  commits that touched _these_ lines; a file's churn over time so a spike takes
  you to the commit that caused it.
- **Signatures, answered honestly.** Verified, present-but-unproven, and broken
  are three different answers, and Gitweaver gives all three rather than
  flattening them into two.
- **Untracked files are not a dead end.** Delete them from a plan that names
  what goes, or add them to `.gitignore` from the row — with the exact pattern
  shown before it is written, and Git asked afterwards whether it took.
- **Remotes you can actually manage.** Add, rename, re-point and remove them,
  with fetch and push URLs kept apart when they differ. Every branch is counted
  against its own upstream, so the ones with unpushed work are visible at a
  glance.
- **Merge the way your project merges.** Fast-forward, always-a-merge-commit,
  fast-forward-only, or squash — chosen rather than assumed. Reverting a merge
  asks which side to undo.
- **A dirty tree does not stop a pull.** When local changes are in the way,
  Gitweaver offers to stash them, run the pull or rebase, and put them back — as
  one action, at the moment it matters, rather than as a checkbox you were
  supposed to have found earlier.
- **Look inside a stash before you apply it.** A stash is a commit, so it gets
  the same diff view as anything else — applying one stops being an act of
  memory.
- **Put a single file back the way it was.** Browse any revision and restore one
  file from it into your working tree, with what gets overwritten named first.
- **Amending tells you the truth.** If the commit you are about to replace is
  already pushed, you are told before you amend it — not by the push that fails
  afterwards.
- **Worktrees, submodules, LFS, reflog, bisect, stash** — including the parts
  most clients leave out. Submodules can be added, removed and synced, not just
  listed.
- **Interactive rebase by dragging** — or with the keyboard — with the plan
  shown in the order Git will apply it. Slot in a command to run between
  commits, so your tests decide whether the rebase carries on, or a pause to
  look around. The plan is checked before Git starts rather than failing
  halfway through it.
- **Remove a secret from every commit**, with the cost spelled out before
  anything is rewritten.
- **Your own terminal, one click away**, already in the repository.
- **Six themes**, light and dark and four more.
- **Updates itself**, and only ever from the welcome screen — never while you
  have a repository open. Every update is signed and verified before it is
  installed.

## Download

Get the latest build from the
[**Releases**](https://github.com/codertapsu/gitweaver-release/releases/latest)
page.

| Platform    | File                                | Notes                                    |
| ----------- | ----------------------------------- | ---------------------------------------- |
| **macOS**   | `Gitweaver_<version>_universal.dmg` | Intel and Apple silicon, in one download |
| **Windows** | `Gitweaver_<version>_x64-setup.exe` | Installer (NSIS)                         |
| **Windows** | `Gitweaver_<version>_x64_en-US.msi` | Same app, for deployment tools           |

## Installation

### macOS

1. Download and open the `.dmg`.
2. Drag **Gitweaver** into your **Applications** folder, then launch it.

One download covers both kinds of Mac — it is a universal binary, so an Intel
Mac and an Apple silicon Mac run the same file, each at full native speed. The
app is notarized by Apple, so it opens without a Gatekeeper warning, and there
is nothing else to install.

### Windows

1. Download the `-setup.exe` and run it.
2. Windows SmartScreen currently warns on first run, because these builds are
   not yet Authenticode-signed. Choose **More info → Run anyway**.

The `.msi` is the same application packaged for tools that deploy MSIs; either
one is fine for a single machine.

## Requirements

- **Git** must be installed and on your `PATH`. Gitweaver runs your Git rather
  than shipping its own, which is what makes its behaviour match your terminal's
  — including your config, your hooks, and your credential helpers.
- **macOS 11** (Big Sur) or later, on **Intel or Apple silicon**. Both slices
  are built for 11.0. Keep Safari up to date on Big Sur and Monterey: the
  interface uses CSS that arrived in Safari 16, and the version of WebKit an app
  gets is the one the system has.
- **Windows 10** (1803) or later, 64-bit.

## Reporting a problem

Open an issue on this repository. Every failure Gitweaver shows has a **See
more** button with the exact command that ran and everything Git printed —
pasting that in makes a report far easier to act on.

## Source

The source repository is private. This repository exists to distribute the
builds and to collect issues.
