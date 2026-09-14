# .github

Organization defaults. Any repo without its own `ISSUE_TEMPLATE/` inherits these forms on the New issue screen.

## Before these work

Create the four **Issue Types** in the organization first, or the `type:` line in each form is ignored:

Organization settings → Planning → Issue types → add `Outcome`, `External`, `Decision`, `Spike`. Disable the defaults (Bug, Task, Feature) so nobody picks them.

## Forms

| Form | Sets issue type | Title should be |
| --- | --- | --- |
| Outcome | Outcome | A plain sentence stating what is true when done |
| External dependency | External | The thing we need |
| Decision | Decision | The question |
| Spike | Spike | The question, ending in `?` |

`config.yml` disables blank issues so every issue has a type.

## Why YAML forms and not markdown templates

Only YAML issue forms can set the `type:` qualifier and mark fields required. The type is an org-level property of the issue, filterable in every repo and every project via the built-in **Type** field, so it replaces the old `type:*` labels entirely.

## Location

These live in `ISSUE_TEMPLATE/` at the root of this repo. GitHub also accepts `.github/ISSUE_TEMPLATE/` inside this repo; use one, not both.

## Rules

- No repo should add its own `ISSUE_TEMPLATE/` folder. Doing so replaces all of these, not just the one it overrides.
- Full writing rules live in the handbook and in the build-workflow plugin's `issue-writing` skill. The forms carry only the skeleton and one-line reminders.
- If Issue Fields (org-level, currently preview) are enabled, pin `Waiting on`, `Asked on`, `Needed by` to External and `Owner`, `Needed by` to Decision. The form inputs above then become redundant and can be removed.
