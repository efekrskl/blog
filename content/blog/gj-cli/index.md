+++
title = "gj - dead simple journaling CLI"
description = "gj is a dead simple journaling CLI. Directly from the terminal to Notion. No clutter, no fuss."
date = 2025-04-10
slug = "gj-cli"

[taxonomies]
tags = ["Projects"]

[extra]
display_published = true
+++

![An example CLI prompt with gj](cover.png)

[gj is an open-source journaling CLI](https://github.com/efekrskl/gj) that allows you to write journal entries directly from the terminal and save them to Notion.

### Idea
I came up with the idea for gj after struggling with sticking to work journaling. [Notion](https://www.notion.com/) is already a great tool for journaling.
After reading [Atomic Habits by James Clear](https://jamesclear.com/atomic-habits) I realized, there was still some friction in the process of writing journal entries.
So I decided to build a tool that would remove that friction and take advantage of me already using my terminal every day.

My original approach was to build a hook that would save your commits and turn them into journal entries.
However, I wasn't sure if this would be legal or not. Instead, I kept how one would journal similar to how one would write a commit message.

"gj" is a play on the common phrase "good job" that you would say to yourself after completing a task or writing a journal entry.

### Goals
The goal was to build a simple CLI tool that allows you to write your journals directly from the terminal and save them to Notion.

Additionally, I wanted to learn [Rust](https://www.rust-lang.org/) and build a tool with it. I think it is an amazing language and I hope to use it more in the future.

### Tech Stack

Well, Rust. And Notion's API.

### Key Features

These were my must-haves:

- [x] Journal from the terminal with a simple syntax (`gj "hello world"`)
- [x] Automatically create the Notion page and database

Some nice-to-haves:
- [ ] Brag functionality (summarize entries and automatically create a brag document)
- [ ] Support non-Notion databases (e.g. local files, other APIs)

### Learnings

Although a simple project through gj I learned a lot about Rust and how to build a CLI tool with it.

### Aftermath

![The calendar view in Notion with gj entries](notion.png)

Due to some limitations in Notion's API, gj was not "as automated" as I wanted it to be. It still ended up being a useful tool.
It attracted some users and even some contributors.
