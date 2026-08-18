
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

- **See the conflict coming.** Gitweaver asks Git which files a merge _would_
  conflict on, before you start it — so you find out while you can still choose,
  not from the middle of a merge you did not want.
- **Diffs that read like changes.** Side-by-side or inline, with moved blocks
  marked as moved rather than reported as a deletion and an unrelated addition.
  Images diff as images.
- **Find a file by typing part of its name.** Fuzzy, ranked, over the whole
  repository at any revision.
- **History as a graph.** Every branch and merge drawn as lanes, built to stay
  smooth at a hundred thousand commits.
- **Blame, line history, and file churn.** Who last touched each line; the
  commits that touched _these_ lines; a file's churn over time so a spike takes
  you to the commit that caused it.
- **Signatures, answered honestly.** Verified, present-but-unproven, and broken
  are three different answers, and Gitweaver gives all three rather than
  flattening them into two.
- **Worktrees, submodules, LFS, reflog, bisect, stash** — including the parts
  most clients leave out.
- **Interactive rebase by dragging**, with the plan shown in the order Git will
  apply it.
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
