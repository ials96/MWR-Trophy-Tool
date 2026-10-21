# Changelog

## v1.0.5 — 2026-10-21

### Fixed

- Fixed **Invalid process mapping** during PS4 connection when ps4debug-NG returns one completely empty leading map record. The empty metadata record is excluded; all actual mappings still undergo the original range validation.
- Existing build, private-LAN, recipient and write checks remain in place. PS5 behavior and trophy-processing timing are unchanged.

### Validation and update

- 46 automated regression checks passed, including replay of the affected PS4 response and rejection of other malformed mappings.
- The affected PS4 tester confirmed successful connection after the fix, as reported by the tool author.
- Download and extract the complete v1.0.5 Windows x64 ZIP. This release does not add an automatic updater. The application version is v1.0.5; the supported game remains MWR Multiplayer 1.15.

## v1.0.4

- Added bounded recovery for verified normal game-message contention.
- Grouped debugger reads and checked acknowledgments immediately to reduce unnecessary waiting.
- Added groups of 10 requests with processing gaps and a final processing period.
- Retained session/recipient checks and stopped on uncertain writes, missing acknowledgments or competing trophy senders.
