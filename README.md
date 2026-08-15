# Photovoltaic System Design Study — Residential New-Build, Fliegerhorst Quarter, Oldenburg

University project for a real 14-unit residential building under construction in Oldenburg, Germany.

## Motivation
New residential developments increasingly need to decide on PV layout early in the design process. This project compares multiple PV configurations for a real building to identify which layout maximizes energy yield and coverage of household demand, while accounting for German regulatory requirements.

## What we did
- Simulated and compared 4 PV configurations (south-facing rows, east–west, low-tilt, façade-mounted) using Python (`pvlib`) and NREL SAM, with PVGIS TMY weather data
- Derived usable roof geometry from AutoCAD site plans and sized each layout via ground-coverage-ratio analysis
- Performed tilt/azimuth sensitivity analysis across configurations
- Cross-validated pvlib results against NREL SAM outputs
- Incorporated German regulatory context: §32a NBauO PV obligation and negative electricity price feed-in rules

## Key results
- A dense **east–west layout delivered ~49% more annual energy** than south-facing rows on the same roof area
- pvlib and NREL SAM outputs agreed within **4–8% deviation**, with differences traced to thermal and transposition model assumptions
- Recommended a **29 kWp system covering ~70%** of estimated household demand

## Tools
Python · pvlib · NREL SAM · PVGIS · AutoCAD (site plan measurement)

