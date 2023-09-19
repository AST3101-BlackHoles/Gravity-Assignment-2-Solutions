# Gravity Assignment 2

  * 20% of final grade
  * assigned 22 Sep 2023
  * due 29 Sep 2023

---

## Problem 1

> Some order of magnitude calculations for compact binary systems:
> 
> a) estimate the maximum frequency a binary system will achieve before the components plunge for
> 
>  - black holes with m1 = m2 = 30 Msun

BBH will plunge at ISCO

```math
r_\mathrm{ISCO} \sim \frac{6GM_\mathrm{tot}}{c^2}
```

plugging this into Kepler's law yields

```math
\Omega_\mathrm{orb} = \sqrt{\frac{GM_\mathrm{tot}}{r^3}} \sim \left(\frac{1}{6}\right)^{3/2} \frac{c^3}{GM_\mathrm{tot}}
```

For the dominant quadrupole radiation, we then have

```math
f_\mathrm{GW} = 2 f_\mathrm{orb} = \frac{\Omega_\mathrm{orb}}{\pi}
```

Plugging in numbers for a 30+30 Msun binary system, this corresponds to

```math
f_\mathrm{GW} \approx 73\,\mathrm{Hz}
```

>  - neutron stars m1 = m2 = 1.4 and r1 = r2 = 13km

The radial separation at ISCO for a 1.4+1.4 Msun system is 24.8 km. This is smaller than twice the NS radius (26 km), so the objects will touch before ISCO.
We therefore compute the frequency corresponding to a radial separation of 26 km and obtain

```math
f_\mathrm{GW} = \frac{1}{\pi}\sqrt{\frac{GM}{R^3}} \approx 1460\,\mathrm{Hz}
```

> b) estimate the amplitude of the strain observed at Earth for a binary black hole systems with
> 
>   - m1 = m2 = 30 Msun

>   - orbital frequency at ISCO

>   - luminosity distance of 200 Mpc from Earth

> c) what is the characteristic frequency of a Black Hole's normal modes? (hint, what is the light-travel time?)

## Problem 2

> Using the quadropole approximation and neglecting radiation reaction, compute the strain for the general Keplerian trajectory of two point masses in Newtonian gravity. You can work in the center-of-mass frame.

---

## Extra (not graded)

> Using the detector tensor and the definitions of all GW polarizations, plot the antenna power patterns across the sky for each polarization. Assume a cartesian coordinate system aligned with the detector arms. Is there anything special about the antenna pattern for breathing and longitudinal modes?
