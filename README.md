<div align="center">

[![Total Downloads](https://img.shields.io/github/downloads/CapStash/CapStash-Core/total?label=Total%20Downloads&cacheSeconds=300)](https://github.com/CapStash/CapStash-Core/releases)
[![v27.0.0 Downloads](https://img.shields.io/github/downloads/CapStash/CapStash-Core/v27.0.0/total?label=v27.0.0%20Downloads&cacheSeconds=300)](https://github.com/CapStash/CapStash-Core/releases/tag/v27.0.0)
[![Latest Release](https://img.shields.io/github/v/release/CapStash/CapStash-Core?label=Latest%20Release&cacheSeconds=300)](https://github.com/CapStash/CapStash-Core/releases)

</div>

# ☢️ CapStash Core ☢️

Before there were banks, there were bullets.  
Before there were markets, there was barter.
And after the bombs fell, there were Caps.

In the old world, money was numbers on screens, promises in databases, and paper backed by faith in systems too large to fail.

Then the world failed.

When civilization collapsed, people did what they have always done: they adapted. They traded what held value. Food. Water. Ammunition. Medicine. Tools. Fuel. Information. And, over time, one strange relic of the dead world rose above the rest:

the bottle cap.

It was durable. Recognizable. Difficult enough to fake. Small enough to carry. Useless enough in any other context to gain meaning in this one. In the wasteland, value did not come from governments. It came from trust, scarcity, and survival.

CapStash is that idea reborn for the digital wasteland.

CapStash imagines what the currency of the Fallout universe would become if bottle caps evolved beyond pockets, pouches, and rusted vending trays—if they became programmable, mineable, transferable, and verifiable across a decentralized network built to survive the collapse of the old financial world.

This is not just another cryptocurrency with a recycled codebase and a new logo.

CapStash is a digital bottle cap economy:
- mined instead of minted
- verified instead of trusted
- carried by nodes 
- secured by proof-of-work

If Bitcoin is pristine digital gold, CapStash is something far more rugged:

Money for survivors.

Not polished. Not delicate. Not sterile.  
A currency for scavengers, traders, mechanics, prospectors, bunker lords, signal hunters, and anyone stubborn enough to keep building after the world is supposed to be over.

CapStash Core is the terminal through which that world comes alive.

A full node.  
A wallet.  
A miner.  
A blockchain explorer.  
A retro-futurist machine glowing with phosphor light in the dark.

This is what bottle caps become when the wasteland goes online.

---

## What is a Cap?

A Cap is the base unit of the CapStash network.

Every Cap represents a unit of value secured by a living decentralized system of miners, nodes, and users. Like the physical caps of the wasteland, digital Caps are designed around the same core principles:

- recognizable
- countable
- limited by effort
- useful in trade
- trusted because the network says so, not because a central authority does

In a dead world, value belongs to whatever still works.

Caps still work.

---

## Why Caps?

Because bottle caps were never just a joke.

They were one of fiction’s greatest monetary symbols: absurd at first glance, then strangely perfect the longer you think about them. A bottle cap is small, standardized, portable, and culturally sticky. In Fallout, it became money because people believed in it long enough for it to become real.

CapStash takes that same leap.

It asks a simple question:

What if the wasteland had a blockchain?

What if the currency of survivors wasn’t locked in vaults, controlled by institutions, or printed into meaninglessness—but instead emerged from computation, scarcity, and collective agreement?

What if the bottle cap grew teeth?

---

## CapStash Core

CapStash Core is the reference full-node wallet for the CapStash network.

It is built to feel less like a financial app and more like a machine recovered from the ruins:
- terminal-born
- phosphor-lit
- heavy with atmosphere
- engineered to feel like a working artifact from another timeline

It does not just hold the currency.

It inhabits the world the currency belongs to.

---

## The Idea

CapStash is built on a simple premise:

When the old world dies, money does not disappear.  
It mutates into whatever the survivors trust.

In fiction, that was the bottle cap.

In software, that is CapStash.

## Network Traits

- Proof of Work
- 1 Cap per block
- 1 minute target block time
- transaction fees paid to miners
- built-in miner
- built-in explorer
- custom retro-futurist theme system

## Join Vault 1337

Discord: https://discord.gg/Cs8PRZQb


---

## Stable Source Notice

This repository is intentionally based on the official CapStash Core v27.1.0 tagged source release.

It is intentionally not synced with the latest upstream main branch because newer development commits may not sync blocks correctly on some systems.

This repository is intended to provide a stable and working build target for Ubuntu 22.04 and similar Linux environments.

---

## Build on Ubuntu 22.04

Install dependencies:

    sudo apt update
    sudo apt install -y build-essential libtool autotools-dev automake pkg-config bsdmainutils python3 libevent-dev libboost-system-dev libboost-filesystem-dev libboost-test-dev libboost-thread-dev libsqlite3-dev libminiupnpc-dev libzmq3-dev libqrencode-dev git curl wget gcc-12 g++-12

Clone and build:

    git clone https://github.com/emanwrxsti/CapStash-Core.git
    cd CapStash-Core
    ./autogen.sh
    ./configure --without-gui CC=gcc-12 CXX=g++-12
    make -j$(nproc)

Start daemon:

    ./src/CapStashd -daemon

Check sync:

    ./src/CapStash-cli getblockcount
    ./src/CapStash-cli getnetworkinfo

Optional install system-wide:

    sudo install -m 0755 ./src/CapStashd /usr/local/bin/capstashd
    sudo install -m 0755 ./src/CapStash-cli /usr/local/bin/capstash-cli
    sudo install -m 0755 ./src/CapStash-wallet /usr/local/bin/capstash-wallet
    sudo install -m 0755 ./src/CapStash-tx /usr/local/bin/capstash-tx
    sudo install -m 0755 ./src/CapStash-util /usr/local/bin/capstash-util

## Notes

The generated src/test/fuzz/fuzz binary is intentionally not included because it is only a test/fuzzing artifact and is not required for normal node or wallet operation.

