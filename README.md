# AI Module Cyberpunk

**A brand concept for a luxury smartphone swarm dock. Designed for flagship devices from Google, Apple, or Samsung. Not a product.**

---

## What this is

A dock that holds **four flagship smartphones** and connects them into a small local swarm over Wi-Fi 6/7. The dock provides active cooling, shared NVMe storage, power delivery, and an optional security module for encrypted data.

The design is deliberately luxury: brushed aluminium, amber accent lighting, fine mesh, no visible screws. It is meant to sit on a desk in a studio, a private office, or a collector's shelf — not in a server room.

This repository is a record of the idea. It is not planned for prototyping, funding, or production.

---

## Who it is for

This concept is addressed to **flagship brands**, not to individual makers:

- **Google** — a dock for Pixel devices, positioned as a "local AI companion" for Tensor-powered phones.
- **Apple** — a dock for iPhone Pro, positioned as a "private compute extension" for Apple Intelligence.
- **Samsung** — a dock for Galaxy Ultra, positioned as a "Knox-protected swarm" for secure local workloads.

The dock is a **brand accessory**, not a third-party gadget. It carries the brand's design language and extends the brand's ecosystem.

---

## Why a brand would consider it

- **Ecosystem lock-in.** A dock that only works with the brand's phones strengthens the ecosystem.
- **Premium accessory revenue.** A luxury dock is a high-margin accessory for flagship owners.
- **A visible statement of local AI.** The dock makes the brand's on-device AI strategy physically visible on a desk.
- **A testbed for NPU orchestration.** The dock gives the brand a controlled environment to experiment with multi-device AI workloads.

---

## Why it is not a product today (honest reasons)

1. **Thermal throttling is unavoidable.** Flagship SoCs lose 40–50% of peak performance under sustained load, even with external cooling. A brand could engineer around this, but it would require custom thermal design inside the phone, not just the dock.
2. **No direct NPU access.** Android and iOS do not allow an external device to use the phone's neural accelerator as a general-purpose compute resource. A brand could open this API for its own dock, but it would be a platform decision, not an accessory decision.
3. **Cost.** Four flagship phones cost more than six to eight single-board computers. The dock only makes sense as a brand accessory, not as a standalone product.
4. **Security module is limited.** An external Secure Element protects the dock's SSD, not the phones. A brand could integrate it with its own secure enclave, but that requires platform-level cooperation.
5. **Fragile orchestration.** OS updates, battery health, and vendor policies make long-term swarm stability unpredictable outside a controlled brand ecosystem.

---

## Visuals

- `1780913527270 (1).png` — dock with four phones, airflow channels, single power cable
- `1780913590968.png` — open rack with phones on stands, fans below
- `1781255302424.png` — bench prototype with mini-PC, microphone, screen, power banks
- `1781256270020.png` — server-room variant with multiple mini-PCs and cable management

---

## Status

| Field | Value |
|---|---|
| Stage | Brand concept |
| Revision | v0.1 |
| Build intent | None |
| Audience | Flagship brand R&D, not individual makers |
| Reason | Kept for record: the idea is interesting as a brand accessory, not as a standalone product |

---

## See also

- [`docs/notes.md`](docs/notes.md) — brainstorm notes and honest limits (coming next)
