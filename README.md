# Comparative Electronics Cooling Analysis of Heat Sink Configurations

A comparative electronics-cooling study performed in **Autodesk Fusion** to evaluate two forced-air heat-sink configurations under identical operating conditions.

The study compares how changing the **fan placement and resulting cooling arrangement** affects the temperature field and peak component temperature while keeping the thermal load and airflow constant.

## Project Objective

The objective was to compare two heat-sink layouts under the same operating conditions and determine which configuration provides more effective thermal management.

Two configurations were evaluated:

1. **Case 01 — Top-mounted fan configuration**
2. **Case 02 — Side-mounted fan configuration**

## Common Simulation Conditions

| Parameter | Value |
|---|---:|
| Software | Autodesk Fusion |
| Study type | Electronics Cooling |
| Heat generation | 60 W |
| Fan airflow | 70 CFM |
| Ambient temperature | 298.15 K (25 °C) |
| Materials | Identical in both cases |
| Boundary conditions | Identical in both cases |
| Primary design variable | Fan placement / cooling configuration |

Keeping the operating conditions identical isolates the effect of the cooling-layout change on the thermal response.

## Case 01 — Top-Mounted Fan

![Case 01 geometry](case-01-top-mounted-fan/images/geometry.png)

The first configuration places the fan above the finned heat sink, producing a top-driven cooling arrangement.

### Temperature Result

![Case 01 temperature field](case-01-top-mounted-fan/images/temperature-field.png)

- Maximum temperature: **313.122 K**
- Maximum temperature: **39.97 °C**
- Minimum displayed temperature: **298.15 K (25 °C)**

The temperature field remains comparatively low under the prescribed 60 W thermal load and 70 CFM airflow.

[Detailed Case 01 notes](case-01-top-mounted-fan/README.md)

## Case 02 — Side-Mounted Fan

![Case 02 geometry](case-02-side-mounted-fan/images/geometry.png)

The second configuration moves the fan to the side of the fin array, producing a predominantly horizontal cooling arrangement through the heat-sink structure.

### Temperature Result

![Case 02 temperature field](case-02-side-mounted-fan/images/temperature-field-front.png)

- Maximum temperature: **327.728 K**
- Maximum temperature: **54.58 °C**
- Minimum displayed temperature: **298.15 K (25 °C)**

A larger high-temperature region is visible in the thermal field, and the predicted peak temperature is higher than in Case 01.

[Detailed Case 02 notes](case-02-side-mounted-fan/README.md)

## Results Comparison

| Metric | Case 01 — Top Fan | Case 02 — Side Fan |
|---|---:|---:|
| Heat generation | 60 W | 60 W |
| Fan airflow | 70 CFM | 70 CFM |
| Ambient temperature | 25 °C | 25 °C |
| Maximum temperature | 39.97 °C | 54.58 °C |
| Temperature rise above ambient | 14.97 °C | 29.58 °C |
| Difference in peak temperature | — | +14.61 °C |

Under otherwise identical simulation conditions, the top-mounted configuration produced a peak temperature approximately **14.61 °C lower** than the side-mounted configuration.

Expressed as thermal resistance relative to ambient,

- Case 01: **0.250 K/W**
- Case 02: **0.493 K/W**

These values are derived from \(R_{th}=(T_{max}-T_{ambient})/Q\) using the simulated peak temperature and the applied 60 W heat load. They are useful as compact comparative metrics for these two simulation cases.

## Engineering Interpretation

The simulations indicate that fan placement has a substantial influence on the thermal performance of this heat-sink assembly. With the heat input, airflow, materials, and boundary conditions held constant, the top-mounted fan arrangement produced both a lower peak temperature and a lower temperature rise above ambient.

For this specific geometry and simulation setup, **Case 01 provides the more effective cooling configuration**.

The contour plots also show different heat-spreading patterns between the two layouts. The comparison therefore demonstrates that identical nominal fan airflow does not necessarily produce identical component cooling when the airflow path and heat-sink arrangement change.

## Scope and Limitations

This repository documents a comparative simulation study rather than an experimental validation campaign. The conclusions therefore apply to the modeled geometry, material definitions, boundary conditions, and Autodesk Fusion Electronics Cooling setup used here.

The comparison is intended to evaluate the relative performance of the two configurations under matched numerical conditions. Experimental measurements would be required to validate the absolute predicted temperatures.

## Repository Structure

```text
fusion-electronics-cooling-comparison/
├── README.md
├── data/
│   └── results-summary.csv
├── case-01-top-mounted-fan/
│   ├── README.md
│   └── images/
│       ├── geometry.png
│       └── temperature-field.png
└── case-02-side-mounted-fan/
    ├── README.md
    └── images/
        ├── geometry.png
        ├── temperature-field-front.png
        └── temperature-field-side.png
```

## Tools

- Autodesk Fusion
- Electronics Cooling simulation environment
- CAD-based thermal design comparison

## Author

**Turan Özbayrak**

Materials / Mechanical Engineering
