# GWTC-Lau-correction: V=0.9797

## Idea
Gravitational wave propagation may not be exactly c, but V = 1 - f^2
where f = 14.26% = 0.1426
f^2 = 0.02033
**V = 0.9797 (2.03% slower than c)**

## Test on GWTC-5.0 O4b marginal events

GWTC-5.0 has 161 new candidates (total 390). Some have pipeline disagreement:

- **GW250120_042414**: gstlal p_astro 0.84 vs MBTA p_astro 0.30 (from screenshot)
- **GW240930_123408**: FAR 2.9, p_astro 0.81, no distance
- **GW241009_022835**: SNR 8.4, distance 5600 Mpc

### Lau Correction
D_Lau = D_official * 0.9797

| Event | D_official | D_Lau | Delta |
|---|---|---|---|
| GW241009_022835 | 5600 Mpc | 5486.1 Mpc | -113.9 Mpc |
| GW241007_082943 | 4000 Mpc | 3918.7 Mpc | -81.3 Mpc |
| GW241009_084816 | 1130 Mpc | 1107.0 Mpc | -23.0 Mpc |
| GW250120_042414 (est) | 1500 Mpc | 1469.5 Mpc | -30.5 Mpc |

A 2.03% distance decrease = ~2% SNR increase, could shift p_astro 0.3 -> 0.7 for threshold events.

## How to reproduce (phone friendly)
No HDF needed, use JSON:
https://www.gw-openscience.org/eventapi/json/GWTC-5.0/

## Author
tiny1813 - Hong Kong
Theory: Lau 14.26% geometric factor
