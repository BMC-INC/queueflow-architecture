# QueueFlow · Architecture Explorer

An interactive explanation of the QueueFlow webhook pipeline: device events pass through verification and policy evaluation before actions are dispatched and recorded.

[Explore the architecture](https://bmc-inc.github.io/queueflow-architecture/)

## What you can explore

Select any of the four stages to see its role in the system:

1. **Event source** — device events enter the pipeline.
2. **Ingress and verification** — signature checks, deduplication, and normalization establish the input boundary.
3. **Policy evaluation** — configured thresholds, windows, and cooldowns determine when an action should run.
4. **Action dispatch and audit** — matched actions and their outcomes are recorded.

This repository is a standalone architecture presentation, not the QueueFlow application or a deployable webhook service. Its animation is illustrative; it does not connect to Ring devices, process live events, or establish the current production configuration. Product implementation and operations are maintained separately.

## Run locally

The explorer is a single HTML file with embedded CSS and JavaScript. No dependencies, account, API keys, or build step are required.

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open [localhost:8000](http://localhost:8000). Click a stage, or focus it with `Tab` and press `Enter` or `Space`, to expand its details. Select it again to close it. The layout adapts to narrow screens and respects reduced-motion preferences.

## Maintain the presentation

The `stages` array in [`index.html`](index.html) contains the stage titles, descriptions, and icons. Keep the explanation consistent with the implementation, and avoid adding customer data, device identifiers, or operational credentials. GitHub Pages publishes this repository's site.

Report presentation defects through [GitHub Issues](https://github.com/BMC-INC/queueflow-architecture/issues).

## Reuse

No repository-wide open-source license is currently included. This public presentation does not grant a general reuse license or include the separately maintained product source.
