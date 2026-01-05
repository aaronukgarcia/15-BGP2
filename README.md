# Sovereign Routing Infrastructure (SRI)

**A Five-Layer Hardware-Integrated Architecture for Securing Inter-Domain Routing**

| Document Details | |
| :--- | :--- |
| **Author** | [cite_start]Aaron Garcia (Independent Researcher) [cite: 6] |
| **Date** | [cite_start]January 2026 [cite: 8] |
| **Current Version** | [cite_start]2.1 (Red Team Revision) [cite: 20] |
| **Status** | [cite_start]**Open for Public Comment / Discussion** [cite: 3] |

---

## 📢 Request for Comments (RFC)

[cite_start]**This document is explicitly "Open for Comment."** [cite: 19]

Unlike a finalized standard, this is a research proposal intended to stimulate discussion within the network security community. We are actively seeking feedback on the following areas:

* [cite_start]**Validator Governance:** Critiques of the proposed "Swiss Association" legal structure and liability caps[cite: 454, 464].
* [cite_start]**Consensus Protocol:** Feedback on the TLA+ specifications for the Routing Authority Consensus (RAC)[cite: 553].
* [cite_start]**Economic Modeling:** Alternative perspectives on the "Negative NPV" financial analysis and incentive structures[cite: 321].

**How to Comment:**
* Open an **Issue** for specific technical flaws or questions.
* Submit a **Pull Request** for errata or clarification.
* [cite_start]Contact the author directly for private feedback: `aaron@garcia.ltd`[cite: 603].

---

## 📖 Abstract

[cite_start]The Border Gateway Protocol (BGP) remains fundamentally vulnerable to route hijacking and path manipulation[cite: 10]. [cite_start]Current standards (RPKI, ASPA) provide limited defense against nation-state adversaries or supply chain attacks[cite: 11].

[cite_start]**Sovereign Routing Infrastructure (SRI)** is a vendor-agnostic architecture designed to complement RPKI[cite: 12]. [cite_start]It integrates hardware security with distributed consensus to address these advanced threats while maintaining backward compatibility[cite: 13, 14].

## 🏗️ Architecture Overview

[cite_start]SRI implements a defense-in-depth strategy across five distinct layers[cite: 13]:

1.  [cite_start]**Hardware Root of Trust:** TPM 2.0 integration for unforgeable platform identity[cite: 128].
2.  [cite_start]**Microkernel Foundation:** Formally verified seL4 kernel for component isolation[cite: 134].
3.  [cite_start]**Secure Enclaves:** Route computation within TEEs (Intel TDX, ARM TrustZone)[cite: 141].
4.  [cite_start]**Distributed Consensus:** A "slow" consensus layer for authority attestation, separate from "fast" packet validation[cite: 144].
5.  [cite_start]**BGP Extensions:** New transitive path attributes for carrying security attestations[cite: 152].

---

## ⚠️ Critical Analysis (v2.1)

[cite_start]This repository hosts **Version 2.1**, which incorporates findings from a rigorous "Red Team" analysis[cite: 20]. It explicitly acknowledges:

* [cite_start]**Financial Reality:** A likely negative Net Present Value (NPV) over 15 years; deployment is not justified on ROI alone[cite: 321].
* [cite_start]**Governance Risk:** A "Fragility Score" of 72%, driven by the difficulty of coordinating competitor ISPs and RIRs[cite: 546].
* [cite_start]**Performance Degradation:** Validation latency spikes from ~360μs (cache hit) to 50-200ms (cache miss)[cite: 181].

---

## 📄 License

This project is licensed under the **MIT License**. This means you are free to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the software and documentation, provided the original copyright notice is included.

[cite_start]**Copyright (c) 2025 Aaron Garcia** [cite: 668]

> Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
>
> The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.
>
> THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. [cite_start]IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE. [cite: 669, 670]