**SSH Workbench** turns your IDE into a place to connect, browse, and **publish** to remote hosts — SSH, a file tree, a terminal, and **Recipes** that replay a release checklist (build, upload, restart, health-check) without leaving the editor.

### Recipes

-   Canvas steps for a publish run: local/remote commands, upload or sync, backup, confirm, notify
-   Pick one or more SSH hosts per remote step; start from a template (Java hotfix, frontend dist)
-   Confirm hosts and paths before Run; follow progress in **Recipe Run**
-   Save under `.ssh/recipes/*.json` so the flow follows Git — hosts as `user@host:port`, passwords only in the IDE PasswordSafe. Importing on another machine creates missing hosts locally

### Connect & terminal

-   Password, key pair, or OpenSSH config (import / export `~/.ssh/config`)
-   Jump hosts (including a chain), HTTP / SOCKS, or the IDE’s own proxy
-   SSH terminal tabs from a saved host
-   One Settings page for SSH hosts and remote servers (a server is a host plus a protocol)

### Files

-   Browse, open, edit; drag-and-drop upload and download
-   **Transfers**: progress, speed, cancel, retry — a folder is one expandable row
-   Search on the server by name, contents, or both; path bar to jump anywhere
-   Sync / compare with local and upload on save (needs a path mapping); overwrite prompt when the remote file is newer

### AI agents

Optional on 2025.2+ with the IDE MCP Server plugin: set up hosts, move files, run commands, type into an SSH terminal, and list / save / run Recipes. Older IDEs omit the tools.

### How to start

**Settings → Tools → SSH Workbench** — add an SSH host, then a remote server that uses it. Open the tree from **Remote Servers**, a terminal from **Tools → Connection to SSH**, or a publish flow from the **Recipes** tool window.

### FTPS tip

If FTPS fails with `522 SSL connection failed session reuse required`, add these lines to the IDE `.vmoptions` file:

-   `-Djdk.tls.useExtendedMasterSecret=false`
-   `-Djdk.tls.client.enableSessionTicketExtension=false`

[GitHub](https://github.com/mbtsp/ssh) · [Issues](https://github.com/mbtsp/ssh/issues)

![demo](https://github.com/mbtsp/ssh/assets/31949635/33656649-d300-46da-a50e-cb9186ccc2fb)

