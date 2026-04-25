# InsightfulPipe MCP for Antigravity

MCP server configuration for connecting Antigravity to InsightfulPipe.

## Requirements

- Node.js 18 or newer (`node --version` to verify)

## Installation

1. Copy the config for your operating system:

   | OS | File |
   |---|---|
   | macOS | [`mcp_config.macos.json`](./mcp_config.macos.json) |
   | Windows | [`mcp_config.windows.json`](./mcp_config.windows.json) |
   | Linux | [`mcp_config.linux.json`](./mcp_config.linux.json) |

2. Place it at:
   - macOS / Linux: `~/.gemini/antigravity/mcp_config.json`
   - Windows: `%USERPROFILE%\.gemini\antigravity\mcp_config.json`

   If the file already contains other servers, merge the `insightfulpipe` entry into the existing `mcpServers` object.

3. In Antigravity, open **Manage MCPs** and click **Refresh**, or restart the application.

## Verification

`insightfulpipe` should appear in **Manage MCPs** with a connected status and available tools.

## Notes

- **Intel Macs:** replace `/opt/homebrew` with `/usr/local` in the macOS config.
- **nvm users:** the bundled paths assume system or Homebrew Node. Replace `command` with the output of `which npx` (macOS / Linux) or `where npx` (Windows), and update `env.PATH` to include the directory containing `node`.

## Troubleshooting

| Error | Cause | Fix |
|---|---|---|
| `exec: "npx": executable file not found in $PATH` | Antigravity cannot locate `npx` | Set `command` to the absolute path from `which npx` / `where npx` |
| `env: node: No such file or directory` | `npx` runs but cannot locate `node` | Add the directory containing `node` to `env.PATH` |
| Server connects but tools fail | Authentication or workspace issue | Verify access to https://main.insightfulmcp.com |

## Supported Platforms

Facebook Ads, Google Ads, Microsoft Ads, LinkedIn Ads, Pinterest Ads, Google Analytics, Search Console, PageSpeed Insights, Klaviyo, Mailchimp, Facebook Pages, Instagram, LinkedIn Pages, Google Business Profile, Magento, Apple App Store, Google Play, Google Sheets, site crawler, ad transparency libraries, company enrichment.
