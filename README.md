# simple-nixns
Simple Linux namespaces bash script

Note: Works best on native Linux. Tested on WSL (Windows 10 > Ubuntu 18.04): results are less than favorable, but it does (barely) work.

## Usage

`initns` is an executable bash script which acts as a simple interface to create and clean namespaces a la `ip netns` commands.

There are 3 modes:

| Mode | Args | Desc |
|:----:|:----:|:-----|
| Default | _no arguments_ | Create 2 namespaces `"nsX"` and link them via `vethX` (where X is the namespace number 1..2). |
| Bridge | `-b N`  | Create N namespaces `"nsX"` plus a bridge `"ns0"`, and connect all namespaces to bridge (where X is the namespace number 1..N). |
| Clean | `-c` | Delete all namespaces. |
