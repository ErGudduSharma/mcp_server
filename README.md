# 🌐 Gemini MCP Server

This repository is designed to integrate and configure **Model Context Protocol (MCP) Servers** for extending automation and agentic capabilities within the VS Code environment, specifically utilizing integrations. Currently, this setup aggregates multiple autonomous MCP servers allowing an AI system/agent to actively execute tasks across various integrated platforms.

## ✨ Supported MCP Servers

By leveraging simple `npx` executions, this configuration exposes three powerful servers:

1. **Browser MCP** (`@browsermcp/mcp`): Enables comprehensive agentic web browsing and browser automation operations.
2. **Airbnb MCP** (`@openbnb/mcp-server-airbnb`): specialized operations linked to Airbnb endpoints and flows.
3. **Flipkart MCP** (`@flipkart/mcp-server`): Integrates E-Commerce interactions localized to Flipkart's features and search parameters.

## 📁 Repository Structure

```
gemini MCP Server/
│
├── .gemini/
│   ├── settings.json       # The core JSON manifest configuring the executing MCP servers
│   └── steps.txt           # Raw textual execution and setup instructions
├── main.py                 # Placeholder script test for Python initialization
└── README.md               # Documentation (this file)
```

## 🛠️ Step-by-Step Installation

### 1. Construct the Configuration Payload
The platform dynamically maps these integrations via a `settings.json` file. Ensure this file exists structurally: `.gemini/settings.json`.
*It should look like this:*
```json
{
  "mcpServers": {
    "browsermcp": {
      "command": "npx",
      "args": ["@browsermcp/mcp@latest"]
    },
    "airbnb": {
      "command": "npx",
      "args": ["-y", "@openbnb/mcp-server-airbnb"]
    },
    "flipkart": {
      "command": "npx",
      "args": ["-y", "@flipkart/mcp-server"]
    }
  }
}
```

### 2. Install the VS Code Extension
To securely bridge the MCP definitions with your workspace, you will need the native VS Code extension.
1. Open Visual Studio Code.
2. Navigate to the **Extensions tab** (`Ctrl+Shift+X` or `Cmd+Shift+X`).
3. Search for the `"browsermcp.io"` extension.
4. Click **Install**.

### 3. Execution & Server Startup
Once constructed and the extension installed, you can trigger the environment to spin up the servers directly from your terminal pane.

1. Open your VS Code integrated Terminal (`Ctrl+` `).
2. Start the protocol wrapper by typing the initialization command: `gemini`.

After initializing, you can run prompts and automate tasks across the three domains (Browsing, Airbnb, Flipkart) organically based on your connected workflow needs.
