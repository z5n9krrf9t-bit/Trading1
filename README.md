# Trading1

Day-trading toolkit for Claude Code.

## Skills

`.claude/skills/trader-*` holds the eleven skills from
[Jakeschincariol/day-trader-skill](https://github.com/Jakeschincariol/day-trader-skill)
(MIT, commit 3d0f4ef), copied in as project skills because
`/plugin` is not available in Claude Code cloud sessions. They are invoked as
`/trader-scanner`, `/trader-news`, `/trader-entry`, `/trader-exit`,
`/trader-timemachine`, `/trader-budget`, `/trader-risk`, `/trader-broker`,
`/trader-alerts`, `/trader-analyst` and `/trader-pelosi`.

Python 3.8+, standard library only. Output lands in `trader/` (git-ignored).
The SEC tools need `SEC_USER_AGENT="Your Name you@example.com"`.

## Safety

- Not financial advice. Most day traders lose money.
- No skill places orders by itself. `/trader-broker` needs a broker connector
  (e.g. Alpaca MCP, paper account by default) plus an explicit yes per order.
- `.claude/settings.json` forces a permission prompt for Alpaca order tools and
  blocks the bulk/option/crypto ones.
