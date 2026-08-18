# Case 01 — Top-Mounted Fan Configuration

## Overview

This case evaluates a finned heat-sink assembly cooled by a **top-mounted fan** in Autodesk Fusion's Electronics Cooling environment.

The simulation uses the same thermal load, airflow, material definitions, ambient condition, and remaining boundary conditions as Case 02 so that the effect of the cooling-layout change can be compared directly.

## Simulation Conditions

| Parameter | Value |
|---|---:|
| Heat generation | 60 W |
| Fan airflow | 70 CFM |
| Ambient temperature | 298.15 K (25 °C) |
| Study type | Electronics Cooling |
| Software | Autodesk Fusion |

## Geometry

![Top-mounted fan geometry](images/geometry.png)

The fan is positioned above the finned heat-sink assembly. The arrangement is intended to drive cooling air through the heat-transfer region from the top of the structure.

## Temperature Field

![Temperature field](images/temperature-field.png)

### Key Result

- **Maximum temperature:** 313.122 K = **39.97 °C**
- **Temperature rise above ambient:** approximately **14.97 °C**
- **Derived peak-to-ambient thermal resistance:** approximately **0.250 K/W**

## Interpretation

Under the applied 60 W heat load and 70 CFM airflow, this configuration maintains the lowest peak temperature of the two evaluated designs.

Because both cases use the same operating conditions, the lower predicted peak temperature indicates that the top-mounted cooling arrangement is more effective for this specific heat-sink geometry and numerical setup.
