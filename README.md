# Automated Weekly Dev Summary (n8n + Claude Code)

This workflow automatically fetches your GitHub repository's commits, closed issues, and merged PRs for the past week, uses the Claude API to generate a narrative summary, and posts it to a Discord webhook.

## Quick Setup (5 Steps)

1. **Import the Workflow**: Open your n8n instance, click **Add Workflow**, then select **Import from File** and upload `weekly_dev_summary_workflow.json`.
2. **Configure GitHub Repo & Language**: Double-click the **Config** node. Change the `GITHUB_REPO` value to your target repository (e.g., `owner/repo`) and the `SUMMARY_LANGUAGE` to your preferred language (e.g., `EN` or `FR`).
3. **Add Anthropic API Key**: In the same **Config** node, replace the `ANTHROPIC_API_KEY` placeholder with your actual Anthropic API key.
4. **Add Discord Webhook**: Still in the **Config** node, replace the `DISCORD_WEBHOOK_URL` value with your actual Discord Webhook URL.
5. **Activate**: Click the toggle switch in the top right corner of the n8n canvas to **Active**. The workflow will now automatically run every Friday at 5:00 PM (relative to your n8n server's configured timezone)!

> **Note**: This workflow strictly follows secure development guidelines by validating all fetched data subsets, extracting magic variables into a central Config node, and safely avoiding array duplication.
