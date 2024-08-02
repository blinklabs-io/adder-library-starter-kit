# adder-library-starter-kit

This is a starter kit for the Adder library.

This starter kit is an introduction tutorial on how to use the
[adder](https://github.com/blinklabs-io/adder) library to create simple indexer.
Adder communicate with a Cardano Node using the ChainSync protocol.

## Dev Environment using Demeter

For running this starter kit you'll need access to a fully synced instance of a
Cardano Node.

If you do not want to install the required components yourself, you can use the
[Demeter.run](https://demeter.run) platform to create a cloud environment with
access to common Cardano infrastructure. The following command will open this
repo in a private, web-based VSCode IDE with access to a shared Cardano Node.

[![Code in Cardano Workspace](https://demeter.run/code/badge.svg)](https://demeter.run/code?repository=https://github.com/blinklabs-io/adder-library-starter-kit.git&template=golang)

### Cardano Node Access

Since you're running this starter kit from a _Cardano Workspace_, you already
have access to the required infrastructure, such as the Cardano Node.

The network to which you're connected (mainnet, preview, preprod, etc) is
defined by your project's configuration, selected at the moment of creating
your environment.

To simplify the overall process, _Cardano Workspaces_ come already configured
with specific environmental variables that allows you to connect to the node
without extra step. These are the variables relevant for this particular
tutorial:

- `CARDANO_NODE_SOCKET_PATH`: provides the location of the unix socket within
    the workspace where the cardano node is listening.
- `CARDANO_NODE_MAGIC`: the network magic corresponding to the node that is
    connected to the workspace.

### Adder

In this case Adder is using chain-sync Node-to-Client communication to observe all events that happen on blockchain. The example is in a single `main.go` file under `./cmd/adder`.

For `adder`, the default configuration will communicate over the local
UNIX socket mounted at `/ipc/node.socket` via Node-to-Client ChainSync.

Running the code:

```bash
go run ./cmd/adder-publisher
```
