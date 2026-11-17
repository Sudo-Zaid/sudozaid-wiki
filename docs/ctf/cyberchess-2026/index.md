# CyberChess 2026 — Writeups

Solved challenges from the **CyberChess** CTF (flag format `HTB{...}`). Each page is a short writeup: challenge info, the flag, and how I found it.

## :trophy: Result

!!! success ":goat: Team Wargaye :flag_pk: — 4th / 96 teams — Full clear 49/49 flags — 13,800 points"
    Every challenge on the board cracked and captured.

| Metric | Value |
|--------|------:|
| **Team ranking** | **4th / 96** |
| **Flags** | **49 / 49** |
| **Points** | **13,800** |
| **First bloods** | **3** |
| **CTF date** | 10–11 Oct 2026 |

**Writeups documented: 18** across Pwn, Reversing, Crypto, Web, Forensics, OSINT, ICS, AI and Quantum.

| # | Challenge | Category | Difficulty | Key technique |
|---|-----------|----------|------------|---------------|
| 01 | [Operation Phantom Runner](01-operation-phantom-runner.md) | OSINT | Easy | Entities hard-coded in client JS bundles |
| 02 | [Locker](02-locker.md) | Reversing | Medium | Androguard decompile, fixed AES-256 key |
| 03 | [pump it](03-pump-it.md) | Crypto | Hard | SHA-512 hash length extension |
| 04 | [twisted cloud](04-twisted-cloud.md) | Crypto | Hard | PHP `mt_rand` seed brute-force |
| 05 | [MetroControl](05-metrocontrol.md) | ICS | Medium | S7Comm DB write, XOR auth key leak |
| 06 | [Siren](06-siren.md) | Web | Medium | Blind RCE via `$(...)` + `${IFS}` |
| 07 | [Shard Council](07-shard-council.md) | AI | Medium | LLM PIN leak + prompt-injection SSRF |
| 08 | [Phase Phantom](08-phase-phantom.md) | Quantum | Hard | Kitaev phase estimation + ML fit |
| 09 | [Perimeter Zero](09-perimeter-zero.md) | Pwn | Insane | Heap overflow → tcache → ROP ORW |
| 10 | [GHZ Collapse](10-ghz-collapse.md) | Quantum | Hard | Signed-GHZ stabilizer readout |
| 11 | [Controlled Meltdown](11-controlled-meltdown.md) | AI | Hard | Adversarial sensor spoofing vs RPS |
| 12 | [SmartBridge](12-smartbridge.md) | ICS | Insane | SSRF → stolen mTLS → cEMI passthrough |
| 13 | [The Debug Door](13-the-debug-door.md) | Forensics | Medium | AWS CloudTrail log correlation (21/21) |
| 14 | [Unfinished Business](14-unfinished-business.md) | Forensics | Hard | Volatility 3 + AES key carve |
| 15 | [Gradient Heist](15-gradient-heist.md) | AI | Medium | Gradient leakage from a zeroed param |
| 16 | [Final Key](16-final-key.md) | Pwn | Medium | Stack overflow → ret2libc |
| 17 | [WeakLink-2](17-weaklink-2.md) | ICS | Medium | OPC UA auto-trust → recipe write |
| 18 | [Dash Rush](18-dash-rush.md) | Web | Easy | pg-promise `--` type confusion |

## Categories

Pwn · 2 &nbsp;|&nbsp; Reversing · 1 &nbsp;|&nbsp; Crypto · 2 &nbsp;|&nbsp; Web · 2 &nbsp;|&nbsp; Forensics · 2 &nbsp;|&nbsp; OSINT · 1 &nbsp;|&nbsp; ICS · 3 &nbsp;|&nbsp; AI · 3 &nbsp;|&nbsp; Quantum · 2

!!! note
    All flags use the `HTB{...}` format. Entries 1–7 are from the main event; 8–18 were cracked in follow-up sessions (quantum, adversarial-ML, ICS, cloud/memory forensics and pwn) — all flags captured.

---

> These writeups were written by **Claude Code**, from screenshots and content provided by **Muhammad Zaid**.
