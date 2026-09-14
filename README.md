# .github

Org-wide defaults. Any repo without its own `.github/ISSUE_TEMPLATE/` inherits these issue forms in the web UI.

## Issue templates

| Template | Label applied | Title should be |
| --- | --- | --- |
| Outcome | `type:outcome` | A plain sentence stating what is true when done |
| External dependency | `type:external` | The thing we need |
| Decision | `type:decision` | The question |
| Spike | `type:spike` | The question, ending in `?` |

`config.yml` disables blank issues so every issue picks a type.

## Rules

- No repo should add its own `ISSUE_TEMPLATE/` folder. Doing so replaces all of these, not just the one it overrides.
- Labels referenced here must exist in each repo. Run `/setup-board` from the build-workflow plugin, or `scripts/labels.sh`, in each new repo.
- Full writing rules live in the handbook and in the build-workflow plugin's `issue-writing` skill. These templates carry only the skeleton and one-line reminders.
