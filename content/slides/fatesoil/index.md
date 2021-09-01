---
title: FATE soil
description: ""
ratio: "16:9"
themes:
- apron
- descartes
- adirondack
classes:
- feature-math
- feature-nohighlight


---
layout: true
.footer[
<!-- - @DrIsaBlg -->
- <i class="fab fa-github"></i>iboulangeat
<!-- - isabelle.boulangeat@irstea.fr -->
- 2019
<!-- - ![logo](/img/logo.jpg) -->
]
<!--  -->

---
class: title, smokescreen, no-footer
background-image: url(Foto0020.jpg)
# Plant and soil interactions
---
class: col-2
# Fundamental hypothesis
![Image](b1.png#)
![Image](b2.png#)

---
class: img-right
# Objective and fundamental hypothesis
![Image](successionSoil.png#)

Objective: Improve the modeling of plant succession by integrating a dynamic **soil general property**.

Hypotheses:
<sub><sub><sub>Berendse 1998, Biogeochemistry</sub></sub></sub>

1. Soil composition evolve during the succession: Nitrogen, soil moisture, organic matter,C:P, N:P, C:N,... increases.
2. This is partly due to litter decomposition

---
class:
# Rationale
>> Conceptual frameworks describing mechanisms of primary succession should acknowledge soil conditioning by previous plants as a potential mechanism of positive feedback <sub><sub><sub>Castle et al. 2015, JoE</sub></sub></sub>

- With the arrival of **new species**, the soil is progressively **enriched** depending on each species specific **contribution** and thus potentially **becomes suitable** for late successional species.

- After a while, **pioneer species**, which are not competitive enough to survive in rich soils **are excluded** or highly limited in abundance (without any competition for light involved)
---
class:
# The algorithm
- bare soil has a default value
- soil value changes from year to year: a **community weighted mean** based on each species specific **soil contribution parameter** and **cover**.
- Each PFG (or species) has a **specific tolerance** with respect to three levels of soil “richness” leading to **mortality**
<br><br>Secondary succession:
- After a disturbance, the **"bare" soil default value** is set according to the composition of the **community before the disturbance**, until the pixel reaches again is full cover.
-  There is an option to set a specific default value after a particular disturbance.
---
class:
# Test in a pixel: Glacier Bay (primary succession)
![Image](img_GB.jpg# relative w-90pct)
---
class:
# Test in a pixel: Glacier Bay (primary succession)
![Image](GB_Chapin2.png# relative w-90pct)

---
class: col-2
# Test in a pixel: Glacier Bay (primary succession)
![Image](GBparams.png# relative w-100pct t-4)
![Image](gbSimu.png# relative w-100pct)

---
class:
# Remarks

This plant-soil interaction represents a **proxy for a number of different mechanisms** of soil modification, just like competition for light synthesizes multiple processes (cf. canopy effect).

Questions:
- what are the **best foliar traits** to represent contributions and tolerances?
  - plant and soil N:P ratios are decoupled (i.e. not related) along the ecological succession<sub><sub><sub>Di Palo 2017, PloS one ; see also Wardle et al. 2009, FuncEcol</sub></sub></sub>

- Is there the same gradient in secondary succession than primary succession? How to deal with nitrogen deposits?


---

class: no-footer
background-image: url(marais_acide_lautaret.JPG)
# Thanks
Damien, Ceres, Marta, Maya, Wilfried, Tamara
