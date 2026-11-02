# MDEconomy: Issues and Suggestions

This is the public place to **report bugs** and **suggest features** for **MDEconomy**, the all-in-one economy plugin by MinecraftDevs (auction house, bidding auctions, player stalls, trading, jobs, its own Vault economy and cross-server sync).

There is no plugin code here. This repository only holds issues.

| I want to... | Go here |
| --- | --- |
| Report a bug | [New bug report](../../issues/new?template=bug_report.yml) |
| Suggest a feature or improvement | [New suggestion](../../issues/new?template=feature_suggestion.yml) |
| Get setup help or ask a question | [Discord](https://discord.gg/chQDaW3QXc) |
| Fix a license, purchase or download problem | [Discord](https://discord.gg/chQDaW3QXc) (open a ticket) |

## Reporting a bug

1. **Update first.** Make sure you run the latest MDEconomy version; the bug may already be fixed.
2. **Search** the [open and closed issues](../../issues?q=is%3Aissue) to see if it is already reported. If it is, add a comment with your details instead of opening a new issue.
3. **Open a [bug report](../../issues/new?template=bug_report.yml)** and fill in every field you can:
   - MDEconomy version (`/version MDEconomy`)
   - Server software and version (`/version`) and Java version
   - Storage type (SQLite, MySQL/MariaDB or MongoDB)
   - Single server or network, and the sync messenger if sync is enabled
   - Exact steps to reproduce, expected and actual behavior
   - The full console error or a [mclo.gs](https://mclo.gs) link to `logs/latest.log`

> [!WARNING]
> **Never post passwords, database URIs, Redis passwords, Discord webhook URLs, license keys or order numbers.** Remove them from logs and config before posting.

### Security problems

If you find a dupe, an exploit or anything that could hurt servers running MDEconomy, **do not open a public issue**. Report it privately on [Discord](https://discord.gg/chQDaW3QXc) so it can be fixed before it is known.

## Suggesting a feature

Open a [suggestion](../../issues/new?template=feature_suggestion.yml) and explain the problem it solves for your server, not only the feature. If the idea already exists, give it a 👍 reaction; the most-wanted suggestions are looked at first.

## Labels

Every issue is labeled automatically by its template and by the areas you pick, then moved along by the team.

| Label | Meaning |
| --- | --- |
| `bug` | Something does not work as it should |
| `suggestion` | A feature request or improvement |
| `needs-info` | We need more details from you. It is removed automatically when you reply |
| `confirmed` | Bug reproduced, or suggestion accepted |
| `in-progress` | Being worked on |
| `fixed` | Fixed or added; ships in the next release |
| `wontfix` | Will not be fixed or added |
| `duplicate` | Already reported in another issue |

Area labels: `auction`, `stalls`, `trading`, `jobs`, `economy`, `network-sync`, `config`, `other`.

## Rules

- **One bug or one idea per issue.**
- **English please**, so everyone can follow along.
- **Be respectful.** No spam, insults or "+1" comments; use reactions instead.
- **Support is for buyers of MDEconomy.** Issues about cracked, leaked or redistributed copies are closed without an answer.
- Issues that stay in `needs-info` without a reply for a long time may be closed. You can always reopen them with the missing details.
- This is not a support desk for other plugins. If the problem is caused by another plugin, please report it to its author.

## Maintainer setup

Things that are configured once by the repository owner:

1. **Labels.** The **Sync labels** workflow creates every label from [`.github/labels.json`](.github/labels.json) when that file changes on `main`. Run it by hand from the Actions tab to resync, and tick *delete other labels* once to remove GitHub's default labels.
2. **Project board.** Create a GitHub Project (for example *MDEconomy Roadmap*) under your account.
3. **Token.** Create a **classic** personal access token with the `project` scope (add `repo` if this repository is private), and save it as the repository secret `ADD_TO_PROJECT_PAT` (Settings > Secrets and variables > Actions > Secrets).
4. **Project URL.** Save the project's URL (for example `https://github.com/users/Vasilew69/projects/1`) as the repository **variable** `PROJECT_URL` (same page, Variables tab). Until it is set, the **Add issues to project** workflow is skipped.
5. Optional: in Settings > General, turn off Wikis and Projects tab if you do not use them, and in Settings > Actions > General allow workflows to have read and write permissions only if the label workflows report permission errors.
