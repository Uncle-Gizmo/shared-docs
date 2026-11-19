# Mazda2 HN16 ZJO: fault code report review

Review date: 2026-11-19
Scan date: 2026-11-18 09:58, TOPDON ONE Lite, at R C S Motors Ltd, Wantage

## Vehicle (from the scan report)

| Field | Report shows | Comment |
| --- | --- | --- |
| Plate | HN16ZJO | Correct |
| Make / model | Mazda2 (Demio) | Correct |
| Engine | P5, 1.5 litre petrol (Skyactiv-G 1.5), automatic | Consistent |
| Mileage | 80,123 miles | As recorded |
| Year | **2001** | **Wrong.** An HN16 plate is a 2016 registration, and the Skyactiv-G 1.5 Mazda2 (DJ) only started in 2014. The scanner seems to have decoded the year from the VIN. This doesn't change the fault codes. |

## Fault codes stored (PCM)

| Code | Description | Status |
| --- | --- | --- |
| P0091:00 | Fuel pressure regulator 'A' control circuit low | ODDTC |
| P0091:00:AF | Fuel pressure regulator 'A' control circuit low | CMDTC |
| P0092:00:A8 | Fuel pressure regulator 'A' control circuit high | CMDTC |
| P0091 | Fuel pressure regulator 'A' control circuit low | Pending |

## What the codes mean

On the Skyactiv-G engine, the "fuel pressure regulator" in these codes is the **spill valve control solenoid**, which is **built into the high-pressure fuel pump**. These codes are **not** fuel pressure sensor codes: the sensor has its own codes, P0087 and P0088.

- **P0091 (circuit low):** the engine computer (PCM) has switched the solenoid off, but the circuit voltage stays low for 5 seconds. This means an open circuit or a short to ground.
- **P0092 (circuit high):** the PCM has switched the solenoid on, but the circuit voltage stays high for 5 seconds. This means a short to power.

When either code sets, the PCM stops controlling the high-pressure pump and limits the air going into the engine, so the car is down on power.

## Possible causes, in Mazda's order

1. High-pressure fuel pump connector or terminals
2. PCM connector or terminals
3. Wiring between pump terminal B and PCM terminal 1EF (short to ground or power), or a break in the pump A/B to PCM 1EE/1EF wiring
4. Spill valve solenoid, which is built into the pump, so the fix is to replace the high-pressure fuel pump assembly
5. PCM

Having both a "circuit low" and a "circuit high" code on the same circuit often points to an intermittent connection, such as a connector, a pin or a chafed wire. Mazda's procedure checks those before replacing the pump.

## Questions for the garage

- Have the pump connector, the PCM connector and the wire between them been checked and tested?
- If the pump is needed, what is the exact Mazda part number? Note that it is the high-pressure fuel pump assembly, not a sensor.

## Sources (Mazda service information)

- DTC P0092:00 [Skyactiv-G 1.5 / 2.0 / 2.5]: https://charm.li/Mazda/Mazda3%2009%2F2013%20-%2005%2F2016%20%28d9g6-1a-21b_ver17%29/esicont/srvc/html/id0102h9009200.html
- DTC P0091:00 [PCM Skyactiv-G]: https://charm.li/Mazda/Mazda6%2007%2F2016%20-%2002%2F2018%20%28d9j8-1a-21b_ver10%29/esicont/srvc/html/id0102j1009100.html
- Mazda2 09/2014 to 01/2017 service manual index (lists P0091:00 for Skyactiv-G 1.3 / 1.5): https://charm.li/Mazda/Mazda2%2009%2F2014%20-%2001%2F2017%20%28d9h1-1a-22c_ver17%29/index.html
