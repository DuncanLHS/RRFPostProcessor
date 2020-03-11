# Initial Release 11/03/2020
First attempt at a RepRap Firmware post-processor for Fusion 360 FFF. More changes to come once Autodesk release the CAM functions specific to FFF.

All previous start and end scripts stored in slicer should be moved to start.g and stop.g in RRF firmware.

### Early changes to examples:
- Replace deprecated M107 with M106 S0
- Replace deprecated M104 & M109 with G10 commands (untested for tool changes)
- Remove start and end sripts
- Append M0 to execute stop.g at end of job
- Support 4 extruders (in comments)
