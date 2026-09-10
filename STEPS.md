# WebMCP Bridge Extension + Chrome DevTools Quickstart

## Prerequisites

- Node.js 18+
- pnpm (`npm i -g pnpm`)
- Chrome / Chromium
- Claude Code (optional)

---

## 1. Build & Install WebMCP Bridge Extension

```bash
# Clone (or download release zip)
git clone https://github.com/agentcathq/webmcp-react.git
cd webmcp-react/extension

pnpm install
pnpm build
```

### Load in Chrome

1. Open `chrome://extensions`
2. Enable **Developer mode**
3. Click **Load unpacked**
4. Select the `extension/dist` folder

Pin the extension. Icon starts gray until activated on a tab.

**Easier alternative:** Install [WebMCP Bridge](https://chromewebstore.google.com/detail/webmcp-bridge/chgjbookknohehmaocfijekhaocaanaf) from the Chrome Web Store.

### Connect to Claude Code

```bash
claude mcp add --transport stdio webmcp-server -- npx webmcp-server
```

---

## 2. Build & Run the Demo

```bash
git clone https://github.com/WebMCP-org/chrome-devtools-quickstart.git
cd chrome-devtools-quickstart
npm install
npm run dev
```

Demo runs at **http://localhost:5173**

### Add Chrome DevTools MCP (for Claude Code)

```bash
claude mcp add chrome-devtools npx @mcp-b/chrome-devtools-mcp@latest
```

### Test

Ask Claude:

> Navigate to http://localhost:5173, list available WebMCP tools, and set the counter to 42

Demo tools:
- `get_page_title`
- `get_counter`
- `set_counter`

---

## Quick Reference

| Step | Command / Action |
|------|------------------|
| Build extension | `cd extension && pnpm install && pnpm build` |
| Load extension | Load `extension/dist` in `chrome://extensions` |
| Run demo | `npm install && npm run dev` |
| Claude MCP (bridge) | `claude mcp add --transport stdio webmcp-server -- npx webmcp-server` |
| Claude MCP (devtools) | `claude mcp add chrome-devtools npx @mcp-b/chrome-devtools-mcp@latest` |


# See also

https://agentcat.com/guides/connect-webmcp-tools-claude-code-bridge-extension/

https://grok.com/share/bGVnYWN5_49646c98-ffc8-451b-8041-7ec3c6511724


https://docs.nekuda.ai/