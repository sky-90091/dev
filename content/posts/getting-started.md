---
title: "Getting Started"
date: 2018-01-18T17:43:53+08:00
---

Our setup consists of Following main components:

* Skycoin [Node](https://github.com/skycoin/skycoin) itself and its command line utilities

* Skycoin [Teller](https://github.com/skycoin/teller)

---

# Quick Start

Both the node & teller are developed in [Go](https://golang.org/doc). In order to proceed, you must have a developer environment [ready](https://golang.org/doc/install).

---

## Skycoin Node:

This is a full Skycoin Node on the network. It downloads & stores the full chain on disk. It is used for sending signed transactions to the network and verify transactions.

Command Line tools interact with the node over JSON-RPC.

### Download the Code

```
go get github.com/skycoin/skycoin/...
```

### Install Node

```
cd $GOPATH/src/github.com/skycoin/skycoin/
cd cmd/skycoin; go install
```

Then `skycoin -h` to see the command-line options. The node can be now be started

```
skycoin
```

Note, that on first start & all subsequent starts, the node will connect to peers & download remaining blocks. The storage size is however quite modest ( 41 M as of Jan 18).

The node makes a web-ui available on http://localhost:6420/.

### Client [Reference](https://github.com/skycoin/skycoin/blob/develop/cmd/cli/README.md)

The client interacts with the node over JSON-RPC.

```
cd $GOPATH/src/github.com/skycoin/skycoin/
go run cmd/cli.go
```

---

## Teller

The Teller is OTC exchange that can be used to exchange BTC and ETH for Skycoin. Getting started should be familiar

### Download the Code

```
go get github.com/skycoin/teller/...
```

### Install Teller

```
cd $GOPATH/src/github.com/skycoin/teller/
cd cmd/teller; go install
```

Then `teller -h` to see the command-line options. The teller can be now be started

```
teller
```

Teller's web-ui is available on http://localhost:7071/.

Further setup is required in order to get the teller connected with the Skycoin, Bitcoin & Ethereum nodes.

---

Please refer to the README in corresponding [Teller](https://github.com/skycoin/teller) and [Skycoin](https://github.com/skycoin/skycoin) for further details.

---
