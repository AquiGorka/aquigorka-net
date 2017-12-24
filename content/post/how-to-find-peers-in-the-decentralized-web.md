+++
categories = []
date = "2017-12-24T10:23:08+02:00"
tags = []
thumbnail = "/images/2017/12/decentralised.jpg"
title = "How to find peers in the decentralised web"

+++

# The Decentralised Paradigm & Problem



The decentralized web refers to an Internet where no central authorities take responsibility to provide features/processes/services for Internet apps to work.

This solves the issue of such central authorities being able to store user profile information and preferences and monetize on such data.

But a problem arises: how are peers going to find each other in such decentralized network?

## The solutions

### Using a central server

This kind of defeats the purpose of the decentralized web, but in reality what is needed from this servers is that they act as places where users find each other to connect.

To do so, this servers need to:

- Be publicly available from well known/static address
- Provide hig availabilityand uptime
- Understand the different protocols to let clients connect to each other once they find each other

Open source servers:

- [Signalhub](https://github.com/mafintosh/signalhub)
- [Easy SSB Pub](https://github.com/staltz/easy-ssb-pub)
- [PeerJS Server](https://github.com/peers/peerjs-server)
- [Peer Chord Signaler](https://github.com/oxyflour/simple-peer-chord)
- [WebRTC Explorer](https://github.com/diasdavid/webrtc-explorer)


### Other solutions

#### Using DHT with WebRTC to find peers.


From [js-ipfs](https://github.com/ipfs/js-ipfs):

> DHT (automatic content discovery) and Circuit Relay (pierce through NATs and dial between any node in the network) are two fundamental pieces that are not finalized yet. There are multiple applications that can be built without these two services but nevertheless they are fundamental to get that magic IPFS experience.

This is an ongoing proposal, not quite ready for prime time but a lot of minds are trying to figure this one out:

- https://github.com/webtorrent/webtorrent/issues/288
- https://github.com/hallettj/bitable
- https://github.com/maxogden/discovery-channel
- https://github.com/mafintosh/discovery-swarm
- https://github.com/mappum/peer-exchange

The following repo provides an example to create a namespaced peer-network via the DHT:

- https://github.com/mafintosh/peer-network

## References

- https://github.com/kgryte/awesome-peer-to-peer
- https://www.html5rocks.com/en/tutorials/webrtc/infrastructure/
- https://github.com/diasdavid/webrtc-connect


## P2P & Fun Experiments

- https://github.com/substack/swarmlog
- https://github.com/mafintosh/hyperirc
