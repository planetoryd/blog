# Design of the protocols

> 2021

![](./protocol.drawio.svg)

The diagram shows the general evolution of related projects.

## Arch

![](./arch.drawio.svg)

## Protocols present

- Bitswap with DHT
  - Only works if the blocks are static, immutable, since the records on DHT are not to be changed
- Gossip
  - Not suitable for large amounts of data

![](./proto.drawio.svg)

(An object can't exist without a site)

## Site

![](./s.drawio.svg)

## Object

![](./obj.drawio.svg)

## Encoding

To some specific peer

- Utility rate of the base block by the current block
- Overall utility rate of the base block
  - Possiblity of being required again by other blocks
    - Possibilty of requring the blocks that require the base block
- Difficulty of fetching
  - Size
  - Seeders

![](./enc.drawio.svg)
