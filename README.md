# AO3 Reader

A Visual Studio Code extension for reading public AO3 works in a Webview or in the Output panel.

## Install

Marketplace users only need to install the extension. Node.js, npm, Playwright, and a browser do not need to be installed separately.

To run from source:

```bash
npm ci
npm run compile
```

Open this project in VS Code and press `F5` to launch the Extension Development Host.

To package a VSIX:

```bash
npm run package
```

## Usage

1. Open the Command Palette: press `Ctrl+Shift+P` on Windows/Linux or `Cmd+Shift+P` on macOS.
2. Run `Open AO3 Fanfiction`.
3. Paste a link to an AO3 work or chapter, for example:
   `https://archiveofourown.org/works/1234567/chapters/2345678`
4. Choose **Read in VS Code** or **Pretend to Work in Terminal Mode**.

Content in "Terminal Mode" appears in the **Output** panel, not in the actual terminal.

## Network and Proxy

The extension needs access to `https://archiveofourown.org`. If your network cannot connect to AO3 directly, configure a working proxy, then search for `http.proxy` in VS Code settings and enter the proxy address, for example:

```text
http://127.0.0.1:7890
```

The extension also supports the `HTTPS_PROXY` and `HTTP_PROXY` environment variables. After changing your proxy settings, run `Developer: Reload Window`.

## Limitations

- Supports `/works/<id>` and `/works/<id>/chapters/<id>` links.
- Works that require login are not currently supported.
- If AO3 returns a 403 or 5xx response, or the connection times out, check AO3's status, your network, and your proxy settings.

## Feedback

Please submit a GitHub issue or contact `bluetrainswemissed@proton.me`.

## License

MIT
