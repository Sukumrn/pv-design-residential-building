# Photovoltaic Configuration Study — Residential Building, Fliegerhorst Oldenburg

A collaborative university project examining photovoltaic layout options for a 14-unit residential development in Oldenburg, Germany.

## Objective

Compare candidate PV configurations for the building's roof, wing, and façade, considering annual energy production, specific yield, seasonal production, and an indicative household electricity-demand profile.

## Modelling workflow

- Retrieve Typical Meteorological Year (TMY) weather data for the site from PVGIS using pvlib.
- Calculate solar position and plane-of-array irradiance for candidate surface orientations.
- Estimate module temperature using the Faiman model.
- Estimate DC output with the pvlib PVWatts model and apply simplified system and inverter loss factors.
- Compare south-facing, east–west, wing, and façade configurations.
- Conduct tilt and azimuth sensitivity analyses.
- Evaluate an indicative 29 kWp roof-and-wing scenario against an assumed household electricity-demand profile.

## Repository contents

- `notebooks/pv_configuration_analysis.ipynb` — cleaned analysis notebook.
- `requirements.txt` — Python package dependencies.

## Run the notebook

```bash
python -m venv .venv
source .venv/bin/activate
# On Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter lab
```

The notebook retrieves TMY weather data from PVGIS at runtime, so an internet connection is required for the initial data request.

## Tools and methods

Python · pvlib · pandas · NumPy · Matplotlib · PVGIS TMY · AutoCAD site-plan measurements

## Important assumptions and limitations

This is an academic design study based on supplied site-plan geometry and model assumptions. Results depend on usable roof area, module packing density, orientation, tilt, weather-year selection, temperature coefficients, shading treatment, and assumed system losses.

The household demand profile is an estimate for comparison, not measured consumption. The model does not establish actual self-consumption, grid export, storage dispatch, or financial performance. The notebook uses a pvlib/PVWatts-based workflow; it should not be interpreted as an NREL SAM simulation or cross-validation.

Specific numerical comparisons should be quoted only with their corresponding system capacities and assumptions. Total annual energy and specific yield (kWh/kWp) are different comparison metrics.
