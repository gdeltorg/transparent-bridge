# Predictive Transparent Hardware Bridge over IP

This repository contains an original technical paper and a patent-application
draft for a system that extends hardware-facing links over a distance while
preserving the endpoint's native device experience.

## Documents

- [Technical paper](paper.md)
- [Patent application draft](patent-draft.md)
- [Prior-art and evidence index](prior-art.md)

The paper is organized as a submission-ready research proposal: it states
research questions, separates physical/effective/end-to-end/perceived latency,
defines probability and confidence, specifies the bridge architecture and
cross-medium capability graph, and provides a reproducible evaluation and
audit protocol. The patent document is a claim-oriented drafting document;
patent counsel must adapt it to the filing jurisdiction and verify novelty,
inventorship, enablement, and formal requirements before submission.

## Scope

The proposed architecture covers Bluetooth, HDMI, DisplayPort, Wi-Fi, USB and
similar links. It combines local real-time link termination with an IP tunnel,
clock synchronization, predictive pre-transmission, speculative reconstruction,
and correction. Prediction is an optimization for perceived latency; it does
not claim to violate causality or eliminate physical propagation delay.

The design principle is **universal transparent relay**: preserve the native
endpoint experience wherever a medium can be terminated and reconstructed, and
optimize perceived responsiveness so the bridged experience can outperform a
conventional local direct connection whose buffering, interference, codec, or
device processing is worse. This is an engineering target, not a guarantee for
every medium or workload.

The central research question is separated into four layers: whether a
measured physical/effective path can beat a selected local baseline; whether
end-to-end processing can beat it; whether constrained prediction can present
useful output early; and whether users prefer and trust the result. A football
embodiment can show a clearly labelled predicted goal replay on the main
display while a small inset retains the authoritative delayed feed. This is a
testable product hypothesis, not a claim that arbitrary unknown events can be
known in advance.

This repository is a technical disclosure and drafting aid, not legal advice and
not a patent filing. A patent attorney should review claim scope, inventorship,
prior art, enablement, and jurisdiction-specific formal requirements.
