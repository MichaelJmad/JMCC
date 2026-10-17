# JMAD Media Control Center (JMCC)
### High-Performance Desktop Media Organizer & Library Orchestrator

[![Latest Release](https://img.shields.io/github/v/release/MichaelJmad/JMCC?color=00e5ff&label=Release&style=flat-square)](https://github.com/MichaelJmad/JMCC/releases)
[![Platform](https://img.shields.io/badge/Platform-Windows%2010%20%7C%2011-blue?style=flat-square)](https://github.com/MichaelJmad/JMCC/releases)
[![Architecture](https://img.shields.io/badge/Architecture-x64-indigo?style=flat-square)](https://github.com/MichaelJmad/JMCC/releases)
[![License](https://img.shields.io/badge/License-Proprietary%20%2F%20Closed%20Source-red?style=flat-square)](#license--distribution)

**JMAD Media Control Center (JMCC)** is a specialized, hardware-accelerated desktop workstation application engineered to automate the intake, metadata reconciliation, physical file reorganization, collision-safe multi-drive movement, and long-term curation of large home media libraries.

Built on a decoupled multi-database architecture with SQLite, hardware media stream probing via FFprobe, and a reactive Electron/React user interface, JMCC bridges raw, chaotic download folders with standardized home theater software (Plex, Jellyfin, Kodi, Emby).

---

<!-- IMAGE PLACEHOLDER: HERO_BANNER -->
> *Placeholder: Application Hero Banner / Dashboard Overview Screenshot*
<!-- END IMAGE PLACEHOLDER -->

---

## 🚀 Core Modules & Capabilities

### 1. 📥 Staging & Organize Studio
The Staging subsystem serves as the entry gate for raw media downloads and unorganized file archives.

* **Dual-Stage Decoupled Workflow**: Physical folder organization in staging is strictly separated from library transfer. Files are organized, standardized, probed, and inspected locally in staging before committing any movements to production library drives.
* **Organize Studio**:
  * **Interactive Slot Matrix**: A 40-season target assignment pane with 1-to-1 slot uniqueness invariant and automatic slot conflict swapping.
  * **Intelligent Title & Fluff Stripper**: Dynamically extracts clean series titles, cour groupings, release groups (`{group}`), and season/episode numbers while neutralizing release years and multi-part tags.
  * **Movie Extraction & Disambiguation**: Wizard to separate companion anime films, OVAs, and specials into dedicated movie staging trees or multi-part structures (`.part1.mkv`, `.part2.mkv`).
  * **Multi-Provider Artwork Acquisition**: Browse and download master posters, subsidiary posters, and episode thumbnails directly from AniList and TMDB.
  * **Automated Kodi/Jellyfin NFO Generation**: Emits standardized `tvshow.nfo`, `movie.nfo`, and `<episode>.nfo` files with complete stream specs and plot summaries.
* **Non-Blocking Clutter Pruner**: Scans and isolates `.nfo.bak`, `.txt`, sample clips, empty directories, and junk files with safe trash routing and dry-run preview.

<!-- IMAGE PLACEHOLDER: STAGING_ORGANIZE_STUDIO -->
> *Placeholder: Staging Module & Organize Studio Screenshot*
<!-- END IMAGE PLACEHOLDER -->

---

### 2. 🏛️ Library & Tactile Collection Browser
The Library subsystem maintains authoritative custody of your permanent media collection across any number of internal, external, or networked drives.

* **Multi-Drive Architecture**: Transparently monitors multiple library roots across separate drives (e.g., `E:\Anime`, `M:\Anime`, `D:\TV Shows`, `F:\Movies`) without forcing unified symlinks or mergerfs setups.
* **High-Density Tactile Cards**:
  * Formatted premier air dates, total runtimes, and storage metrics (Size on Drive).
  * Video resolution badges (4K UHD, 1080p FHD, 720p HD) and audio stream codec pills.
  * Dual-Audio & English Dub indicators powered by canonical MyDubList and AniList synchronization.
  * Health & Diagnostics badge with glassmorphic discrepancy popovers.
* **Expanded Series Inspection Drawer**:
  * **Expected Episodes Matrix**: Identifies missing episodes across all seasons using provider episode manifests.
  * **Physical Duration Pipeline**: Live container runtimes extracted via FFprobe (`24m`, `48m`, `1h 22m`).
  * **Franchise Relations Graph**: Visual tree of sequels, prequels, side stories, and parent series with instant library markers.
  * **2:3 Portrait Recommendations Grid**: Visual suggestions with rating overlays and 1-click Wishlist acquisition.

<!-- IMAGE PLACEHOLDER: LIBRARY_BROWSER -->
> *Placeholder: Library Grid & Tactile Card Inspection Screenshot*
<!-- END IMAGE PLACEHOLDER -->

---

### 3. ⚖️ Multi-Drive Pre-Flight Collision Engine
Safeguards your library against accidental overwrites and lost episodes when moving items from Staging to Library.

* **Side-by-Side Stream Inspector**: Compares colliding episodes side-by-side: container formats, video codecs, vertical resolutions, audio channels, and physical file sizes.
* **Complementary Merge Logic**: Merges non-colliding episodes seamlessly while adopting existing database entity IDs and preserving disk structures.
* **Non-Blocking Asynchronous Streaming**: Win32 cross-drive transfers utilize streamed chunk copying with CRC/size verification before source pruning, eliminating UI lockouts or operating system freezes.

<!-- IMAGE PLACEHOLDER: COLLISION_WIZARD -->
> *Placeholder: Side-by-Side Collision Resolution Wizard Screenshot*
<!-- END IMAGE PLACEHOLDER -->

---

### 4. 📋 Tag-Based Wishlist & Auto-Fulfillment
A centralized radar for tracking wanted series, missing seasons, upcoming air dates, and media quality replacements.

* **Dynamic Taxonomy Filters**: Filter across `Get List`, `On Hold`, `Backlog`, and `Needs Fixed`.
* **Automated Acquisition Sweeper**: Background monitor automatically matches incoming library additions against Wishlist provider IDs and marks items as fulfilled.
* **Format-Agnostic Import Wizard**: Supports batch pasting of plain text titles, AniList XML/JSON exports, and JWIS RFC-2026-09 wishlist data files.
* **Condition Evaluator**: Customizable rule engine (e.g., trigger download when English dub airs, or when Blu-ray version releases).

<!-- IMAGE PLACEHOLDER: WISHLIST_MODULE -->
> *Placeholder: Wishlist Kanban & Item Cards Screenshot*
<!-- END IMAGE PLACEHOLDER -->

---

### 5. 🔍 Visual Cross-Provider ID Enrichment Studio
Eliminates fragmented external metadata by unifying provider IDs into a consolidated database record.

* **Human-in-the-Loop Visual Verification**: Compares suggested matches from AniList, TMDB, MyAnimeList (MAL), and TVDB side-by-side with original posters, plot synopses, and release years before applying.
* **Season-Level ID Persistence**: Stores granular provider IDs at the season level, solving multi-cour and split-season metadata desyncs.
* **Permanent Rejection Memory**: Rejection ledger ensures dismissed false positives are never re-scouted.

<!-- IMAGE PLACEHOLDER: ENRICHMENT_STUDIO -->
> *Placeholder: Provider ID Enrichment Studio Review Board Screenshot*
<!-- END IMAGE PLACEHOLDER -->

---

### 6. 💻 Live Diagnostics Console & Telemetry Bus
Built-in developer tools and system observability for continuous health monitoring.

* **Real-Time Log Streamer**: Filter logs instantly across `INFO`, `WARN`, `ERROR`, and `TELEMETRY`.
* **Pop-Out Standalone Window**: Detach the console into an independent desktop window for dual-monitor debugging.
* **One-Click Diagnostic Export**: Copies formatted JSON/text stack traces directly to the OS clipboard.

<!-- IMAGE PLACEHOLDER: DIAGNOSTICS_CONSOLE -->
> *Placeholder: Live Diagnostics Console Tray & Pop-out Window Screenshot*
<!-- END IMAGE PLACEHOLDER -->

---

## 💾 Installation & Distribution

JMCC is distributed exclusively as compiled 64-bit Windows executables.

| Distribution Type | Asset Name | Description |
| :--- | :--- | :--- |
| **Setup Installer** | `JMCC Setup <version>.exe` | Recommended for desktop integration, start menu shortcuts, and automatic updates. |
| **Portable Executable** | `JMCC-<version>-win-x64.exe` | Zero-install standalone executable; ideal for USB drives or sandbox testing. |
| **ZIP Package** | `JMCC-<version>-win-x64.zip` | Standalone archive with all required application binaries. |

### Download Links
Releases can be downloaded directly from the official [Releases](https://github.com/MichaelJmad/JMCC/releases) page.

### Update Channels
JMCC supports two release channels configurable inside **Settings ➔ General**:
* **Stable (Recommended)**: Thoroughly tested and verified production builds.
* **Pre-Release / Beta (Tester Channel)**: Early-access release candidates (`-RC`) featuring the latest experimental modules and optimizations.

---

## 🖥️ System Requirements

* **Operating System**: Windows 10 (64-bit) or Windows 11 (64-bit).
* **Processor**: Modern x64 multi-core processor (Intel Core i3 / AMD Ryzen 3 or higher recommended for fast media probing).
* **Memory**: 4 GB RAM minimum (8 GB recommended for libraries with 5,000+ files).
* **Storage**: 500 MB free space for the application and database caches.
* **Filesystems**: NTFS, ReFS, exFAT, and SMB/NFS network shares.

---

## 🛠️ Getting Started

1. **Launch Application**: Run the installer or double-click the portable executable.
2. **Configure Storage Roots**:
   * Navigate to **Settings ➔ Directories**.
   * Add one or more **Staging Roots** (where new downloads arrive).
   * Add one or more **Library Roots** (permanent storage for Anime Series, TV Shows, Movies).
3. **Scan Staging**: Go to **Staging** and click **Scan Staging** to discover incoming folders.
4. **Organize**: Click **Organize** on any series card to open the Organize Studio, link metadata, and align episodes.
5. **Move to Library**: Click **Move to Library** to run the preflight collision check and execute safe transfer.

---

## 🔒 License & Closed-Source Distribution

JMAD Media Control Center (JMCC) is a proprietary, closed-source project developed by MichaelJMAD.
All rights reserved.

* Source code is not public.
* Binaries, release packages, and documentation are provided free of charge for personal home media curation.
* For bug reports, feature requests, or tester feedback, please submit an issue via the [GitHub Issue Tracker](https://github.com/MichaelJmad/JMCC/issues).
