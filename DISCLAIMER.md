# ⚠️ Disclaimer & Liability Limitation

**Use at your own risk.** The code, workflows, and scripts in this repository (`n8n-hubspot-nps-detractor-slack-huddle-provisioner`) are provided for educational and architectural demonstration purposes.

## No Liability

The author and dhRobin Systems accept no responsibility or liability for any direct, indirect, incidental, or consequential damages that result from using, misusing, or deploying these scripts. That includes, without limitation:

- emergency alerts that were sent, missed, delayed, duplicated or routed to the wrong people or channels;
- retention tasks, emergency tickets or company property changes (`retention_status`, `last_nps_score` and related fields) created or written in error, or not created when expected;
- customer relationships, renewals or revenue affected by a response that the workflow triggered, or failed to trigger;
- survey comments or respondent details exposed in Slack, HubSpot tasks, tickets, webhooks or n8n execution data;
- API quota consumption, rate limiting or account restrictions imposed by HubSpot or Slack.

## No Warranty

All software, n8n JSON blueprints, JavaScript modules and prompts are provided "AS IS", without warranty of any kind, express or implied. This includes, but is not limited to, warranties of merchantability, fitness for a particular purpose, and non-infringement.

The NPS categories, segment rules, churn keywords and response tiers are heuristics. A detractor score isn't a churn prediction, and a promoter score isn't a guarantee of renewal. I make no warranty that every at-risk customer will be flagged, or that every flagged customer is at risk.

## Production Testing Required

Always test thoroughly in an isolated staging environment, such as a HubSpot developer test account or sandbox, with `SANDBOX_MODE=true`, `DRY_RUN=true`, `SEND_SLACK_ALERTS=false` and `WRITE_TO_HUBSPOT=false` enabled, before you connect live HubSpot or Slack credentials.

Before enabling live outputs:

- confirm your tier values, contract value threshold, internal domains and test-account patterns against real (but test-channel) data;
- confirm task owners, ticket pipeline and stage IDs, and the *At Risk* dropdown option exist in your portal;
- send alerts to a test Slack channel first, and review the mentions and the respondent details shown;
- unpin every node you expect to run live.

Treat every emergency alert and retention task as a prompt for a person to contact the customer, not as a judgement about the customer, the respondent or the account team.

## Third-Party APIs & Compliance

You alone are responsible for complying with the terms of service, rate limits, data privacy regulations (GDPR/CCPA), and security policies of HubSpot, Slack and any connected services. That includes:

- telling survey respondents how their answers are used and that they may be followed up;
- confirming a lawful basis for following up on identified survey responses;
- limiting who can see survey comments and respondent details in Slack and HubSpot;
- honouring access and deletion requests across HubSpot, Slack and n8n execution data;
- securing every token, shared webhook secret and webhook URL;
- reviewing every automatically created task, ticket and property change.

Slack and HubSpot features, endpoints and scopes change over time. Verify them against current vendor documentation before deploying.

## License

Released under the MIT License. Copyright (c) 2026 DH Robin (dhRobin Systems). See [LICENSE](LICENSE).

---

Full text: DISCLAIMER.md · Licensed under the MIT License. License: MIT © 2026 dhRobin Systems · Provided as-is, see the disclaimer.
