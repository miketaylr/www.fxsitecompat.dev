---
title: "`RTCIceCandidateStats` has been updated to the latest spec"
date: "2018-12-12T08:22:00-05:00"
categories: ["audio-video", "dom"]
tags: []
releases: ["65", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1324788"
      title: "Bug 1324788 - Update RTCIceCandidateStats to spec"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1489040"
      title: "Bug 1489040 - WebRTC ICE candidate stats ipAddress needs to be renamed"
---
The implementation of the `RTCIceCandidateStats` dictionary has been updated to the current WebRTC spec. The backward incompatible changes include:

* The deprecated `candidateId` property has been removed.
* The `candidateType` enum members has been renamed. `serverreflexive`, `peerreflexive` and `relayed` are now `srflx`, `prflx` and `relay` respectively.
* The `componentId` property has been removed. The standardized `transportId` property is not yet available in Firefox.
* The `ipAddress` property has been renamed to `address`.
* The [deprecated](https://www.fxsitecompat.dev/en-CA/docs/2018/rtcicecandidatestats-mozlocaltransport-has-been-deprecated/) `mozLocalTransport` property has been renamed to `relayProtocol`.
* The `portNumber` property has been renamed to `port`.
* The `transport` property has been renamed to `protocol`.
