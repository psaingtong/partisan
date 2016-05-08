Partisan
=======================================================

[![Build Status](https://travis-ci.org/lasp-lang/partisan.svg?branch=master)](https://travis-ci.org/lasp-lang/partisan)

Partisan is a prototype and primarily used in experiments.  This is not
meant for production use.

Partisan is still full membership and under active development (for now!).

* Single node testing, facilitated by a disterl control channel for figuring out which ports the peer service is operating at.
* Designed to be compatible with the Lasp fork of Basho's plumtree implementation.
* Messages are sent via TCP connections that are maintained to all cluster members.
* Failure detection is performed TCP.
* Connections are verified at each gossip round.
* Configurable fanout.
* On join, gossip is performed immediately, instead of having to wait for the next gossip round.
* Prototype HyParView implementation.

Partisan has two peer services:

* Full membership with TCP-based failure detection: `plumtree_default_peer_service_manager.`
* HyParView, hybrid partial view membership protocol, with TCP-based failure detection: `plumtree_hyparview_peer_service_manager.`
