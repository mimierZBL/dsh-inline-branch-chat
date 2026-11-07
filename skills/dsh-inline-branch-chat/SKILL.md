---
name: dsh-inline-branch-chat
description: Use when installing or verifying this repository's inline branch chat source patch for DeepSeek Harness dsh-v0.2.2-rc.1.
---

# Install inline branch chat

Use the patch in this repository only with DeepSeek Harness `dsh-v0.2.2-rc.1`. Follow [README.md](../../README.md) for user-facing behavior and limitations.

1. Find an isolated DSH source checkout at the exact tag. Do not overwrite an existing application bundle, user profile, conversation log, or other local modifications.
2. Run `git apply --check patches/dsh-v0.2.2-rc.1-branch-chat.patch` from the DSH checkout with the patch's absolute path. If it fails, stop and report the mismatch; do not force the patch.
3. Apply the patch, install dependencies with `pnpm install --no-frozen-lockfile`, then run `pnpm run build` and the focused tests listed in the README.
4. Launch through the supported `pnpm dsh web` profile. Test selection, branch creation, a context-dependent follow-up, independent model choice, math rendering, and the parent transcript remaining unchanged.

The × button closes a window but currently leaves the hidden child session log. Explain this accurately when helping a user manage their data. Do not claim compatibility with untested DSH versions or describe this source patch as a standalone plugin.
