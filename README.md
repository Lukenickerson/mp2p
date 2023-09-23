# mp2p - A Minimal P2P WebRTC Library 
***Communicate browser-to-browser without a signaling server, without dependencies***

Based on: https://github.com/xem/miniWebRTC

## How does it work?

* A STUN server is contacted to get some information about your browser's "address" on the internet.

* The WebRTC API (specifically [RTCPeerConnection](https://developer.mozilla.org/en-US/docs/Web/API/RTCPeerConnection)) is used to create a *peer connection*.

* Peers need to communicate long strings of data in some way -- email, text, chat, etc. -- in order to make the connection. These strings contain the [SDP (SessionDescription Protocol)](https://developer.mozilla.org/en-US/docs/Glossary/SDP) information that describes the peer-to-peer connection.

* After these long strings are traded back and forth, the peers are connected, and may trade data (chat, files, audio, video).

## Goals

* Be small -- so it can be easily read and understood, and also so it could be used in game jams such as js13k
* No dependencies -- no external libraries
* No signaling server or third-party server, other than the necessary STUN servers
