# Case 02 — Side-Mounted Fan Configuration

## Overview

This case evaluates the same thermal-management problem using a **side-mounted fan** and a predominantly horizontal cooling arrangement through the finned heat-sink structure.

All operating conditions are kept identical to Case 01 so that the effect of changing the fan placement and airflow path can be assessed directly.

## Simulation Conditions

| Parameter | Value |
|---|---:|
| Heat generation | 60 W |
| Fan airflow | 70 CFM |
| Ambient temperature | 298.15 K (25 °C) |
| Study type | Electronics Cooling |
| Software | Autodesk Fusion |

## Geometry

![Side-mounted fan geometry](images/geometry.png)

The fan is positioned at the side of the heat-sink assembly, directing cooling air across the fin structure.

## Temperature Fields

### Front Section

![Front temperature field](images/temperature-field-front.png)

### Side Section

![Side temperature field](images/temperature-field-side.png)

## Key Result

- **Maximum temperature:** 327.728 K = **54.58 °C**
- **Temperature rise above ambient:** approximately **29.58 °C**
- **Derived peak-to-ambient thermal resistance:** approximately **0.493 K/W**

## Interpretation

Despite using the same 60 W heat load and 70 CFM nominal fan airflow as Case 01, this configuration reaches a substantially higher peak temperature.

The predicted maximum temperature is approximately **14.61 °C higher** than in the top-mounted configuration. The contour plots also show a broader elevated-temperature region around the heat-sink assembly.

For this geometry and simulation setup, the side-mounted fan arrangement therefore provides less effective cooling than the top-mounted configuration.
