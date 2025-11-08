
# Browser MCP Server Setup

A complete setup for running Multiple MCP (Model Context Protocol) servers including Browser MCP, Airbnb, and Flipkart servers in VS Code.

## 🚀 Features

- **Browser MCP**: Web browsing automation and interaction
- **Airbnb MCP**: Airbnb platform operations and data
- **Flipkart MCP**: Flipkart e-commerce operations

## 📋 Prerequisites

- [Node.js](https://nodejs.org/) (v16 or higher)
- [Visual Studio Code](https://code.visualstudio.com/)
- Gemini CLI or compatible AI assistant

## 🛠️ Installation

### Step 1: Clone or Create Project Structure
```bash
mkdir browser-mcp-setup
cd browser-mcp-setup
Step 2: Create Configuration Directory
bash
mkdir .gemini
Step 3: Create Configuration File
Create .gemini/settings.json with the following content:

json
{
  "mcpServers": {
    "browsermcp": {
      "command": "npx",
      "args": ["@browsermcp/mcp@latest"]
    },
    "airbnb": {
      "command": "npx",
      "args": [
        "-y",
        "@openbnb/mcp-server-airbnb"
      ]
    },
    "flipkart": {
      "command": "npx",
      "args": [
        "-y",
        "@flipkart/mcp-server"
      ]
    }
  }
}
Step 4: Install VS Code Extension
Open VS Code

Go to Extensions (Ctrl+Shift+X)

Search for "browsermcp.io"

Install the Browser MCP extension

🎯 Usage
Starting the Servers
Open terminal in VS Code (Ctrl+` )

Run the command:

bash
gemini
Available MCP Servers
🌐 Browser MCP
Web page navigation

Content extraction

Form interactions

Screenshot capture

Automated browsing

🏠 Airbnb MCP
Property search

Booking information

Price comparisons

Location data

🛒 Flipkart MCP
Product search

Price tracking

Order management

E-commerce operations

📁 Project Structure
text
browser-mcp-setup/
├── .gemini/
│   └── settings.json
└── README.md
⚙️ Configuration Details
Browser MCP
Package: @browsermcp/mcp

Command: npx @browsermcp/mcp@latest

Features: Automated web browsing and interaction

Airbnb MCP
Package: @openbnb/mcp-server-airbnb

Command: npx -y @openbnb/mcp-server-airbnb

Features: Airbnb platform integration

Flipkart MCP
Package: @flipkart/mcp-server

Command: npx -y @flipkart/mcp-server

Features: Flipkart e-commerce integration

🔧 Troubleshooting
Common Issues
Node.js not found

Ensure Node.js is installed and added to PATH

Verify installation: node --version

npx command not working

Update npm: npm install -g npm@latest

Clear cache: npm cache clean --force

Extension not loading

Restart VS Code after installation

Check extension is enabled

MCP servers not connecting

Verify internet connection

Check firewall settings

Ensure all dependencies are installed

Verification Steps
Check Node.js installation:

bash
node --version
npm --version
npx --version
Test MCP server installation:

bash
npx @browsermcp/mcp@latest --help
📝 Notes
The -y flag in Airbnb and Flipkart servers automatically confirms prompts

MCP servers run locally on your machine

Ensure you have stable internet connection for server operations

Some features may require additional authentication

🔒 Security Notes
MCP servers run with the permissions of your user account

Be cautious when granting browser automation permissions

Review the source of MCP packages before installation

🤝 Contributing
Feel free to submit issues and enhancement requests!

📄 License
This project is setup for educational and development purposes.

