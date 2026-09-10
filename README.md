# Same Page

[English](README.md) | [한국어](README.ko.md)

**Align understanding. Agree on a plan. Execute together.**

Same Page is a Codex skill plugin that helps authors and AI confirm the purpose of a task, agree on a plan and task-specific constraints, execute the work, and verify the result.

**Review materials → ask important questions → confirm understanding → agree on a plan → confirm constraints → execute → verify**

When a new idea would change the agreed plan, Same Page explains the difference and impact and asks whether to update the plan. Explicit change requests are applied without asking for the same approval again.

## Repository contents

- `.agents/plugins/marketplace.json`: marketplace entry
- `plugins/same-page/.codex-plugin/plugin.json`: plugin manifest
- `plugins/same-page/skills/same-page/SKILL.md`: skill entry point
- `plugins/same-page/skills/same-page/references/workflow.md`: full workflow and task document templates
- `GLOBAL_INSTRUCTIONS.md`: optional instructions for applying the workflow broadly
- `VALIDATION.md`: completed checks and checks that still require a live environment

## Install

In a Codex workspace that supports plugins, import this repository as a marketplace:

- Source: `https://github.com/kaa9900-ops/same-page`
- Path: leave empty because the marketplace file is at the repository root

Then install **Same Page** from that marketplace. Marketplace import, plugin installation, and automatic use in every conversation are separate steps and may require workspace administrator access.

Official guidance: [Build plugins](https://learn.chatgpt.com/docs/build-plugins) and [Plugin management](https://learn.chatgpt.com/docs/enterprise/plugin-management).

## Use

Select the Same Page plugin or skill in a new conversation and make a request such as:

> Apply Same Page to this task. Review the attached materials, ask what you need to understand, and confirm your understanding before creating a plan.

Useful follow-ups include:

> Compare what we just discussed with the current plan.

> Apply the proposed change to the plan and constraints.

> Read the current plan and constraints, verify the actual files, and resume from the next task.

The plugin uses instructions and Markdown templates only. It has no server, API key, or external service dependency. Task-specific plans and constraints belong in the task's working directory, not inside the installed plugin.

## Apply the workflow broadly

Installing the skill does not make it run in every conversation. Merge the relevant text from `GLOBAL_INSTRUCTIONS.md` into your existing global instructions, without overwriting unrelated settings, then verify the behavior in a new conversation.

## Version and updates

The current release is `v0.1.0`. To update, sync or re-import the marketplace source, install the updated plugin version, and verify it in a new conversation. Release downloads are available on the [Releases page](https://github.com/kaa9900-ops/same-page/releases).

## License

Same Page is released under the [MIT License](LICENSE).
