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

From lecture, we have the following expression

```math
|\bar{h}_{ij}| \sim \frac{4c}{r} \left( \frac{G}{c^3} \mathcal{M} \Omega_\mathrm{orb} \right) \Omega_\mathrm{orb}^{-1}
```

and at ISCO

```math
\Omega_\mathrm{orb} = 6^{-3/2} \frac{c^3}{GM_\mathrm{tot}}
```

Plugging in numbers, we get

```math
\Omega_\mathrm{orb} = 230\,\mathrm{rad/sec}
```

```math
\mathcal{M} = \frac{(m_1 m_2)^{3/5}}{(m_1+m_2)^{1/5}} = 26.1\,M_\odot = 5.19\times10^{31}\,\mathrm{kg}
```

```math
r = 200\,\mathrm{Mpc} = 6.172 \times 10^{24}\,\mathrm{m}
```

so that

```math
|\bar{h}_{ij}| \sim 2.4 \times 10^{-21}
```

> c) what is the characteristic frequency of a Black Hole's normal modes? (hint, what is the light-travel time?)

We consider the time it takes light to go around the circumfrence of a BH.

```math
T \sim \frac{2\pi R}{c} \sim \frac{4\pi G M}{c^3} \sim (60\,\mu\mathrm{s}) \frac{M}{M_\odot}
```

for a 30+30=60 Msun BH, we obtain

```math
T_{60\,M_\odot} \sim 3.7\,\mathrm{ms}
```

```math
f_{60\,M_\odot} \sim 270\,\mathrm{Hz}
```

## Problem 2

> Using the quadropole approximation and neglecting radiation reaction, compute the strain for the general Keplerian trajectory of two point masses in Newtonian gravity. You can work in the center-of-mass frame.

In the center-of-mass frame, we have

```math
H = \frac{p_r^2}{2\mu} + \frac{L^2}{2\mu r^2} - \frac{GM_\mathrm{tot}\mu}{r} = \mathrm{constant}
```

where

```math
one \\
two
```

---

## Extra (not graded)

> Using the detector tensor and the definitions of all GW polarizations, plot the antenna power patterns across the sky for each polarization. Assume a cartesian coordinate system aligned with the detector arms. Is there anything special about the antenna pattern for breathing and longitudinal modes?

Important points to note are:

  * the detector response depends on both the direction to the source (RA, Dec) *and* an additional angle that determines the relative rotation between the wave's coordinate system and the detector's coordinate system (polarization angle)
  * the response to the breathing and longitudinal modes are the same in magnitude and opposite in sign. This is because there is a linear combination of these modes that corresponds to isotropic expansion/contration, and the differential arm lengths measured by current interferometers will always be zero for isotropic expansion/contraction.
