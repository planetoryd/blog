---
title: Rethinking the protocol
date: 2021-02-20 14:32:04
tags:
    - draft
    - dweb
    - diagram
---


# Design of the protocols

> 2021

![](/images/protocol.drawio.svg)

The diagram shows the general evolution of related projects.

## Arch

![](/images/arch.drawio.svg)

## Protocols present

- Bitswap with DHT
  - Only works if the blocks are static, immutable, since the records on DHT are not to be changed
- Gossip
  - Not suitable for large amounts of data

![](/images/proto.drawio.svg)

(An object can't exist without a site)

## Site

![](/images/s.drawio.svg)

## Object

![](/images/obj.drawio.svg)

## Encoding

To some specific peer

- Utility rate of the base block by the current block
- Overall utility rate of the base block
  - Possiblity of being required again by other blocks
    - Possibilty of requring the blocks that require the base block
- Difficulty of fetching
  - Size
  - Seeders

![](/images/enc.drawio.svg)

## To design

The common issues of internet, and its dweb solution

- Data reuse, deduplication
  - IPLD
- Archival
  - Immutability of IPLD
  - Object archival
- Convenience, unification, security
  - Site runtime
- Hyperlink, and beyond it
  - Semantic links
- Code reuse
  - Inter-site reuse, component, template, etc.
  - IPLD (as the way of reusing the code itself)
- Simplicity (of the network itself and the development of applications)
  - IPLD as an alternative to filesystem
  - Less repeating concepts

## Archive

The space and bandwidth of each peer is limited ⇒Archive to save space and bandwidth for the new versions

The bandwidth is saved and the speed of fetching new versions is raised only when the majority have stopped seeding the older versions, and the new version is preferred by the majority ⇒Archival must be done after negotiation at the same time

Archival ⇏ Saving space or bandwidth

- solid compression

