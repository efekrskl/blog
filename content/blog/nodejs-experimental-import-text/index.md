+++
title = "A Better Way to Load Prompts, SQL & Markdown in Node.js"
description = "Node.js just shipped a feature that lets you import files as text directly!"
date = 2026-07-10
slug = "nodejs-experimental-import-text"

[taxonomies]
tags = ["Software Engineering"]

[extra]
display_published = true
+++

### A Better Way to Load Prompts, SQL & Markdown in Node.js

Node.js just shipped `--experimental-import-text`, which lets you import text files directly as strings. 
That means loading `.txt`, `.sql`, `.html`, Markdown, or LLM prompt files becomes much cleaner.

*(I'd also shamelessly like to mention that I implemented this feature in Node.js core. 🎉)*

Deno and Bun have supported similar functionality for a while, and I'm glad to see Node.js moving in the same direction. 
Having similar capabilities across JavaScript runtimes makes it easier to write portable code, which I think is very critical for JavaScript's future.

You can read more about the TC39 proposal here: https://github.com/tc39/proposal-import-text

Or check out the Node.js implementation: https://github.com/nodejs/node/pull/62300

How to use it you say?
```js
// before
import { readFileSync } from 'node:fs';

const template = readFileSync(
  new URL('./template.html', import.meta.url),
  'utf8',
);

console.log(template);

// after
import template from './template.html' with { type: 'text' };

console.log(template);
```
