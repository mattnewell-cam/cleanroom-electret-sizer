# Cleanroom electret sizer

https://mattnewell-cam.github.io/cleanroom-electret-sizer/

Pick what pressurises the room (a vacuum cleaner slowed by a space heater in series, a pedestal fan or a
small portable air cleaner) and the room pressure you want. The page finds the operating point where
fan pressure = room pressure (from the room's leakage, Q = C·Δpⁿ) + electret pressure drop, and the least
electret (square side × layers) that reaches the PF you ask for at 0.3 µm.

- Room leakage defaults to a measured test bedroom: 16 Pa at 13.2 L/s and 7 Pa at 8.6 L/s, so n = 0.51 and
  23.6 L/s at 50 Pa. Both are editable.
- Fan curves are measured: sealed-inlet pressure and bag-fill free flow for the vacuum on each heater setting,
  orifice tests for the pedestal fan, bag fills against pressure for the Levoit Core Mini.
- Electret per layer: Δp = 2.58·v Pa, log10 PF = 1.5863·v^−0.307 at 0.3 µm (v in cm/s), fitted to vacuum-bag
  electret measured at 4.9–5.9 cm/s. Outside that range it is extrapolated, and the page says so.
- PF is the electret alone. It ignores leaks around the electret and air leaking into the room.

Single file, no build step.
