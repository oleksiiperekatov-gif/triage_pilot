# Triage Pilot

Slack-based pilot for collecting and triaging Evo product feedback.

## Goal

This repo is used by Cursor to run a pilot automation that:

- Reads selected Slack channels where Cursor has access.
- Finds recent Evo-related product feedback.
- Ignores messages older than 14 days.
- Deduplicates similar feedback.
- Tags feedback by product area, feature, and implementation ease.
- Posts and updates a triage inbox in Slack.
- Lets humans mark feedback as discarded, accepted, agent-candidate, in-progress, or done.

## Pilot Rules

- Source channels are allowlisted manually.
- Only scan the last 14 days of messages.
- Include thread replies.
- Do not create Linear issues by default.
- Do not launch coding agents automatically.
- Keep Slack as the triage UI.
- Keep durable state outside the Slack message.

## Triage Statuses

- `new`
- `accepted`
- `discarded`
- `agent-candidate`
- `in-progress`
- `done`

## Feedback Tags

Product area:

- onboarding
- agents
- editor
- integrations
- admin
- billing
- performance
- reliability
- other

Ease:

- easy
- medium
- hard
- unknown

## Slack Actions

Suggested reactions:

- ✅ accept
- 🗑 discard
- 🚀 agent candidate
- 🏗 in progress
- 🎉 done

## Notes

This is an MVP. The first phase should be observe-only: scan selected channels, deduplicate feedback, tag it, and post a proposed triage inbox for review.
