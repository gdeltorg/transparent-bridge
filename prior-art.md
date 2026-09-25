# Prior-art and evidence notes

This is a research index, not a patentability or freedom-to-operate opinion.
The sources below establish adjacent techniques; they do not by themselves
prove novelty of the combined architecture.

| Area | Reference | Evidence | Difference from this proposal |
|---|---|---|---|
| Transparent peripheral over IP | Hirofuchi et al., “USB/IP - a Peripheral Bus Extension for Device Sharing over IP Network,” USENIX FREENIX, 2005 | [USENIX](https://www.usenix.org/legacy/events/usenix05/tech/freenix/hirofuchi.html) | USB-focused; no multi-medium prediction graph |
| Transparent peripheral over IP | Hirofuchi et al., “USB/IP: A Transparent Device Sharing Technology over IP Network,” IPSJ, DOI [10.2197/ipsjdc.1.394](https://doi.org/10.2197/ipsjdc.1.394) | Peer-reviewed transparent USB sharing | No synchronized A-to-B/B-to-A speculative correction |
| Prediction and correction | “Latency Reduction in CloudVR: Cloud Prediction, Edge Correction,” arXiv [2410.01898](https://arxiv.org/abs/2410.01898) | Cloud prediction/edge correction research | Rendering-focused, not native hardware-link bridging |
| Cloud media transport | “Nebula: Reliable Low-latency Video Transmission for Mobile Cloud Gaming,” arXiv [2201.07738](https://arxiv.org/abs/2201.07738) | Measured low-latency cloud gaming transport | Does not expose arbitrary native endpoint media |
| Perceptual optimization | “Foveated Video Streaming for Cloud Gaming,” arXiv [1706.04804](https://arxiv.org/abs/1706.04804) | Gaze-aware QoE optimization | Foveation rather than protocol-transparent bridging |
| Live service measurement | “Network Anatomy and Real-Time Measurement of Nvidia GeForce NOW Cloud Gaming,” arXiv [2401.06366](https://arxiv.org/abs/2401.06366) | Real-world latency/QoE measurements | Measurement baseline, not a bridge architecture |
| Product practice | NVIDIA Reflex, GeForce NOW, Xbox Cloud Gaming, Meta ASW, NVIDIA DLSS Frame Generation | Commercial prediction/scheduling/frame synthesis | Vendor products; claims and configurations require independent measurement |

## What must be tested rather than assumed

The proposal treats “remote is better than local” as a measurable hypothesis.
For each medium, publish:

- exact local and remote endpoints and observation points;
- propagation/effective transport, device processing, end-to-end, and perceived
  latency as separate values;
- clock source, route, bandwidth, packet loss, jitter, and queue policy;
- prediction horizon, confidence, coverage, exact/error rate, and correction
  rate;
- p50/p95/p99 and worst-case results;
- independent replay from immutable source and prediction logs.

A remote path may beat a particular local device or local configuration. That
does not establish that every remote path beats every local path, and it does
not justify conflating physical propagation with codec, buffering, display, or
speaker processing latency.

