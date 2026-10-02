# DepoVaultTick

**One private Android app for a family's money, memory and work.**

Built In DART CODE

DepoVaultTick keeps a household's financial records, daily expenses, notes, secrets and work paperwork in one place, entirely on the phone and behind its own locks. It warns the owner in **red** and **yellow** before anything matures, falls due or expires.

> This repository contains plain-English documentation of the app. The source code is not published here.

---

## At a Glance

| | |
|---|---|
| **Project type** | Personal app, designed, built and documented end to end by one developer |
| **Platform** | Android |
| **Built with** | Flutter and Dart |
| **Data** | Offline-first: everything stays on the device, with no accounts and no cloud |
| **Scale** | 5 main sections, 6 dashboards, about 77 source files and 91,000 lines of Dart |
| **Protection** | Three-secret App Lock, separate Stash Lock, optional biometrics, password-encrypted backups |

---

## The Problem

Important household details are scattered: fixed-deposit receipts in a drawer, insurance premiums remembered by habit, Post Office passbooks in a bag, SIP dates in a bank app, certificates that quietly expire and passwords in a notebook. Nothing shows what is coming up across all of it, and missing one date can cost money or cover.

## The Solution

One app, five sections, a single combined alert list, and one consistent set of colour-coded warnings.

| Section | What it gives the user |
|---|---|
| **Family & Vault** | Per-person tracking of bank deposits (fixed and recurring), insurance, Post Office schemes and mutual funds, with maturity and due-date warnings and family-wide dashboards |
| **Daily Log** | An expense register, a bill and reminder board, and a calendar that also shows what is coming up in every other section |
| **Notes** | A corkboard of coloured sticky notes with real text formatting |
| **Stash** | A small private safe for passwords and PINs, behind its own lock |
| **Work** | A timesheet-to-PDF invoice generator, a contact book, and a certificate tracker with expiry reminders |

---

## Feature Highlights

- **Never miss a date.** A notification bell combines every date-based item into six periods: Today, Tomorrow, Next 7 Days, This Month, This Quarter and Missed.
- **Red means act now, yellow means due soon.** The most severe colour rolls up from one deposit to its bank, the person, the whole family and the Home logo.
- **See the whole family at once.** A rotating "Next Up" panel and four financial dashboards, with two more for daily expenses and invoices. Every dashboard exports to Excel or CSV.
- **Private by design.** No servers. An App Lock that asks for one of three different secrets at random, plus a separate Stash Lock.
- **Take your data with you.** Encrypted backups with a choose-what-to-include checklist, and a guided restore with a side-by-side conflict review.
- **Built for daily life and work.** Rich-text sticky notes, a five-step invoice wizard, and a certificate tracker with nested folders.

---

## Engineering Highlights

| Challenge | Approach |
|---|---|
| Totals that never go stale | Totals, statuses and due dates are recomputed from raw facts every time rather than stored |
| Paused SIP plans | Stopped months are skipped when counting, and the whole schedule shifts later |
| Dashboards drifting from the real rules | Dashboards call the same shared status functions as the main screens |
| Bell and list disagreeing | Home uses a lightweight check that mirrors the exact rules of the bell's tabs |
| Shoulder-surfing a PIN | Three secrets set up together, one asked at random, a reshuffled keypad and a five-try lock-out |
| Merging a backup safely | Conflicts are shown side by side, and Save stays disabled until each one has a decision |
| Rich text in a plain text box | Text is stored as short styled "runs" that join back into the exact sentence |
| Overnight shifts | An end time that isn't later than the start is rolled into the next day |

The full table is in the [Project Highlights](DepoVaultTick_Project_Highlights.pdf) document.

---

## Documentation

### Start here

| Document | Covers |
|---|---|
| [Project Highlights](DepoVaultTick_Project_Highlights.pdf) | The product story, feature highlights and engineering decisions |
| [00 · App Overview](00_DepoVaultTick_Overview.pdf) | The whole app on one page, with a map of every section |

### Foundations

| Document | Covers |
|---|---|
| [01 · Setup & Startup](01_Setup_and_Startup.pdf) | Packages, Android build, theme and splash screen |
| [02 · Home Screen](02_Home_Screen.pdf) | The hub, badges, bell and backup buttons |
| [03 · Notifications & Alerts](03_Notifications_and_Alerts.pdf) | The six-period alert list and the red / yellow warning system |
| [04 · App Lock & Privacy](04_App_Lock_and_Privacy.pdf) | The three-secret lock, biometrics, privacy settings and About |

### Family & Vault

| Document | Covers |
|---|---|
| [05 · Family & Banks](05_Family_and_Banks.pdf) | People, banks and the family-wide view |
| [06 · Deposits](06_Deposits.pdf) | Fixed and Recurring Deposits and their dashboard |
| [07 · Insurance](07_Insurance.pdf) | Policies, premiums, maturities and their dashboard |
| [08 · Post Office](08_Post_Office.pdf) | Savings schemes and their dashboard |
| [09 · Mutual Funds](09_Mutual_Funds.pdf) | SIPs, lump sums and their dashboard |

### Everyday sections

| Document | Covers |
|---|---|
| [10 · Daily Log](10_Daily_Log.pdf) | Expenses, reminders, calendar and dashboard |
| [11 · Notes](11_Notes.pdf) | The sticky-note corkboard |
| [12 · Stash](12_Stash.pdf) | The private secrets keeper and its own lock |

### Work tools

| Document | Covers |
|---|---|
| [13 · Work: Invoices](13_Work_Invoices.pdf) | The invoice wizard, saved invoices and billing dashboard |
| [14 · Work: Rolodex & Certificates](14_Work_Rolodex_and_Certificates.pdf) | Contacts and certificate tracking |

### Data and shared parts

| Document | Covers |
|---|---|
| [15 · Backup, Export & Import](15_Backup_Export_and_Import.pdf) | Encrypted backups, merge-and-review restore, Excel, CSV and PDF output |
| [16 · Shared Building Blocks](16_Shared_Building_Blocks.pdf) | Storage, sound, pickers and common components |

---

## Technology

Flutter and Dart with Material 3 styling, targeting Android. Data is held in on-device storage behind one central service. The app generates PDF, Excel and CSV files, uses encryption and hashing libraries, and relies on the phone's own biometric system and Share menu.

---

## Notice

These documents are provided **for understanding purposes only, not for commercial or teaching use.** No license is granted to copy, redistribute or reuse the contents.

© 2026 Prasanaa Kartick T. All rights reserved.
