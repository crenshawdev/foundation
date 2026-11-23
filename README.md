# Foundation

Foundation is a Claude Code plugin marketplace. It lists Cadence, burnrate and Headroom, so you add one marketplace and install any of them from it.

## What's in it

- **[Cadence](https://github.com/crenshawdev/cadence)** brings engineering practices to software you'll keep running after the session ends. It writes a plan before code, commits once per task, holds tests to a stopping rule, and checks the result against your goal.
- **[burnrate](https://github.com/crenshawdev/burnrate)** builds a local dashboard of your own Claude Code token usage from your transcripts, and answers quick usage questions in chat.
- **[Headroom](https://github.com/crenshawdev/headroom)** reminds you to `/clear` with a toast when your session's context fills past a point you choose. The toast stays out of the transcript, so a reminder costs no tokens.

Each plugin lives in its own repository and carries its own version. Foundation only points at them, so a new release of a plugin needs no change here.

## Install

```
claude plugin marketplace add crenshawdev/foundation
claude plugin install cadence@foundation
claude plugin install burnrate@foundation
claude plugin install headroom@foundation
```

To pick up a new release later:

```
claude plugin marketplace update foundation
claude plugin update cadence@foundation
```

## If you already have one of these installed

Each plugin also has its own marketplace, and installs from there (`cadence@cadence`, `burnrate@burnrate`) keep working and keep getting updates. You don't have to switch.

If you do switch, remove the old install first:

```
claude plugin uninstall cadence@cadence
claude plugin install cadence@foundation
```

Don't leave both enabled. When two enabled plugins share a name, Claude Code leaves out the hooks of one of them.

The commands don't change either way. The prefix on a command comes from the plugin's name, so `/cadence:cad-progress` is the same from both marketplaces.
