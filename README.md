# Hey, I'm Joe

I'm a SOC Analyst with a background in cybersecurity, networking, endpoint support, and hands-on infrastructure.

My personal technical work is centered around a homelab that has grown into a household infrastructure and operations platform. I use it to run real services, support family workflows, test architectural decisions, and practice the kind of troubleshooting that only appears after a system is used over time.

I care less about collecting tools and more about understanding how systems behave across virtualization, Linux, containers, networking, applications, and the people using them.

## Featured Project

### [Homelab Infrastructure Portfolio](https://github.com/Joegamer1/homelab-infrastructure-portfolio)

This repository documents my actual homelab: what I built, why the architecture changed, what failed along the way, how I isolated problems, and how I validated the resulting fixes.

The environment is built around:

- Dell Precision T7820 hardware
- Proxmox VE virtualization
- A Debian Docker service host
- A dedicated Home Assistant OS VM
- Tailscale private remote access
- Pi-hole internal DNS
- Uptime Kuma monitoring
- Homepage service navigation
- Plex and automated media services
- Donetick-backed household chore workflows
- Google Calendar and work-schedule visibility
- Configuration-focused backup planning

## What Makes the Project Different

The project began as a traditional homelab and media-server build. It gradually became infrastructure that my household actually uses.

That changed the engineering priorities.

A technically correct calendar event still needed redesign when an overnight shift confused the person reading it. A visible chore integration still needed an API bridge when it could not create the recurring, assigned tasks the household needed. A functional dashboard still needed refinement when default controls were too large or exposed the wrong workflow.

The portfolio documents those iterations instead of showing only the polished result.

## Selected Engineering Work

### Proxmox and Docker Infrastructure

- Rebuilt and updated the Proxmox virtualization host.
- Created a lightweight Debian VM as the primary Docker platform.
- Troubleshot QEMU Guest Agent communication and VM configuration.
- Deployed and operated infrastructure, monitoring, DNS, dashboard, media, and household services.
- Inspected live bind mounts and named volumes instead of assuming tutorial paths matched the running environment.

### Plex Hardware Transcoding

- Enabled Intel IOMMU on Proxmox.
- Identified and bound NVIDIA GPU functions to `vfio-pci`.
- Passed a Quadro P620 through to the Debian VM.
- Configured NVIDIA access inside the Plex container.
- Preserved the working runtime and library configuration through Docker Compose.
- Diagnosed Direct Play, Direct Stream, video transcoding, and audio-only transcoding separately.

### Home Assistant Household Operations

- Built a family-facing dashboard rather than exposing a default administration layout.
- Integrated Google Calendar for shared schedule visibility.
- Created detailed and simplified calendar entities for overnight work shifts.
- Built Donetick-backed daily and weekly recurring chore creation through Home Assistant.
- Added assignment, helper reset, completion feedback, and targeted Card Mod styling.
- Refined the interface based on actual household feedback.

### Operations and Recovery

- Created configuration-focused backup archives for important Docker services.
- Inventoried real storage locations across bind mounts and named volumes.
- Added Docker metadata, logging, timestamps, and retention.
- Kept restore testing explicitly marked as incomplete until it is actually performed.

## How I Approach Problems

My normal troubleshooting pattern is:

1. Verify the actual running state.
2. Identify which layer owns the failure.
3. Inspect live configuration, mounts, entities, playback details, or network paths.
4. Change one meaningful variable at a time.
5. Validate the result through the layer closest to the original problem.
6. Preserve the working configuration.
7. Document what remains uncertain or incomplete.

I am especially interested in problems where the first technically valid answer is not the best operational answer.

## Technical Areas

- Security operations
- Proxmox virtualization
- Linux administration
- Docker and Docker Compose
- Home Assistant
- REST API integration
- Private remote access
- DNS and service networking
- Monitoring and operational visibility
- GPU passthrough and media delivery
- Backup and recovery planning
- User-focused automation
- Defensive security workflows

## Current Direction

My main goal is to keep developing the homelab into a clear professional portfolio that demonstrates:

- Real infrastructure ownership
- Cross-layer troubleshooting
- Security-minded architecture
- Operational judgment
- Honest validation and limitations
- Documentation discipline
- The ability to build systems that other people can use successfully

Cybersecurity-specific labs such as SIEM deployment, detection engineering, attack simulation, and incident writeups will remain separate projects built on top of this infrastructure foundation.

---
