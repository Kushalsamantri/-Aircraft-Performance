[Uploading trainer_aircraft_workbook.md…]()
# Trainer Aircraft
## Reference Database & Design Workbook

Aircraft Performance and Design · Team Data Study

Stage 1 master data set for ten fixed-wing training aircraft, extended with the design variables required for individual aircraft sizing: centre-of-gravity position, wing and tail stationing, tail volume coefficients, propulsion detail and structural limits.

**Category** — Trainer aircraft  
**Reference aircraft** — 10  
**Extended fields** — CG / tail / geometry  
**Status** — working database, verification required  

---

## 1. How to read this document

Every numerical entry carries a confidence flag. Nothing in this file may be entered into the team master table without first resolving its flag against a traceable source, and any parameter that cannot be sourced must be recorded as **"Not available"** rather than estimated without a stated method.

| Flag | Meaning | What you must do before submission |
| :--- | :--- | :--- |
| **P** | Widely published figure for the type | Confirm against a Tier 1–3 source and record the document and access date |
| **D** | Derived value — computed from other fields | Record the formula and the input values used |
| **NV** | Not published by the manufacturer | Extract from the aircraft flight manual, measure from a three-view drawing, or write "Not available" |
| **DISP** | Conflicting sources | Resolve against the type-certificate data sheet; cite exactly the value you adopt |

---

## 2. Reference set — identity, mass and propulsion

*Values are indicative working figures of the kind published in manufacturer data sheets and official fact sheets. They are correct in magnitude for the type and must be verified before they enter the graded master table.*

| # | Aircraft | Manufacturer / country | Powerplant | Engines | Rated power or thrust | MTOW [kg] | OEW [kg] | Fuel [kg] | Flag |
| :- | :--- | :--- | :--- | :-: | :--- | -: | -: | -: | :--- |
| 1 | T-6A Texan II | Beechcraft–Textron / USA | P&WC PT6A-68 turboprop | 1 | ≈1,100 shp | 2,858 | 2,150 | Not available | P |
| 2 | PC-9M | Pilatus / Switzerland | P&WC PT6A-62 turboprop | 1 | 850–950 shp quoted; flat rating often higher | 3,200 | 2,250 | Not available | DISP |
| 3 | PC-21 | Pilatus / Switzerland | P&WC PT6A-68B turboprop | 1 | ≈1,600 shp | 4,250 | 3,100 | Not available | P |
| 4 | EMB-312 Tucano | Embraer / Brazil | P&WC PT6A-25C turboprop | 1 | ≈750 shp | 2,990 | 2,150 | Not available | P |
| 5 | A-29 Super Tucano (EMB-314) | Embraer / Brazil | P&WC PT6A-68C turboprop | 1 | ≈1,600 shp | 5,400 | 3,200 | Not available | P |
| 6 | L-39NG | Aero Vodochody / Czechia | Williams FJ44-4M turbofan | 1 | ≈16.9 kN | 4,300 | 3,100 | Not available | P |
| 7 | MB-339 | Leonardo / Italy | Rolls-Royce Viper 632-43 turbofan | 1 | ≈17.8 kN | 6,350 | 4,300 | Not available | P |
| 8 | Hawk T2 / 128 | BAE Systems / UK | Rolls-Royce Adour Mk 951 turbofan | 1 | ≈29 kN | 9,100 | 4,500 | Not available | P |
| 9 | M-346 Master | Leonardo / Italy | 2 × Honeywell F124-GA-200 turbofan | 2 | ≈2 × 27.8 kN | 10,200 | 7,000 | Not available | P |
| 10 | T-50 Golden Eagle | KAI / Republic of Korea | GE F404-GE-402 afterburning turbofan | 1 | ≈78.7 kN with afterburner | 13,500 | 7,500 | Not available | P |

> **Set logic:** five turboprop trainers and five jet trainers span a factor of about 4.7 in takeoff mass and both propulsion classes, so the Stage 2 trend analysis has meaningful spread while the whole set stays inside one operational category — advanced pilot training. The T-50 is a family of supersonic advanced trainers and anchors the upper bound; the T-6A and the EMB-314 Super Tucano are the two types most often cited as fixed-wing training aircraft in the source material.

---

## 3. Wing geometry, loading and derived planform

| # | Aircraft | S [m²] | b [m] | AR = b²/S | Λ [deg] | λw | c̄ ≈ S/b [m] | W/S [kg/m²] | T/W or P/W | Flag |
| :- | :--- | -: | -: | -: | -: | -: | -: | -: | -: | :--- |
| 1 | T-6A | 16.5 | 10.13 | 6.2 | Not available | Not available | 1.63 | 173 | 0.39 shp/kg | P D |
| 2 | PC-9M | 14.9 | 10.12 | 6.9 | Not available | Not available | 1.47 | 215 | 0.30–0.36 shp/kg | DISP D |
| 3 | PC-21 | 15.6 | 9.11 | 5.3 | Not available | Not available | 1.71 | 272 | 0.38 shp/kg | P D |
| 4 | EMB-312 | 19.4 | 11.28 | 6.6 | Not available | Not available | 1.72 | 154 | 0.25 shp/kg | P D |
| 5 | A-29 | 20.0 | 11.14 | 6.2 | Not available | Not available | 1.80 | 270 | 0.30 shp/kg | P D |
| 6 | L-39NG | 18.8 | 9.46 | 4.8 | Not available | Not available | 1.99 | 229 | 0.0039 kN/kg | P D |
| 7 | MB-339 | 19.3 | 10.86 | 6.1 | Not available | Not available | 1.78 | 329 | 0.0028 kN/kg | P D |
| 8 | Hawk | 16.7 | 9.42 | 5.3 | Not available | Not available | 1.77 | 545 | 0.0032 kN/kg | P D |
| 9 | M-346 | 23.5 | 9.72 | 4.0 | Not available | Not available | 2.42 | 434 | 0.0055 kN/kg | P D |
| 10 | T-50 | 23.2 | 9.17 | 3.6 | Not available | Not available | 2.53 | 582 | 0.0058 kN/kg | P D |

*Aspect ratio and mean aerodynamic chord here are computed from the published planform. The exact tapered-wing chord is c̄ = (2/3)·c<sub>r</sub>·(1+λ+λ²)/(1+λ), which needs the root and tip chords — record both once measured from the manufacturer three-view drawing.*

---

## 4. Aerodynamic efficiency parameters

| # | Aircraft | CD0 | e | CLmax clean | (L/D)max | ηp or SFC | Flag |
| :- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1–5 | Turboprop trainers (T-6A, PC-9M, PC-21, EMB-312, A-29) | Not available | Not available | Not available | Not available | ηp ≈ 0.80–0.85 assumed; SFC ≈ 0.5–0.6 lb/hp/hr | NV |
| 6–10 | Jet trainers (L-39NG, MB-339, Hawk, M-346, T-50) | Not available | Not available | Not available | Not available | SFC ≈ 0.7–0.9 lb/lb/hr (cruise) | NV |

> **Method to replace these blanks:** write the drag polar as CD = CD0 + k·CL² with k = 1/(π·AR·e), state CD0 and e as justified assumptions using a recognised estimation approach, then validate the assumption by checking that your predicted cruise speed or range reproduces the published figure in Section 5. That validation is what turns an assumed number into an analysed one.

---

## 5. Performance data

| # | Aircraft | Vmax [km/h] | Vcruise [km/h] | Vs [km/h] | Range [km] | Endurance [h] | Ceiling [m] | ROC [m/s] | TO [m] | LD [m] | n+ / n− [g] | Flag |
| :- | :--- | -: | -: | -: | -: | -: | -: | -: | -: | -: | :-: | :--- |
| 1 | T-6A | 592 | 520 | Not available | 1,660 | Not available | 9,450 | 12.5 | Not available | Not available | +7.0 / −3.5 | P |
| 2 | PC-9M | 593 | 556 | Not available | 1,537 | Not available | 11,580 | 22.3 | Not available | Not available | +7.0 / −3.5 | P |
| 3 | PC-21 | 685 | 560 | Not available | 1,333 | Not available | 11,580 | 23.0 | Not available | Not available | +8.0 / −4.0 | P |
| 4 | EMB-312 | 410 | 350 | Not available | 1,920 | Not available | 10,670 | 10.8 | Not available | Not available | +7.0 / −3.5 | P |
| 5 | A-29 | 593 | 520 | Not available | 2,400 | Not available | 10,670 | 17.0 | Not available | Not available | +7.0 / −3.0 | P |
| 6 | L-39NG | 775 | 600 | Not available | Not available | Not available | 11,500 | 23.0 | Not available | Not available | +8.0 / −4.0 | P |
| 7 | MB-339 | 898 | 720 | Not available | 1,760 | Not available | 11,800 | 32.5 | Not available | Not available | +7.33 / −3.0 | P |
| 8 | Hawk | 1,028 | 780 | Not available | 2,500 | Not available | 13,565 | 47.0 | Not available | Not available | +8.0 / −4.0 | P |
| 9 | M-346 | 1,155 | 900 | Not available | 2,000 | Not available | 13,715 | 32.0 | Not available | Not available | +8.0 / −3.0 | P |
| 10 | T-50 | 1,800 (Mach 1.5) | 1,000 | Not available | 1,850 | Not available | 14,630 | Not available | Not available | Not available | +8.0 / −3.0 | P |
| — | L-39 (conflicting secondary source) | — | — | — | — | — | 16,000 | 260 | — | — | — | DISP — do not use without verification |

> **Disputed-value register.** One secondary source reports for the L-39 a rate of climb of 260 m/s and a service ceiling of 16,000 m, presented as essential for training pilots for high-altitude, high-speed combat. Those two figures are inconsistent with the values commonly published for the type and must be checked against the type-certificate data sheet before use. Comparative material for the L-39 against the MB-339 and against the Yak-130 exists and is usable as a secondary cross-check only.

---

## 6. Extended design database — CG, wing and tail stationing

### 6.1 Field definitions and sourcing

| Field | Symbol / unit | Where it comes from | Current status |
| :--- | :--- | :--- | :--- |
| Fuselage length | L<sub>f</sub> [m] | Manufacturer data sheet | Populated in 6.2 |
| Overall height | H [m] | Manufacturer data sheet | To fill per type |
| Wing leading-edge station from nose | x<sub>LE,w</sub> [m] | Measure from manufacturer three-view | NV |
| Root chord / tip chord / mean aerodynamic chord | c<sub>r</sub>, c<sub>t</sub>, c̄ [m] | Data sheet or three-view | NV — measure, then compute c̄ |
| Wing incidence / dihedral / twist | i<sub>w</sub>, Γ [deg] | Data sheet or three-view | NV |
| Wing airfoil | NACA 4-/5-digit | Handbook, technical paper | NV — a high-lift section such as the Wortmann FX 63-137 is documented as a good trainer choice |
| **CG position from nose** | x<sub>cg</sub> [m] | Aircraft flight manual, weight-and-balance envelope | NV — extract from AFM |
| **CG range forward–aft** | %MAC or units from datum | Aircraft flight manual | NV — record the datum with it |
| Horizontal tail area | S<sub>HT</sub> [m²] | Data sheet / three-view | NV — sanity range S<sub>H</sub>/S ≈ 0.2–0.3 |
| **Tail arm, CG to HT quarter chord** | l<sub>t</sub> [m] | Derived | l<sub>t</sub> = V<sub>H</sub>·S·c̄ / S<sub>HT</sub> |
| Vertical tail area and height | S<sub>VT</sub> [m²], h<sub>v</sub> [m] | Data sheet / three-view | NV |
| Vertical tail moment arm | l<sub>v</sub> [m] | Derived — measured from CG | l<sub>v</sub> = V<sub>V</sub>·S·b / S<sub>VT</sub> |
| Tail volume coefficients | V<sub>H</sub> [–], V<sub>V</sub> [–] | Derived | V<sub>H</sub> = S<sub>HT</sub>·l<sub>t</sub>/(S·c̄) |
| Horizontal tail geometry | λ<sub>t</sub>, Λ<sub>t</sub>, dihedral, airfoil | Data sheet | Design variables — record all four |
| Tail airfoil | NACA 0012-class symmetric | Handbook | Design input for individual cases |
| Propeller diameter / blade count | D [m], B | Engine–propeller data | PT6 applications typically 2.3–2.4 m, 4–5 blades |
| Flap type / landing-gear type | — | Aircraft flight manual | Fixed or retractable main gear typical for turboprop trainers |
| Structural limits | n<sub>+</sub>, n<sub>−</sub>, gust limits | Aircraft flight manual | Populated in Section 5 |
| Mass breakdown | [kg] | AFM or design handbook | Structure, propulsion, systems, avionics, fuel, payload |

### 6.2 Fuselage and configuration values on file

| # | Aircraft | L<sub>f</sub> [m] | H [m] | Flaps | Gear | Propeller | Tail airfoil | Flag |
| :- | :--- | -: | -: | :--- | :--- | :--- | :--- | :--- |
| 1 | T-6A | 10.4 | 3.9 | Slotted | Retractable tricycle | 4-blade, constant speed | NACA 0012 class | P |
| 2 | PC-9M | 10.8 | Not available | Slotted | Retractable | 4-blade, constant speed | NACA 0012 class | P |
| 3 | PC-21 | 11.2 | Not available | Slotted | Retractable | 5-blade, constant speed | NACA 0012 class | P |
| 4 | EMB-312 | 10.0 | Not available | Slotted | Retractable | 3-blade, constant speed | NACA 0012 class | P |
| 5 | A-29 | 11.4 | Not available | Slotted | Retractable | 5-blade, constant speed | NACA 0012 class | P |
| 6 | L-39NG | 12.1 | Not available | Fowler | Retractable | — | NACA 0012 class | P |
| 7 | MB-339 | 11.2 | Not available | Fowler | Retractable | — | NACA 0012 class | P |
| 8 | Hawk | 12.4 | Not available | Fowler | Retractable | — | NACA 0012 class | P |
| 9 | M-346 | 11.5 | Not available | Fowler | Retractable | — | NACA 0012 class | P |
| 10 | T-50 | 13.1 | Not available | Fowler | Retractable | — | NACA 0012 class | P |

---

## 7. Derivation sheet — formulas used in this workbook

```text
1. MEAN AERODYNAMIC CHORD (tapered wing)
   c_bar = (2/3) * c_r * (1 + lambda_w + lambda_w^2) / (1 + lambda_w)
   First estimate when only S and b are known:  c_bar ≈ S / b

2. DRAG POLAR AND INDUCED-DRAG FACTOR
   CD = CD0 + k * CL^2 ,   k = 1 / (pi * AR * e)

3. HORIZONTAL TAIL VOLUME COEFFICIENT
   VH = (S_HT * l_t) / (S * c_bar)
   where l_t is measured from the aircraft CG to the quarter chord of the
   horizontal tail.  Rearranged:  l_t = VH * S * c_bar / S_HT

4. VERTICAL TAIL VOLUME COEFFICIENT
   VV = (S_VT * l_v) / (S * b)
   where l_v is the vertical tail moment arm measured from the aircraft CG.

5. DESIGN-RANGE CHECK
   S_H / S is typically about 0.2 - 0.3 for conventional configurations.

6. HORIZONTAL TAIL DESIGN VARIABLES TO RECORD
   taper ratio, sweep angle, dihedral angle, airfoil section.

7. WING PARAMETERS TO COMPUTE AND RECORD
   wing lift-curve slope, taper ratio, quarter-chord sweep angle, takeoff weight.

8. TURBOPROP THRUST CONVERSION
   T ≈ eta_p * P_shaft / V   plus a residual exhaust term of roughly 10 % of
   total thrust; propellers are constant-speed types with Alpha (flight) and
   Beta (ground / reverse) pitch modes, which matter for takeoff and landing
   distance assumptions.

9. WORKED EXAMPLE — T-6A
   S = 16.5 m2, b = 10.13 m  ->  c_bar ≈ 1.63 m
   S_H / S = 0.25  ->  S_HT ≈ 4.1 m2
   VH = 0.8  ->  l_t = VH * S * c_bar / S_HT ≈ 5.2 m   [DERIVED ESTIMATE]
   Replace with the value measured from the manufacturer three-view before
   the final submission.

10. CG DATA RULE
    CG station and CG range come only from the aircraft flight manual
    weight-and-balance envelope, with the datum convention recorded alongside
    the number.  If the AFM is unavailable the field stays "Not available";
    the fallback is measurement from a scaled three-view drawing, reported as
    "measured, plus or minus 2 % of fuselage length".
```

---

## 8. Source map and verification protocol

| Tier | Source type | What it closes |
| :--- | :--- | :--- |
| 1 | Type-certificate data sheets (FAA / EASA regulatory databases) | MTOW, certified speeds, structural and speed limits, approved powerplant |
| 2 | Aircraft flight manual / pilot's operating handbook | **CG range and datum**, stall speeds, takeoff and landing distances, V–n limits, fuel capacity, fuel-flow data |
| 3 | Manufacturer technical data sheets | S, b, fuselage length, height, powerplant rating, engine variant, wing planform |
| 4 | Official operator and military fact sheets | Role, mass, performance summary, trainer stage |
| 5 | Recognised handbooks, e.g. Bill Gunston, *The Development and Specifications of All Active Military Aircraft* | Geometry and performance cross-check; three-view reference |
| 6 | Comparative studies (L-39 vs MB-339; L-39 vs Yak-130) | Secondary cross-check of speed, range, ceiling and weight only |
| 7 | Design literature and airfoil research | Drag polar parameters k, e, CD0; quarter-chord sweep and taper computation; horizontal tail design variables; tail volume and moment-arm definitions; airfoil selection such as the Wortmann FX 63-137 high-lift section |
| — | Unverified websites | Usable only to locate a Tier 1–7 source; a number copied directly from one is an unsupported value and receives no credit |

---

## 9. Propulsion notes for the analysis stage

- The turboprop trainers in this set are powered almost entirely by the Pratt & Whitney Canada PT6 family, designed in the late 1950s and the standard engine for demanding high-cycle, high-power single- and twin-engine applications.
- The PT6A-62 is rated at 850 or 950 shp depending on the build standard and is the engine used on the Pilatus PC-9; manufacturer literature often quotes a higher flat-rated figure for the PC-9M, so record exactly which rating you adopt.
- The PT6 is a free-turbine turboshaft: only the power turbine drives the propeller while the gas generator spins independently.
- In turboprops, exhaust thrust is sacrificed for shaft power and the exhaust jet produces only about 10 % of total thrust — state this assumption when building the thrust-available curve.
- Piston engines are more efficient than turboprops and bring lower operating cost and lower system mass — a relevant trade-off argument if any team member proposes a piston-powered variant for the individual design case.

---

## 10. Report content categories for the model section

Organise the three-dimensional model discussion under the same breakdown used in structured aircraft documentation: cockpit, cabin, internal structure and equipment. Clear views of the final model are required as visual evidence, and software output must be explained and checked with engineering reasoning — screenshots alone do not constitute analysis.

---

## 11. Closing the remaining blanks — action order

1. **CG and tail arm (highest value, currently NV):** obtain each type's flight manual weight-and-balance section; fill the CG station, CG range and datum fields, then compute l<sub>t</sub> and V<sub>H</sub> with the formulas in Section 7.
2. **Wing and tail planform detail** (λ<sub>w</sub>, Λ, c<sub>r</sub>, c<sub>t</sub>, S<sub>HT</sub>, S<sub>VT</sub>): measure from manufacturer three-view drawings and cross-check against a recognised handbook.
3. **CD0, e, CLmax:** state as justified assumptions and validate by reproducing a published cruise or range figure.
4. **Disputed numbers:** resolve the conflicting L-39 figures in Section 5 against the type-certificate data sheet before any use.
5. **Powerplant columns:** record the exact engine build standard and state the turboprop thrust assumption used.

> **Non-negotiable entry rules.** Every value needs a source recorded in the source column. Keep the original value and state the conversion used. Use one consistent unit set across the whole table. Mark unpublished parameters as "Not available" — never fill a cell with a plausible-looking number. Identify and justify any outlier excluded from mean or median calculations, and never change mass alone while leaving wing, engine and mission physically incompatible.

---

## 12. Unit conversions to record beside converted values

| Quantity | Conversion | Quantity | Conversion |
| :--- | :--- | :--- | :--- |
| Length | 1 ft = 0.3048 m | Mass | 1 lb = 0.453592 kg |
| Area | 1 ft² = 0.092903 m² | Power | 1 hp = 0.7457 kW |
| Force | 1 lbf = 4.44822 N | Speed | 1 kt = 1.852 km/h |
| Vertical speed | 1 ft/min = 0.00508 m/s | SFC | 1 lb/hp/hr = 0.608277 kg/kW/hr |

---

Trainer Aircraft Reference Database & Design Workbook · working document for the team data study.  
Screening figures are provided for set selection and method development only; every value must be verified against the source you cite before it enters the graded master table, and any parameter that cannot be sourced must be recorded as "Not available".
