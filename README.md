# Outstand MCP plugin

Connect Cursor and Grok Bot to [Outstand](https://www.outstand.so), the unified social media API.
Publish and schedule social posts, upload media, read engagement metrics, and manage connected social accounts using natural language.

This package connects to the hosted MCP server at `https://mcp.outstand.so/mcp` over Streamable HTTP.
It contains no executable code, dependencies, API keys, or local server to run.

## Connect

1. Create an [Outstand account](https://www.outstand.so/app/signup) if you do not already have one.
2. Install the Outstand plugin from the marketplace once its listing is approved.
3. Choose the connector's authentication action, sign in to Outstand, and select the organization to authorize.
4. Connect the social accounts you want to use in your Outstand dashboard.
5. Enable or attach Outstand to your conversation and describe the task.

The plugin uses OAuth with PKCE. Each user signs in to their own Outstand account and chooses their organization.
There is no shared credential and no API key to place in the plugin configuration.

Before marketplace approval, a compatible client can connect directly with the same server URL using its custom MCP connector settings.
For Cursor, this is also the configuration in `mcp.json` in this repository.

## Example prompts

- "List my connected social accounts and upcoming scheduled posts."
- "Prepare a draft of this announcement for LinkedIn, Facebook, and Threads."
- "Schedule this approved Instagram post for tomorrow at 9am in Europe/Stockholm."
- "Show me how my latest LinkedIn post performed."
- "Upload this image and attach it to a draft post."

## Capabilities and requirements

Outstand supports publishing, scheduling, post updates, analytics, comments and replies, media uploads, and social account management.
See the maintained [tool reference](https://www.outstand.so/docs/mcp/tools) and [supported platforms](https://www.outstand.so/docs/mcp).
Capabilities and metrics vary by social platform, account type, permissions, and platform restrictions.

Publishing and analytics require social accounts connected by the user. X, Google Business Profile, Vimeo, and Reddit require
user-supplied platform developer credentials. Managed credentials are available for other supported networks;
Bluesky uses an app password. See the [platform configuration guides](https://www.outstand.so/docs/configurations).

The plugin has no separate fee. Outstand usage remains subject to the user's plan, quotas, and platform rate limits.
It has no payment tools. See [Outstand pricing](https://www.outstand.so/#pricing).

## Access and data

The connector can read organization data and perform write actions, including publishing or deleting posts and managing account connections.
Use it only with accounts you are authorized to manage. Review the destination accounts, content, media, and schedule before approving writes.
Use drafts when preparing content for review.

The package itself does not collect telemetry or store credentials. The client connects directly to Outstand's hosted service.
Authentication and service data are handled under the [Outstand Privacy Policy](https://www.outstand.so/privacy)
and [Terms of Service](https://www.outstand.so/terms).

## Support

- [MCP setup and troubleshooting](https://www.outstand.so/docs/mcp/setup)
- [Full MCP documentation](https://www.outstand.so/docs/mcp)
- Email: support@outstand.so

## License

The plugin configuration and documentation are licensed under the MIT License. Outstand's name and logo identify the service;
the license does not grant trademark rights. Use of the hosted Outstand service is governed by its own terms.
