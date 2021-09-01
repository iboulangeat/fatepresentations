---
title: FATE-HD model
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
background-image: url(abandon.gif)
# FATE-HD, a landscape simulation model

---

class: compact, img-left
# FATE-HD, an hybrid model
FATE-HD among DVMs
<br><br>
![Image](FATE-among.png)
.absolute.r-2.b-2[<sub><sup><sup>Boulangeat et al. 2014, GCB</sub></sup></sup>]

--

A landscape model dealing with **forest and non-forests**

- Response to climate (via Habitat model)
- Vegetation diversity (PFG)
- Simpified population dynamics (competition for light, dispersal, demography)
- Semi-quantitatif (easy to parameterize)
- Disturbances (fire, grazing, mowing)


---
class:
# FATE-HD model
.absolute.r-2.b-2[<sub><sup><sup>Boulangeat et al. 2014, GCB</sub></sup></sup>]

![Image](FATE_pixel.png# absolute w-20pct l-60pct t-40pct)

--
![Image](FATE_demo.png# absolute w-20pct l-40pct t-40pct)
.absolute.r-4.t-3[<sub><sup><sup>Germination <br> Recruitment<br> Growth<br>Survival<br>Fecundity</sub></sup></sup>]


---
class:
# FATE-HD model
.absolute.r-2.b-2[<sub><sup><sup>Boulangeat et al. 2014, GCB</sub></sup></sup>]
![Image](FATE_demo.png# absolute w-20pct l-40pct t-40pct)
.absolute.r-4.t-3[<sub><sup><sup>Germination <br> Recruitment<br> Growth<br>Survival<br>Fecundity</sub></sup></sup>]

![Image](FATE_abiotic.png# absolute w-20pct r-6 t-1)
--
![Image](FATE_biotic.png# absolute w-30pct l-4 t-5)
--
![Image](FATE_disp_all.png# absolute w-50pct r-4 b-10pct)

---
class:
# FATE-HD model
.absolute.r-2.b-2[<sub><sup><sup>Boulangeat et al. 2014, GCB</sub></sup></sup>]
![Image](FATE_demo.png# absolute w-20pct l-40pct t-40pct)

![Image](FATE_abiotic.png# absolute w-20pct r-6 t-1)

![Image](FATE_biotic.png# absolute w-30pct l-4 t-5)

![Image](FATE_disp.png# absolute w-20pct r-6 b-10pct)

![Image](FATE_dist.png# absolute w-33pct r-3 b-40pct)

---
class: col-2
# Demography
![Image](FATE_demo.png# relative w-80pct l-20pct t-20pct)
- individuals grouped by cohorts
- maturity attribute
- longevity
<br><br>**seed production**
- = f(longevity, maturity) renewal hypothesis
- = f(habitat, stochasticity) yes/no
---
class: col-2
# Habitat filter
![Image](FATE_abiotic.png# relative w-80pct l-20pct t-20pct)
- habitat model (SDM)
- climate, soil, topography
- stochasticity and step response function for **seed production** and **establishment**
---
class: col-2
# Species interactions
![Image](FATE_biotic.png# relative w-80pct l-20pct t-20pct)
- competition for light
- 3 light levels (low, medium, high)
- growth = age to change of strata
![Image](age_strata.png# relative w-80pct l-20pct t-20pct)
- response to light distinct from germinant, juveniles or matures
- maximum abundance in a pixel for each PFG
---
class: col-2
# Dispersal
![Image](dispersal2.png# relative w-80pct l-20pct t-20pct)

- 50% of seed in a first circle having X pixels
- 49% in a second circle, by packages of two pixels for a total of X pixels
- 1% random in a larger buffer
<br><br>**parameters**
- dispersal distances for 50, 99% of seeds
- long distance
- can be based on traits including the most efficient dispersal mode (not the most prevalent)

---
class: col-2
# Disturbances
![Image](PNE_map_pastures.png# relative w-80pct l-20pct t-20pct)
- pasture maps and intensity
- response of each PFG and stage (juvenile, mature, senescent)
- % of mortality and % of no seed production (rejuvenate)
---
class:
# Modular structure
![Image](modularStruct.png# w-60pct)

---
class:
# Parameterization : data
![Image](paramData.png# w-80pct)

---
class:
# Parameterization: from data to parameters
![Image](parameters.png# w-80pct)


---
class: col-2
# Simulating current distribution of PFG
![Image](FATE_init.png# relative)
- seeding until large trees reach their final strata
- stabilization of the demography
- remove trees in managed areas (pastures)
- stabilization
- remove again trees in managed areas

---
class:
# Validation of the vegetation structure

![Image](validation.png# w-80pct)

---
class:
# FATE-HD vs SDM (at equilibrium)
Refine PFGs distribution inside their habitat limits
![Image](FATE_SDM.png# w-80pct)

---
class:
# Simulate landscape dynamics under scenarios
![Image](scenariosPNE.png# db w-80pct)
.absolute.r-2.b-2[<sub><sup><sup>Boulangeat et al. 2014, Ecography</sub></sup></sup>]

---
class:
# Tree cover change over space and time
![Image](legend_anim.png# absolute t-20pct l-10pct h-10pct)

.absolute.l-4.t-30pct[Intensification]
![Image](intens.gif# fixed b-2 l-4 w-34pct)
<!-- .fixed.b-2.l-4[<video height="400" autoplay><source src="intens.mp4" type="video/mp4"></video>] -->
.absolute.r-5.t-30pct[Abandonment]
![Image](abandon.gif# fixed b-2 r-4 w-34pct)
<!-- .fixed.b-2.r-4[<video height="400" autoplay><source src="abandon.mp4" type="video/mp4"></video>] -->
.absolute.r-2.b-2[<sub><sup><sup>Boulangeat et al. 2014, Ecography</sub></sup></sup>]

---
class:
# Changes in regional diversity

![Image](div_LU.png# w-80pct)
.absolute.r-2.b-2[<sub><sup><sup>Boulangeat et al. 2014, Ecography</sub></sup></sup>]

---
class:
# Changes in regional diversity
.absolute.r-2.b-2[<sub><sup><sup>Boulangeat et al. 2014, Ecography</sub></sup></sup>]

![Image](div_LU2.png# absolute w-40pct center)
--

.absolute.l-3.t-5[additive effects]
--

.absolute.r-3.t-5[multiplicative effects]

---
class:
# Change in local diversity
![Image](div-local.png# w-90pct)
.absolute.r-2.b-2[<sub><sup><sup>Boulangeat et al. 2014, Ecography</sub></sup></sup>]

---
class:
# Diversity decomposition
- change in **composition**
- change in **abundances**
.absolute.r-2.b-2[<sub><sup><sup>Boulangeat et al. 2014, Ecography</sub></sup></sup>]

--

\\[
^2D = ^0D \times EF
\\]

--
\\( ^0D = \\) richness -> beta = compositional turnover

\\( EF =\\) evenness factor -> beta = abundances re-arrangement


---
class: fit-h1, no-footer
# Changes over time, elevation and diversity dimensions
![Image](div-decomp.png)
.absolute.r-2.b-2[<sub><sup><sup>Boulangeat et al. 2014, Ecography</sub></sup></sup>]

---
class: fit-h1
# Main highlights about the changes in functional diversity

.absolute.r-2.b-2[<sub><sup><sup>Boulangeat et al. 2014, Ecography</sub></sup></sup>]
--
<br>
**Effet of human land-use:**
Heterogeneity (beta) in average decreases in case of tree colonization but increases in case of habitat loss

**Effect of different PFG assemblages:**
The diversity response depends on elevation

**Interaction between drivers:**
Multiplicative effects are found when land abandonment is combined with climate change

<!-- ========================================================================== -->

---

class: no-footer
background-image: url(marais_acide_lautaret.JPG)
# Thanks
Damien, Pauline, Maya, Wilfried
<br> Richard, Cédric, Sylvain, Jérémie, Pascal, Rolland
