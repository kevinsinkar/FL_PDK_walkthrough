# FlexLogger UI Screenshots Needed (Phase 2)

This folder is reserved for **live FlexLogger application screenshots** that the
"Block Diagram ↔ FlexLogger UI" tab will reference for hotspot calibration.

The `assets/fl-user-manual/` folder already contains documentation-style
screenshots scraped from the NI online User Manual. Those work as fallbacks,
but the UI surfaces below benefit from clean, current captures from a live
FlexLogger session because they need to highlight specific clickable zones
that don't show clearly in the doc-cropped images.

Each capture below should be:
- Taken at 100% display scaling on a desktop monitor
- 1080p or higher source resolution
- Cropped to show only the relevant surface (no unrelated panels)
- Saved as PNG with a descriptive kebab-case filename

## Required captures

### 1. `channel-spec-full.png`
**Surface:** Channel Specification panel (left pane in FlexLogger).
**Must show:** at least one Display Group heading, 2+ channel rows under it,
the Name column, Unit column, Data Type icon column, Enabled checkbox column,
and the Configure gear icon hover state on a row.
**Suggested setup:** Add the Mouse Input plug-in (or any sample) and capture
the channel table with the plug-in expanded.

### 2. `plugin-properties-dialog-full.png`
**Surface:** Plug-in Properties / Configuration dialog (top-level).
**Must show in one frame:** a Boolean checkbox, a DBL numeric field, an I32
integer field, a String text field, an Enum dropdown, a Single-Channel
selector, an N-Channel selector, **and** a Command button. If no single
plug-in exposes all of these, build a demo plug-in that does — this is the
canonical reference for "Where does Write Parameter end up?"

### 3. `per-channel-properties-pane.png`
**Surface:** Per-channel Properties pane (right side / channel detail dialog
shown when a channel row is selected).
**Must show in one frame:** Boolean, DBL, I32, String, Enum, and Single-Channel
selector controls — same coverage as #2 but channel-scoped.

### 4. `channel-viewer-analog.png`
**Surface:** Channel Viewer with a live analog (Wfm DBL) trace.
**Must show:** the time axis with a clear t0 origin, axis labels with **unit
suffix** ("V", "°C", etc.), the trace label = channel name, and 2+ traces so
the legend is visible.

### 5. `channel-viewer-digital.png`
**Surface:** Channel Viewer with a digital (Wfm Digital) trace.
**Must show:** at least two digital channels rendered as digital traces (not
analog).

### 6. `channel-viewer-string-event.png`
**Surface:** String / Alarms & Events display.
**Must show:** how a string-data channel renders (String column or
Alarms & Events list with timestamp + message). Lower priority than #4 / #5.

### 7. `setpoint-widget-numeric.png`
**Surface:** Run/Test panel with a numeric setpoint entry control.
**Must show:** the editable numeric box + its unit suffix + the channel
name label, ideally with the Channel Viewer above showing the resulting
output trace.

### 8. `setpoint-widget-digital.png`
**Surface:** Run/Test panel with a digital (Boolean) setpoint toggle.
**Must show:** the toggle/switch control state with a channel name.

### 9. `tdms-file-properties.png`
**Surface:** Recorded TDMS file open in TDMS Viewer (or DIAdem).
**Must show:** the top-level file properties pane with custom metadata
key/value rows from `Set File Metadata`, **and** a TDMS group whose name
matches the plug-in's display name.
**Suggested setup:** record a short test using a plug-in that calls
`Set File Metadata`, then open the resulting TDMS in TDMS Viewer.

### 10. `tdms-alarms-events-channel.png`
**Surface:** TDMS Alarms & Events channel.
**Must show:** a recorded TDMS opened to the Alarms & Events channel with
entries from `Log Event` calls visible. Lower priority than #9.

### 11. `plugin-header-collapsed.png`
**Surface:** A plug-in header bar in the Channel Specification panel.
**Must show:** the plug-in name, the Configure gear (right edge), the Delete
icon (right edge), and the error indicator state if possible.

### 12. `errors-and-warnings-pane.png`
**Surface:** Errors and Warnings pane with a real plug-in error.
**Must show:** the detailed error message, the error icon on the plug-in
header, and the Error indicator next to the Stop Test button.
**Note:** `assets/fl-user-manual/viewing-errors-in-flexlogger__screenshot.png`
already covers this — only re-capture if the doc shot is too cropped for the
hotspots needed.

### 13. `add-channels-plugin-menu.png`
**Surface:** The `Add channels → Plug-in →` flyout menu.
**Must show:** the plug-in name appearing as a selectable item — this is the
"file naming success" visual confirmation referenced in the Step-by-Step
Build tab.

## Optional / nice-to-have

- `command-button-tare-press.png` — Command button mid-press / hover state.
  (`commands__screenshot.png` and `-2.png` in fl-user-manual mostly cover this.)
- `channel-viewer-min-max-resampling.png` — Channel Viewer showing two source
  channels at different rates and an output channel at the resampled rate, to
  illustrate the Set Plugin Resampling effect.
- `dynamic-channels-disable-button.png` — Channel Specification with the
  Disable button visible on a hovered channel row.

## Coverage summary

| Surface | Doc shot exists? | Live capture needed? |
|---|---|---|
| Channel Specification | Partial | Yes (composite) |
| Plug-in Properties dialog | Partial | Yes (composite) |
| Per-channel Properties pane | Partial | Yes (composite) |
| Channel Viewer (analog) | No | Yes |
| Channel Viewer (digital) | No | Yes |
| Channel Viewer (string/events) | No | Yes |
| Setpoint widget (numeric) | No | Yes |
| Setpoint widget (digital) | No | Yes |
| TDMS file properties | No | Yes |
| TDMS Alarms & Events | No | Optional |
| Plug-in header | Implicit only | Yes |
| Errors & Warnings | Yes | Optional |
| Add channels → Plug-in menu | No | Yes |
