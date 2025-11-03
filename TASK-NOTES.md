# 🧾 ChameleonUltra — Focused Task Notes (HID / Ultralight / Ultralight EV1 / MIFARE 4K)

This document defines the **target features** for the **ChameleonUltra** fork (USBNinjaRRG) — focused exclusively on **HID, Ultralight, Ultralight EV1, and MIFARE 4K** reading & emulation.

> NOTE: All bounties are indicative and negotiable. Contributors must provide test artifacts (logs / video) and follow the PR checklist.

---

## 🎯 Target Features

| # | Feature | Scope / Deliverable | Est. Price (USD) |
|:-:|:---------|:--------------------|-----------------:|
| 1 | 🔐 **HID Prox** | Implement HID Prox token reading (26 / 37-bit formats) and emulation for common HID standards. Deliver: decode library, emulation command, sample logs, and compatibility tests on multiple readers. | **$220** |
| 2 | 🪪 **Ultralight (NTAG / Ultralight)** | Read and parse NTAG21x / MIFARE Ultralight cards — UID + page memory. Deliver: reader tool, sample dumps, and timing verification on two readers. | **$200** |
| 3 | 🔁 **Ultralight EV1 (Emulation)** | Full emulation of Ultralight EV1 behavior — page read/write, auth (if applicable), and correct NFC timing. Deliver: emulation firmware + demo video showing reader interaction. | **$350** |
| 4 | 🧱 **MIFARE Classic 4K (Read & Simulate)** | Extend existing MIFARE Classic support to 4K (sector layout, Key A/B auth for all sectors, read blocks, and simulation). Deliver: examples + interoperability tests. | **$300** |

💰 **Total Indicative Budget:** **$1,070**

---

## ✅ Acceptance Criteria
- Clean, well-documented code added to correct firmware module.  
- Test logs and video demonstrations included.  
- Compatibility report listing tested readers / locks.  
- Each PR targets a single feature branch (`feature/<short-name>`).  

---

## 🧪 Example Test Cases
- **HID:** Read token → verify facility / ID match; emulate token → open commercial reader.  
- **Ultralight:** Read UID + pages → compare with known dump; detect NDEF if present.  
- **Ultralight EV1:** Emulate EV1 → verify timing and responses with NFC apps / door locks.  
- **MIFARE 4K:** Authenticate and read multiple sectors → emulate UID + sector auth flow.  

---

## ⚙️ Hardware & Toolchain
- **MCU:** nRF52840 (ARM Cortex-M4F with NFC Tag-A)  
- **Toolchain:** nRF SDK / Segger Embedded Studio / Keil  
- **Testing equipment:** HID reader heads, LF antennas, and HF readers (13.56 MHz)  
- **Verification:** smartphone NFC app + 2–3 commercial readers  

---

## 🛠️ PR Checklist
- [ ] Branch named `feature/<short-name>`  
- [ ] Description + test steps in PR body  
- [ ] Demo video / screenshots attached  
- [ ] Serial logs / trace captures included  
- [ ] Compatibility report added  
- [ ] Build passes without warnings  

---

## ⚖️ Legal Notice
This project is for research and interoperability testing only. Contributors must adhere to all applicable laws. Unauthorized cloning or misuse of access credentials is prohibited.

---

## 📇 Contact & Oversight
**Project Owner:** RFID Research Group (RRG)  
**Product Engineer (Overseeing Development):** Ambrose
📧 **Technical Contact:** ambrose@rfidresearchgroup.com  

---

© 2025 RRG – RFID Research Group. All rights reserved.
