# Forgeby for Claude

[Forgeby](https://forgeby.com) is the AI workforce for revenue teams: B2B sellers and go-to-market teams. It works on top of your CRM.

This plugin brings Forgeby into Claude. It holds eleven seller skills on the Forgeby connector (`https://forgeby.com/api/mcp`).

The Forgeby app stays your main desk. Claude is a second door on the same workspace, with the same tools, memory, approval cards and rules.

The plugin does not send, enrol, or write a record. A write returns an approval link. A person opens it in Forgeby and sends.

You need a Forgeby workspace and a seat. When you sign in, Claude sees that seat's tools and data only.

## The skills

| Skill | Use it when you ask |
|---|---|
| `morning-brief` | who to call today, and why now |
| `account-research` | what Forgeby knows about one account |
| `meeting-prep` | for a brief before a meeting on your calendar |
| `pipeline-review` | which deals are stalled or at risk, and the next step |
| `what-changed` | what changed on your accounts since a date |
| `champion-check` | who left or moved at an account |
| `can-i-contact` | whether you may reach a person, and why |
| `found-revenue` | for leads with real signal that nobody followed up |
| `follow-up-draft` | for a follow-up draft, ready for your approval |
| `log-what-happened` | to put a call or meeting outcome on the record |
| `what-kvasir-learned` | what Forgeby learned from your team this week |

## Install

### Claude Code

```
claude mcp add --transport http forgeby https://forgeby.com/api/mcp
claude plugin marketplace add jacobahmid-stack/forgeby-claude-plugin
claude plugin install forgeby@forgeby
```

Sign in with your Forgeby seat when asked.

### claude.ai and Claude Desktop

1. Open Customize, then Connectors.
2. Add a custom connector with the URL `https://forgeby.com/api/mcp`. On Team and Enterprise plans, an Owner adds it under Organization settings, and then each seat clicks Connect.
3. Sign in with your Forgeby seat.

Free plans allow one custom connector.

## After you connect

Ask for your morning brief. A write ends in an approval link on `https://forgeby.com/forge/waiting?card=`. Open it in Forgeby and choose Approve or Decline. Nothing is sent until then.

## What Forgeby does not do

- Forgeby does not replace your CRM.
- It does not send a message without your permission.
- It does not state a fact without its source and date.
- It does not scrape LinkedIn.

## Links

- Documentation: https://forgeby.com/mcp
- Privacy: https://forgeby.com/privacy.html
- Terms: https://forgeby.com/terms
- Support: hello@forgeby.com

## License

Apache License 2.0. See [LICENSE](LICENSE) and [NOTICE](NOTICE).
