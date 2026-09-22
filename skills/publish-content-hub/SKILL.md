---
name: publish-content-hub
description: Publish user-provided images, PDFs, documents, notes, and other materials to the existing AI_study Git repository at D:\00CodexWarkSpace\publish. Use for this publication repository only; do not build or deploy a website.
---

# Publish Content Hub

Publish requested materials through the existing Git repository at `D:\00CodexWarkSpace\publish`.

The public repository is `https://github.com/SongFeifei123/AI_study` and the expected remote is `git@github.com:SongFeifei123/AI_study.git` on branch `main`.

Do not build, update, or deploy a website. Do not use `D:\00CodexWarkSpace\publish-site` or a Sites project unless the user explicitly asks for website work in a later request.

## Publish materials

1. Inspect the supplied material and the repository state. Preserve the source content and original file format.
2. Add only the files requested for publication. Keep clear original filenames when practical; resolve collisions without overwriting unrelated material.
3. Use lightweight subject folders or a concise README index only when they materially improve discoverability. Do not create a site, generated catalog, or build output.
4. Stage explicit paths rather than the whole workspace. Review the staged file list and diff, and exclude credentials, temporary archives, caches, and unrelated files.
5. Commit with a descriptive message and push to `origin/main`. A request to publish materials authorizes that push; a request only to inspect or organize files does not.
6. Verify the pushed commit and return the repository URL, commit identifier, and the paths published.

Never expose credentials, tokens, private remote details, or unrelated local paths.
