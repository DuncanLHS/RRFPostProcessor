# Update 11/03/2020

- Change M0 at end to include H1 parameter to keep heaters on. Heaters can be turned off in stop.g.
- Added optional layer change macro property. Executes a macro at each layer change. Insert full path to macro as per M98 in post-processing properties window.
- Added optional post-heat macro property. Executes a macro after heating but before print start. Insert full path to macro as per M98 in post-processing properties window.

# Initial Release 11/03/2020
First attempt at a RepRap Firmware post-processor for Fusion 360 FFF.

All previous start and end scripts stored in slicer should be moved to start.g and stop.g in RRF firmware.

### Early changes to generic fff example:
- Removed all pre-print homing, these should be added to start.g.
- Replace deprecated M107 with M106 S0.
- Replace deprecated M104 & M109 with G10 commands (untested for tool changes).
- Removed other functions start and end scripts.
- Append M0 to execute stop.g at end of job.

### In testing/ideas:
- ~~Optional execute macro after extruder and bed up to temperature (useful to home Z or run purge/wipe routines)~~ Done
- ~~Optional execute macro at layer change (for timelapses).~~ Done
- Standby temperature properties.

# Additional notes:
- Initial extruder heating, bed heating, and the purge line are all automatic and cannot be edited at present.
- Standby temperatures are not natively supported.
- CAM output for extrusion is absolute only.
