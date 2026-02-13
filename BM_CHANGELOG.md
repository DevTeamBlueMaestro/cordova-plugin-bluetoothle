# Blue Maestro BLE Plugin Optimizations

## Changelog

### v0-baseline (Phase 1)
- Forked from randdusing/cordova-plugin-bluetoothle v6.7.4
- No code changes — baseline for bmLogger compatibility testing
- Branch: bm-optimizations

### v1-connection-priority (Phase 2)
- **Android**: Automatic `CONNECTION_PRIORITY_HIGH` on device connection
- Reduces connection interval from ~50ms to ~11.25ms
- Speeds up service discovery and initial read/write operations
- API 21+ (Lollipop) with backward-compatible version check
- Priority reverts automatically when the system deems appropriate
- File changed: `src/android/BluetoothLePlugin.java` (line ~4189)

### Planned Phases
- **Phase 3**: Native scan filtering for Blue Maestro devices
- **Phase 4**: Background scanning improvements (state restoration, duty cycling)
