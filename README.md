# MWR Trophy Tool

**TROPHY TOOL 1.15 — Made by ials96**

A compact Windows trophy tool for Call of Duty: Modern Warfare Remastered 1.15, with a green MWR-style interface, PS4/PS5 selection, automatic debugger reuse, optional LAN Compatibility and guest-player selection.

**[Download v1.0.4 for Windows x64](https://github.com/ials96/MWR-Trophy-Tool/releases/download/v1.0.4/MWR-Trophy-Tool-v1.0.4-win-x64.zip)** · **[Latest release](https://github.com/ials96/MWR-Trophy-Tool/releases/latest)** · **[Discord](https://discord.gg/ZRvVJkc92)**

## Setup

1. Download the ZIP from Releases and extract the complete folder. Keep its supporting files together.
2. Run **Trophy Tool.exe** on a Windows x64 PC. The .NET runtime is included.
3. Open **MWR Multiplayer 1.15** on the modified host console. Select **PS4** or **PS5**, enter that console's IPv4 address and click **Connect**.
4. An already-running compatible debugger is reused automatically, including one started by another tool. If debug is not running, prepare the matching payload receiver first: PS4 GoldHEN on port 9090, or PS5 ELF receiver on port 9021.
5. Leave **LAN Compatibility** off when joining already works. Enable it only when the host lobby does not appear. Its verified preset aligns runtime LAN data to 1511; it does not install an update or reconcile different game content.
6. Start a private LAN match and join it from the other console. Both players must enter the map.
7. Choose the guest under **Target player**, then click **UNLOCK TROPHIES** once. Keep both consoles in the match until processing finishes.
8. Confirm the unlocked trophies and platinum on the guest console. A delivered-request count is not a direct read of its trophy list.

**STOP** cancels the remaining requests after the current request is accounted for. It also interrupts processing pauses.

## What's new in v1.0.4

- Bounded recovery when a normal game message consumes or replaces the staged entry.
- Grouped debugger reads and immediate acknowledgment checks reduce unnecessary waiting.
- Groups of 10 requests, short processing gaps and a final processing period give the console time to handle trophy jobs.
- Match-reset and recipient checks stop delivery when the active session changes.
- Unknown write results, missing acknowledgments and competing trophy senders stop the run instead of being blindly retried.

## Compatibility and validation

- The verified executable profile is **MWR 1.15, CUSA05379**. Unsupported signatures are refused.
- PS4 and PS5 debugger transports are implemented. Live console validation used a PS5 host; PS4 is not claimed as separately live-tested.
- This tool requires an appropriately prepared modified host and a working local connection. It does not jailbreak the console. The guest can remain unmodified.
- **37 automated regression checks passed.** A live run delivered all 50 requests; four remaining locked trophies were subsequently sent with processing gaps, and the tester confirmed all four unlocked and platinum appeared.
- The final batch timing was checked automatically; a complete new live run with that timing has not yet been confirmed. Timing and outcomes can vary, so check the guest console's trophy list.

Logs, settings and LAN backups are stored under `%LOCALAPPDATA%\ials96\MWR Trophy Tool`.

## Files and credits

Release assets include the Windows ZIP and `SHA256SUMS.txt`. The ZIP contains the application, matching debugger payloads, instructions, licenses and corresponding upstream debugger source archives.

See [third-party notices](THIRD-PARTY-NOTICES.txt) for component and artwork credits. Call of Duty, Modern Warfare Remastered and PlayStation belong to their respective owners; no affiliation or endorsement is implied.

**Made by ials96** · [Discord community](https://discord.gg/ZRvVJkc92)
