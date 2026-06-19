# Nexus Forensics: Digital Evidence Chain of Custody System

**Government-Grade Blockchain Forensics Platform**
*Aligned with Indian Evidence Act (Section 65B) & Global Forensic Standards*

---

## 🏛 Project Overview
Nexus Forensics is a next-generation **Digital Evidence Chain of Custody (CoC) System** designed to solve the critical problem of evidence tampering in judicial processes. Unlike traditional database applications, Nexus employs a **Dual-Ledger Architecture** to guarantee immutability, non-repudiation, and auditability.

### 🔑 Core Value Proposition
-   **Tamper-Proof**: Uses a cryptographic "Permissioned Blockchain" simulation to link every action.
-   **Court-Ready**: Auto-generates legal certificates (Section 65B) and judge-friendly reports.
-   **Secure**: "Military-grade" AES-256 encryption for evidence data at rest.
-   **Smart**: AI detects anomalies (e.g., transfers at 3 AM, custody gaps) in real-time.

---

## 🏗 System Architecture (Dual-Ledger)

The system operates on a unique "Double-Check" principle:

1.  **Fast Access Layer (SQLite Database)**:
    -   Handles UI interactions, search, and relationships.
    -   Stores *Encrypted* evidence metadata (AES-256).

2.  **Immutable Trust Layer (Cryptographic File Log)**:
    -   A permanent, append-only JSON ledger (`ledger.json`).
    -   Every transaction is hashed (SHA-256 + SHA-3) and linked to the previous block.
    -   Acts as the "Ground Truth". If the DB is hacked, this ledger flags the mismatch.

---

## 🛡 Security & Compliance

| Feature | Implementation | Purpose |
| :--- | :--- | :--- |
| **Integrity** | **SHA-256 + SHA-3** | Comparative hashing prevents collision attacks. |
| **Privacy** | **AES-256 (CBC Mode)** | Evidence descriptions/notes are encrypted at rest. |
| **Identity** | **RBAC (Role-Based)** | Enforces strict hierarchy (Investigator > Tech > Admin). |
| **Legal** | **Section 65B Cert** | Auto-drafts compliance certificates for Indian Courts. |

---

## 🚀 Key Features

### 1. Evidence Management (Secure)
-   **Log Evidence**: Capture Audio, Location, and Metadata. 
-   **Encryption**: All sensitive text is encrypted before hitting the disk.
-   **QR Labels**: Generate physical bag tags linked to the digital twin.

### 2. Forensic Dashboard
-   **Integrity Pulse**: Real-time monitor that checks the Dual-Ledger every 10 seconds.
-   **Trust Score**: A dynamic **0-100 rating** for each evidence file based on custody gaps and anomalies.

### 3. "Red Team" Features (Simulation)
-   **Tamper Mode**: A dedicated tool to *intentionally corrupt* the database.
-   **Detection**: Watch the system immediately flag the specific evidence as "COMPROMISED" due to hash mismatch.

### 4. Legal Export
-   **Custody Report**: Plain-English PDF summary for non-technical judges.
-   **65B Certificate**: Formal legal declaration of computer system integrity.

---

## � Tech Stack
-   **Framework**: Next.js 15 (App Router, Server Actions)
-   **Database**: SQLite (via Prisma ORM)
-   **Security**: Node.js Crypto (SHA-3, AES-256)
-   **UI**: Tailwind CSS, Framer Motion, Sonner
-   **PDF Engine**: jsPDF

---

## 🛠 Getting Started

1.  **Install Dependencies**:
    ```bash
    npm install
    ```
2.  **Initialize Database**:
    ```bash
    npx prisma migrate dev --name init
    ```
3.  **Run Development Server**:
    ```bash
    npm run dev
    ```
4.  **Access Portal**:
    Visit [http://localhost:3000](http://localhost:3000)
    -   *Default Login PIN*: `1234`
