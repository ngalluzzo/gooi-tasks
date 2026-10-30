# Gooi Tasks

**One list, shared by you and your assistant.** A local task board with an interactive MCP App view.

[Get Gooi Tasks](https://gooi-tasks.blueflame14.chatgpt.site) · [Downloads](https://github.com/ngalluzzo/gooi-tasks/releases) · [Privacy](https://gooi-tasks.blueflame14.chatgpt.site/privacy.html)

## Easiest installation

The current early-access release supports **Mac with Apple Silicon**.

1. Download the `.mcpb` file from the latest release.
2. Open it with Claude Desktop or another compatible MCPB host.
3. Review the extension and click **Install**. If double-clicking does not open an installer, add the file through the host's extension settings.
4. Ask **“Open my Gooi tasks.”** Then try **“Add a task to plan the weekend.”**

No terminal, JSON editing, API key, Gooi account or additional runtime is required. The host's account and plan requirements are separate. MCP Apps support enables the interactive checklist; tools remain useful as text in other compatible local hosts.

This early-access bundle and its executable are **unsigned and not notarized**. Your OS or host may block them. Signing, additional platforms, directory distribution and automatic updates are still pending. There is no Windows, Linux or Intel Mac desktop download in this release.

## Portable installation

Download and extract the `.tar.gz` archive to a permanent folder. From that folder:

```sh
./gooi-tasks --print-config
```

Add the resulting `gooi-tasks` entry to your host's MCP configuration and reconnect. Hosts with another configuration format need the same `command` and `args`. Your host must support launching local stdio MCP servers; this release is not a remote connector for cloud-only hosts.

To use the included real MCP Apps preview without an assistant:

```sh
./gooi-tasks --preview --port 0
```

Open the address it prints. The preview's advanced controls simulate assistant tool calls through the actual MCP server.

## Data, updates and removal

Your SQLite board lives at `~/Library/Application Support/Gooi/tasks/`, outside the installation folder. The native app connects to no external service. Task inputs/results pass through your chosen assistant host under its privacy policy. The public download page cannot access your installed board.

Stop the app before replacing the executable or updating the extension, then reconnect. Removing the extension keeps the board. Delete the data directory separately, with all instances stopped, if you want to erase it. Use `GOOI_TASKS_DATA_DIR` to select another absolute data directory.

You can add, complete/reopen and filter tasks. The first release supports 500 tasks and has no cloud sync or deletion. Use Refresh for changes from another local instance.

Each release includes `SHA256SUMS` and `release.json`. Checksums verify bytes; they are not publisher signatures. Do not treat an unsigned release as signed simply because its checksum matches.

This repository distributes app releases and support information. It does not contain the full Gooi development source. Third-party license notices accompany each download. Report problems through Issues without including private task contents.
