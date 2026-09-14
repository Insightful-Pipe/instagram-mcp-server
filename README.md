# Instagram MCP Server by Insightful Pipe

[![MCP Compatible](https://img.shields.io/badge/MCP-Compatible-blue)](https://insightfulpipe.com/mcp-servers/instagram)
[![Insightful Pipe](https://img.shields.io/badge/Insightful_Pipe-MCP_Servers-purple)](https://insightfulpipe.com/mcp-servers)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> **Connect Instagram Business accounts to AI assistants for analytics and content management.**

Part of the [Insightful Pipe MCP Server Collection](https://insightfulpipe.com/mcp-servers) — The Instagram MCP server enables Claude, ChatGPT, Cursor, and other AI assistants to analyze your Instagram performance. Monitor engagement, track follower growth, publish content, and get AI-powered content recommendations.

[![Explore All MCP Servers](https://img.shields.io/badge/Explore_All-MCP_Servers-blue?style=for-the-badge)](https://insightfulpipe.com/mcp-servers)

![Instagram MCP Server](https://insightfulpipe.com/images/instagram.svg)

## MCP Server URL

```
https://instagram.insightfulmcp.com/
```

## What is Instagram MCP?

Instagram MCP is a **remote Model Context Protocol server** that connects your Instagram Business or Creator account to AI assistants. This integration allows you to:

- Query Instagram analytics using natural language
- Analyze post, Story, and Reels performance
- Track follower growth and audience demographics
- Publish posts and manage comments

## Installation

### Claude

1. Copy the MCP Server URL: `https://instagram.insightfulmcp.com/`
2. Open [Claude Connectors Settings](https://claude.ai/settings/connectors)
3. Scroll to the bottom and click **Add custom connector**
4. Paste the URL and click **Add**
5. Click **Connect** on the connector to start authorization
6. Click **Authorize access** in the browser to complete the connection

### ChatGPT

Custom MCP servers are added through ChatGPT's **Developer mode**. Availability depends on your ChatGPT plan, and workspace admins may need to allow it.

1. Turn on **Developer mode** in ChatGPT settings
2. Create a new app for a remote MCP server and paste the URL: `https://instagram.insightfulmcp.com/`
3. Authorize with your InsightfulPipe account

See OpenAI's guide: [Developer mode and MCP apps in ChatGPT](https://help.openai.com/en/articles/12584461-developer-mode-and-mcp-apps-in-chatgpt)

### Claude Code

```bash
claude mcp add --transport http instagram https://instagram.insightfulmcp.com/
```

### Cursor

Add the server to `~/.cursor/mcp.json` (all projects) or `.cursor/mcp.json` (one project):

```json
{
  "mcpServers": {
    "instagram": {
      "url": "https://instagram.insightfulmcp.com/"
    }
  }
}
```

Then authorize the connection when Cursor prompts you.

## Available Actions

19 actions: 11 read, 8 write.

### Read Actions (11)

| Action | Description |
|--------|-------------|
| `get_account_insights` | Get account-level insights and analytics |
| `get_business_discovery` | Get profile info and recent public media for another Instagram Business or Creator account by username |
| `get_comment_by_id` | Get details for a specific comment by ID |
| `get_comment_replies` | Get replies to a specific comment |
| `get_media` | List recent media posts for the Instagram account |
| `get_media_by_id` | Get details for a specific media post |
| `get_media_comments` | Get comments on an Instagram media post |
| `get_media_container_status` | Get the processing status for one Instagram media container |
| `get_media_insights` | Get insights for a specific media post |
| `get_profile` | Get Instagram business profile information |
| `get_stories` | List current stories for the Instagram account |

### Write Actions (8)

| Action | Description |
|--------|-------------|
| `create_comment` | Create a new comment on an Instagram media post |
| `create_media_container` | Create exactly one validated Instagram media container |
| `delete_comment` | Delete a comment from Instagram media |
| `hide_comment` | Hide or unhide a comment on Instagram media |
| `publish_media` | Publish exactly one finished Instagram media container |
| `publish_post` | Compatibility action for a complete validated Instagram publish sequence |
| `reply_to_comment` | Reply to a comment on Instagram media |
| `toggle_media_comments` | Enable or disable comments on Instagram media |

## Control What Your AI Can Do

You decide what AI agents can do with each connected account:

- **Turn individual actions on or off** for every connected account, so agents only see the actions you allow.
- **Connect as Read-only or Read & Write.** A read-only connection can only enable read actions.
- **Destructive actions stay off by default.** Actions such as deletes are disabled until an admin enables them.
- **Team access per account.** Restricted team members only use the accounts they are granted, with the read actions enabled on them.

## Usage Examples

### Profile Performance

```
"How is my Instagram performing this week?"
```

### Content Analysis

```
"Which of my Instagram posts got the most engagement this month?"
```

### Audience Insights

```
"What are my Instagram audience demographics?"
```

### Best Posting Times

```
"When are my followers most active on Instagram?"
```

### Publish Content

```
"Publish this image to Instagram with the caption 'New product launch!'"
```

## Supported Instagram Features

- **Feed Posts** - Photo and carousel analytics
- **Instagram Reels** - Short-form video performance
- **Instagram Stories** - 24-hour content insights
- **Profile Analytics** - Account-level metrics
- **Audience Insights** - Follower demographics

## Supported Metrics

| Metric | Description |
|--------|-------------|
| Followers | Total follower count |
| Reach | Unique accounts reached |
| Impressions | Total content views |
| Engagement Rate | Interactions / reach |
| Profile Visits | Profile page views |
| Website Clicks | Link taps |
| Saves | Content bookmarks |
| Shares | Content shares |

## Why Instagram MCP?

### For Content Creators
- **Understand your audience** - Deep demographic insights
- **Optimize content** - Data-driven posting strategy
- **Track growth** - Monitor follower milestones

### For Brands
- **Brand awareness** - Track reach and impressions
- **Engagement monitoring** - Measure audience connection

### For Social Media Managers
- **Content management** - Publish and moderate from AI
- **Automated reporting** - Generate performance reports
- **Client communication** - Easy-to-explain insights

## Security & Privacy

- **Meta Official API** - Instagram Graph API
- **OAuth 2.0** - Secure authentication
- **Granular permissions** - Control read vs write access
- **Business/Creator only** - Personal accounts not supported

## Pricing

The Instagram MCP server is included in every InsightfulPipe plan, together with all other MCP servers and the CLI. Plans start at $29.99/month with a 7-day free trial. See [insightfulpipe.com/pricing](https://insightfulpipe.com/pricing) for current plans.

## Ready-Made Skills and Prompts

- [Instagram Account Performance Overview](https://insightfulpipe.com/marketing-prompts-library/instagram-instagram-account-performance-overview)
- [Instagram Content Performance Analysis](https://insightfulpipe.com/marketing-prompts-library/instagram-instagram-content-performance-analysis)
- [Instagram Reels Strategy Report](https://insightfulpipe.com/marketing-prompts-library/instagram-instagram-reels-strategy-report)

## Explore More MCP Servers by Insightful Pipe

Visit **[insightfulpipe.com/mcp-servers](https://insightfulpipe.com/mcp-servers)** to discover our full collection of MCP servers for marketing and analytics.

### Social Media MCP Servers
- [Facebook Pages MCP](https://insightfulpipe.com/mcp-servers/facebook-pages) - Facebook analytics
- [YouTube MCP](https://insightfulpipe.com/mcp-servers/youtube) - YouTube analytics
- [TikTok Ads MCP](https://insightfulpipe.com/mcp-servers/tiktok-ads) - TikTok marketing

### Advertising MCP Servers
- [Facebook Ads MCP](https://insightfulpipe.com/mcp-servers/facebook-ads) - Meta advertising
- [Google Ads MCP](https://insightfulpipe.com/mcp-servers/google-ads) - Google advertising

**[View All MCP Servers →](https://insightfulpipe.com/mcp-servers)**

## Resources

- [Documentation](https://insightfulpipe.com/docs/connectors-instagram)
- [Video Tutorial](https://www.youtube.com/playlist?list=PLJNzvjxzI5Xwe__BJJLAelSF0ewO3mEFk)
- [InsightfulPipe Blog](https://insightfulpipe.com/blog)

## Support

- **Documentation**: [insightfulpipe.com/docs](https://insightfulpipe.com/docs)
- **All MCP Servers**: [insightfulpipe.com/mcp-servers](https://insightfulpipe.com/mcp-servers)
- **Email**: support@insightfulpipe.com

---

**[Insightful Pipe](https://insightfulpipe.com)** — AI-powered marketing analytics through MCP servers. [Explore all integrations →](https://insightfulpipe.com/mcp-servers)

## License

MIT License - see [LICENSE](LICENSE) for details.
