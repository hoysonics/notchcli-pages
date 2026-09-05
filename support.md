# AgentMeter on Notch Support

AgentMeter on Notch shows Codex CLI quota and Claude Code token activity at the top of your Mac display. The App Store version requires macOS 14 or later and Apple silicon (M1 or later).

## Open the panel

Hover over or click the hardware notch. Clicking pins the panel open. On a Mac without a notch, use the compact panel at the top edge of the display.

## Allow log access

Use Claude Code or Codex CLI once on this Mac. Open Settings from the panel footer, then choose the log folder for each tool you use. Either tool works on its own.

In the folder picker, press Command-Shift-G, enter `~/.claude` for Claude Code or `~/.codex` for Codex CLI, then confirm the folder. These folders are normally hidden in Finder. AgentMeter on Notch requests read-only access and stores the permission in the macOS App Sandbox.

## Missing quota data

Codex quota is read from rate-limit events in local Codex CLI session logs. Run a new Codex CLI session if no recent limits are available.

The App Store version cannot run the `claude` command. Claude token activity works from local logs, but remaining quota requires a compatible, up-to-date snapshot at `~/.claude/notchcli-usage.json`, created by another tool. AgentMeter on Notch does not create or update that file. Snapshots more than 30 minutes old are ignored. Installing Claude Code alone does not enable Claude quota in the App Store version.

If a forecast is unavailable, keep using the CLI normally. A forecast needs enough quota readings over time; a missing forecast does not mean log access failed.

## Contact

For help, email thinoo@thepsyentist.com.
