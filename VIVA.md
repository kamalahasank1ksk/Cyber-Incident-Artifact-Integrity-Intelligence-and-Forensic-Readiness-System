# 🎓 Final Year Project: VIVA / Interview Guide
**Project:** Digital Evidence Chain of Custody System

---

## 🚀 1. Problem Statement (The "Why")
**Simple Explanation:**
Digital evidence (images, videos, logs) is fragile. It can be **copied, modified, or replaced** without leaving visible traces.
In legal systems (like local courts), this creates trust issues:
*   *Was it altered?*
*   *Who accessed it?*
*   *When?*

**Our Solution:**
We replaced manual/editable records with a **Blockchain-backed System** that ensures evidence history is **Immutable (Unchangeable), Verifiable, and Auditable**.

---

## 🛠️ 2. Core Technology Stack
| Tech | Purpose | Why? |
| :--- | :--- | :--- |
| **SHA-256 Hashing** | Integrity Verification | Creates a unique digital fingerprint. Even a 1-bit change alters the hash completely. |
| **Blockchain Ledger** | Tamper-Proof Record | Stores the Hash + Timestamp + Handler ID. No single authority can delete history. |
| **Smart Contracts** | Logic Enforcement | *Simulated logic* ensures only the current custodian can transfer evidence. |
| **Next.js & Node.js** | Full-Stack App | Modern, fast, and scalable interface for officers. |
| **SQLite (Prisma)** | Off-Chain Storage | Stores the actual metadata efficiently, while the *proof* lives on the ledger. |

---

## 🏗️ 3. System Data Flow
1.  **Capture**: Officer uploads file (e.g., crime scene photo).
2.  **Hash**: System computes `SHA-256` hash immediately.
3.  **Ledger**: Hash + Metadata is written to the Blockchain.
4.  **Transfer**: Custody handover requires **PIN Verification** & RBAC checks.
5.  **Verify**: At any time, re-hashing the file compares it to the original block.

---

## ✅ 4. Key Features Implemented
1.  **Evidence Registration**: Upload & Hash generation.
2.  **Chain of Custody**: Immutable timeline of every transfer.
3.  **Secure Handover**: PIN-protected transfers between officers.
4.  **Integrity Pulse**: Visual blockchain health monitor.
5.  **AI Anomaly Detection**: Highlights suspicious gaps/patterns (Bonus Feature).
6.  **Interactive Dashboard**: Real-time charts and audit logs.

---

## 🚫 5. Limitations (Scope Awareness)
*   **No National Integration**: Not connected to real court servers (Academic Scope).
*   **Simulated PKI**: Digital signatures are simulated for the demo.
*   **Local Storage**: Evidence files are stored locally, not on IPFS (for speed/simplicity).

---

## 🎙️ 6. The "One-Liner" Summary
> "We used cryptographic hashing for integrity, blockchain for immutability, and role-based access control to build a verifiable digital evidence system that prevents tampering and ensures accountability."

---

## 🔮 7. Future Scope
*   Integration with Government PKI (Digital Signatures).
*   Deployment on Hyperledger Fabric (Private Consortium Blockchain).
*   Automated Legal Certificate Generation (Section 65B).
