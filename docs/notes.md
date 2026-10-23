# Notes and Brainstorm

**Raw thinking behind the concept. Not a specification, not a roadmap.**

---

## The swarm model

Four flagship smartphones in a dock, connected over Wi-Fi 6/7, orchestrated as a small local swarm.

- **Compute:** phones use their CPU and GPU. NPU access is not exposed to external orchestration.
- **Storage:** shared NVMe SSD in the dock. Phones read and write through the dock.
- **Network:** Wi-Fi 6/7 between phones and dock. Ethernet is not available on phones.
- **Cooling:** active airflow through the dock. Low-RPM 200 mm fans, ducted channels.

The swarm is meant for **light and bursty workloads**: local RAG over documents, background indexing, photo processing, small model inference. Not for sustained heavy compute.

---

## Security module (luxury tier idea)

A physical key for encrypted storage in the dock.

- **Secure Element** (e.g., ATECC608) inside the dock holds the decryption key for the SSD.
- Phones in the dock can access the encrypted volume.
- Phones removed from the dock lose access. The data stays encrypted.
- An **NFC card** can serve as a physical key: tap the card to unlock the volume.

**Why this is not Knox or Secure Enclave:**

- Knox Vault and Secure Enclave are **inside the phone**. They protect the phone's own keys and biometrics.
- An external Secure Element protects **the dock's SSD**, not the phones.
- Android and iOS do not allow an external device to manage the phone's hardware keys.

**What it is good for:**

- Separating storage from devices: the SSD lives in the dock, the key lives in the dock, the phones are just clients.
- A physical ritual: tap a card to unlock. For a luxury audience, ritual is part of the value.
- A clear security boundary: if a phone is lost, the dock's data is still protected.

**What it is not good for:**

- Protecting the phones themselves.
- Replacing the phone's own secure hardware.
- Working without the physical key.

---

## Honest limits

1. **Thermal throttling.** Flagship SoCs lose 40–50% of peak performance under sustained load, even with external cooling. The dock delays throttling; it does not eliminate it.
2. **No NPU access.** Android and iOS do not expose the neural accelerator to external orchestration. The swarm runs on CPU/GPU paths.
3. **Cost.** Four flagship phones cost more than six to eight single-board computers. The dock only makes sense as a brand accessory.
4. **Fragile orchestration.** OS updates, battery health, and vendor policies make long-term stability unpredictable.
5. **Security module is limited.** It protects the dock's SSD, not the phones.

---

## Why a brand might still build it

- **Ecosystem lock-in.** A dock that only works with the brand's phones strengthens the ecosystem.
- **Premium accessory revenue.** A luxury dock is a high-margin accessory for flagship owners.
- **Visible local AI.** The dock makes on-device AI physically visible on a desk.
- **NPU orchestration testbed.** A controlled environment for multi-device AI experiments.

---

## Open questions

- Could a brand expose NPU access to its own dock through a private API?
- Could thermal design inside the phone be adjusted for sustained load in docked mode?
- Would users accept a physical NFC key as part of the ritual?
- Is the dock a product, a prototype, or a marketing object?

These questions are not answered here. They are the reason the concept stays archived.
