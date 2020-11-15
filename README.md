---
author:
- |
  Andrey Kim, University of Connecticut\
  Robert Johnston, MIT\
title: Analysis note on Deeply Virtual $\pi^0$ Production
---

-   [PID](#pid)
    -   [Electron](#electron)
    -   [Proton](#proton)
    -   [Photon](#photon)
    -   [Neutral pion](#neutral-pion)
-   [Exclusive selection](#exclusive-selection)
    -   [Exclusive distributions](#exclusive-distributions)
        -   [Tight $M_{\gamma\gamma}$ mass and transverse missing
            momenta
            cuts](#tight-m_gammagamma-mass-and-transverse-missing-momenta-cuts)
        -   [$\theta_{X\pi}$ cut
            determination](#theta_xpi-cut-determination)
        -   [Final exclusivity cuts](#final-exclusivity-cuts)
-   [Results](#results)
    -   [Kinematic coverage and
        binning](#kinematic-coverage-and-binning)
    -   [Beam Spin Asymmetry](#beam-spin-asymmetry)
        -   [Sideband background
            subtraction](#sideband-background-subtraction)
        -   [Results](#results-1)
-   [Simulations](#simulations)
    -   [Generator and Simulations](#generator-and-simulations)
    -   [Comparison to Data: Basic
        Kinematics](#comparison-to-data-basic-kinematics)
    -   [Comparison to Data: Kinematics - Scattering
        Variables](#comparison-to-data-kinematics---scattering-variables)
        -   [Bjorken X and $Q^2$
            Distributions](#bjorken-x-and-q2-distributions)
        -   [W and t Distributions](#w-and-t-distributions)
    -   [Comparison to Data: Reconstructed Pion and
        Exclusivity](#comparison-to-data-reconstructed-pion-and-exclusivity)
        -   [Pion Mass and Energy](#pion-mass-and-energy)
        -   [Missing Mass](#missing-mass)
    -   [Missing Energy](#missing-energy)
-   [Appendix](#appendix)
    -   [Cross check between our
        results](#cross-check-between-our-results)
    -   [Other Simulation Results](#other-simulation-results)
        -   [Lepton-Hadron Angle](#lepton-hadron-angle)

test

PID
===

For this analysis all final state particles should be detected. After
$\pi^0$ decay we are going to have 4 particles: electron, proton and two
photons. The particle identification methods are applied to select the
exclusive event with at least one electron, proton and two photons.

Electron
--------

Initially electron is selected as a negative track that is identified as
electron by Event Builder, i.e. has assigned pid=11. Next we apply a
series of cuts to further improve electron selection and pion rejection
using the cuts from official note of \"RGA analysis overview and
procedures\". The code for these electron cuts has been cross checked
and validated with Stefan Diehl during his $\pi^+$ SIDIS analysis cross
check. The documentation to the code used for electron PID can be found
here: <https://drewkenjo.github.io/uconn-java-utils/annotated.html>.

The list of electron PID cuts is following:

-   Event Builder PID cut: pid=11

-   Cherenkov nphe cut

-   DC fiducial cuts for regions 1,2,3

-   Z vertex cut

-   EC fiducial cut

-   EC sampling cut

-   minimum PCAL energy

Proton
------

The list of proton PID cuts is following:

-   Event Builder PID cut: pid=2212

-   DC fiducial cuts for regions 1,2,3

-   $\Delta v_z$ vertex cut

-   **Forward Detector** only

Photon
------

The list of photon PID cuts is following:

-   Event Builder PID cut: pid=22

-   Forward Detector only

-   **not** in the sector where electron is detected

Neutral pion
------------

In addition to individual particle PID procedures the cut on the mass of
two photons is applied:

-   $0.07<M_{\gamma\gamma}<0.2$ GeV

![The distribution for mass of two photons
$M_{\gamma\gamma}$](figures/eppi0.exclusive.pdf){#fig:ggmass
width="0.6\\linewidth"}

. [\[fig:ggmass\]]{#fig:ggmass label="fig:ggmass"}

Exclusive selection
===================

Exclusive distributions
-----------------------

r0.58 ![image](figures/eppi0.exclusive.pdf){width="0.97\\linewidth"}

After the selection of events with at least one electron, proton and two
photons, it is time to take a look at the exclusive distributions. The
Fig. [\[fig:MM2vsThetaXPi\]](#fig:MM2vsThetaXPi){reference-type="ref"
reference="fig:MM2vsThetaXPi"} shows 2D distribution of MM$^2$ (epX) vs
$\theta_{X\pi}$, where MM$^2$ (epX) is a missing mass squared of (epX)
system and should have a peak near 0.0182 GeV$^2$, and $\theta_{X\pi}$
is an angle between expected and reconstructed pion. The bright spot on
the figure corresponds to the exclusive $ep\rightarrow~ep\pi^0$ events.
In order to reduce the background exclusivity cuts need to be developed
based on the conservation of energy and momentum. The relevant 1D
exclusive distributions are shown on the
Fig. [2.2](#fig:rawexclusive1){reference-type="ref"
reference="fig:rawexclusive1"} and
[2.4](#fig:rawexclusive2){reference-type="ref"
reference="fig:rawexclusive2"}.

![Exclusive distributions for events with at least one electron, proton
and two photons.](figures/eppi0.exclusive.pdf "fig:"){#fig:rawexclusive1
width="0.47\\linewidth"} ![Exclusive distributions for events with at
least one electron, proton and two
photons.](figures/eppi0.exclusive.pdf "fig:"){#fig:rawexclusive1
width="0.47\\linewidth"}

![Exclusive distributions for events with at least one electron, proton
and two photons.](figures/eppi0.exclusive.pdf "fig:"){#fig:rawexclusive2
width="0.47\\linewidth"} ![Exclusive distributions for events with at
least one electron, proton and two
photons.](figures/eppi0.exclusive.pdf "fig:"){#fig:rawexclusive2
width="0.47\\linewidth"}

### Tight $M_{\gamma\gamma}$ mass and transverse missing momenta cuts

The first step is to use tighter $\gamma\gamma$ mass cut:
$0.096<M_{\gamma\gamma}<0.168$ GeV, and take a look at the missing
transverse momentum distributions (see
Fig. [2.6](#fig:ptdistributions){reference-type="ref"
reference="fig:ptdistributions"}). From momentum conservation law we
expect transverse momentum to be zero, so we can apply cuts on
$\Delta p_x$ and $\Delta p_y$ to further improve exclusive channel
selection. The cuts $|\Delta p_x|<0.2$ and $|\Delta p_y|<0.2$ correspond
roughly to 4-5 $\sigma$.

![Exclusive distributions for events with at least one electron, proton
and two
photons.](figures/eppi0.exclusive.pdf "fig:"){#fig:ptdistributions
width="0.47\\linewidth"} ![Exclusive distributions for events with at
least one electron, proton and two
photons.](figures/eppi0.exclusive.pdf "fig:"){#fig:ptdistributions
width="0.47\\linewidth"}

The exclusive distributions after tight $M_{\gamma\gamma}$ mass and
transverse missing momenta cuts are shown on
Fig. [2.10](#fig:rawexclusive3){reference-type="ref"
reference="fig:rawexclusive3"} and display much stronger signal peaks on
top of reduced background.

![Exclusive distributions after tight $M_{\gamma\gamma}$ mass and
transverse missing momenta cuts
.](figures/eppi0.exclusive.pdf "fig:"){#fig:rawexclusive3
width="0.45\\linewidth"} ![Exclusive distributions after tight
$M_{\gamma\gamma}$ mass and transverse missing momenta cuts
.](figures/eppi0.exclusive.pdf "fig:"){#fig:rawexclusive3
width="0.45\\linewidth"}

![Exclusive distributions after tight $M_{\gamma\gamma}$ mass and
transverse missing momenta cuts
.](figures/eppi0.exclusive.pdf "fig:"){#fig:rawexclusive3
width="0.45\\linewidth"} ![Exclusive distributions after tight
$M_{\gamma\gamma}$ mass and transverse missing momenta cuts
.](figures/eppi0.exclusive.pdf "fig:"){#fig:rawexclusive3
width="0.45\\linewidth"}

### $\theta_{X\pi}$ cut determination

The cut on angle between expected and reconstructed pion is used in
order to further reduce background. To choose the value of the
$\theta_{X\pi}$ cut the $MM^2(epX)$ distribution is analyzed at multiple
$\theta_{X\pi}$ cut values and fit using gaussian+polynomial function as
shown on Fig. [2.16](#fig:mm2fordifferenttheta){reference-type="ref"
reference="fig:mm2fordifferenttheta"}. From the fit we can estimate the
number of good exclusive events (gaussian) and the number of background
events (polynomial) and their dependence on $\theta_{X\pi}$ cut.
Fig. [2.22](#fig:sigbgvsthetacutQ2){reference-type="ref"
reference="fig:sigbgvsthetacutQ2"}
and [2.27](#fig:sigbgvsthetacutxB){reference-type="ref"
reference="fig:sigbgvsthetacutxB"} show the numbers of signal and
background events as functions of $\theta_{X\pi}$ cut value for multiple
bins in $Q^2$ and $x_B$. These plots show that the cut
$\theta_{X\pi}<2^\circ$ allows to select the most number of good events
with the least background, and relaxing it beyond $2^\circ$ does not
gain us any good exclusive events but increases background.

![$MM^2(epX)$ distributions for multiple $\theta_{X\pi}$ cut
values.](figures/sigbg_eppi0.pdf "fig:"){#fig:mm2fordifferenttheta
width="0.3\\linewidth"} ![$MM^2(epX)$ distributions for multiple
$\theta_{X\pi}$ cut
values.](figures/sigbg_eppi0.pdf "fig:"){#fig:mm2fordifferenttheta
width="0.3\\linewidth"} ![$MM^2(epX)$ distributions for multiple
$\theta_{X\pi}$ cut
values.](figures/sigbg_eppi0.pdf "fig:"){#fig:mm2fordifferenttheta
width="0.3\\linewidth"}

![$MM^2(epX)$ distributions for multiple $\theta_{X\pi}$ cut
values.](figures/sigbg_eppi0.pdf "fig:"){#fig:mm2fordifferenttheta
width="0.3\\linewidth"} ![$MM^2(epX)$ distributions for multiple
$\theta_{X\pi}$ cut
values.](figures/sigbg_eppi0.pdf "fig:"){#fig:mm2fordifferenttheta
width="0.3\\linewidth"} ![$MM^2(epX)$ distributions for multiple
$\theta_{X\pi}$ cut
values.](figures/sigbg_eppi0.pdf "fig:"){#fig:mm2fordifferenttheta
width="0.3\\linewidth"}

![The numbers of signal (red markers) and background (black markers)
events as functions of $\theta_{X\pi}$ cut value for multiple $Q^2$
bins.](figures/sigbg_eppi0.pdf "fig:"){#fig:sigbgvsthetacutQ2
width="0.32\\linewidth"} ![The numbers of signal (red markers) and
background (black markers) events as functions of $\theta_{X\pi}$ cut
value for multiple $Q^2$
bins.](figures/sigbg_eppi0.pdf "fig:"){#fig:sigbgvsthetacutQ2
width="0.32\\linewidth"} ![The numbers of signal (red markers) and
background (black markers) events as functions of $\theta_{X\pi}$ cut
value for multiple $Q^2$
bins.](figures/sigbg_eppi0.pdf "fig:"){#fig:sigbgvsthetacutQ2
width="0.32\\linewidth"}

![The numbers of signal (red markers) and background (black markers)
events as functions of $\theta_{X\pi}$ cut value for multiple $Q^2$
bins.](figures/sigbg_eppi0.pdf "fig:"){#fig:sigbgvsthetacutQ2
width="0.32\\linewidth"} ![The numbers of signal (red markers) and
background (black markers) events as functions of $\theta_{X\pi}$ cut
value for multiple $Q^2$
bins.](figures/sigbg_eppi0.pdf "fig:"){#fig:sigbgvsthetacutQ2
width="0.32\\linewidth"} ![The numbers of signal (red markers) and
background (black markers) events as functions of $\theta_{X\pi}$ cut
value for multiple $Q^2$
bins.](figures/sigbg_eppi0.pdf "fig:"){#fig:sigbgvsthetacutQ2
width="0.32\\linewidth"}

![The numbers of signal (red markers) and background (black markers)
events as functions of $\theta_{X\pi}$ cut value for multiple $x_B$
bins.](figures/sigbg_eppi0.pdf "fig:"){#fig:sigbgvsthetacutxB
width="0.32\\linewidth"} ![The numbers of signal (red markers) and
background (black markers) events as functions of $\theta_{X\pi}$ cut
value for multiple $x_B$
bins.](figures/sigbg_eppi0.pdf "fig:"){#fig:sigbgvsthetacutxB
width="0.32\\linewidth"} ![The numbers of signal (red markers) and
background (black markers) events as functions of $\theta_{X\pi}$ cut
value for multiple $x_B$
bins.](figures/sigbg_eppi0.pdf "fig:"){#fig:sigbgvsthetacutxB
width="0.32\\linewidth"}

![The numbers of signal (red markers) and background (black markers)
events as functions of $\theta_{X\pi}$ cut value for multiple $x_B$
bins.](figures/sigbg_eppi0.pdf "fig:"){#fig:sigbgvsthetacutxB
width="0.32\\linewidth"} ![The numbers of signal (red markers) and
background (black markers) events as functions of $\theta_{X\pi}$ cut
value for multiple $x_B$
bins.](figures/sigbg_eppi0.pdf "fig:"){#fig:sigbgvsthetacutxB
width="0.32\\linewidth"}

### Final exclusivity cuts

The list of final exclusive cuts is following:

-   $\Delta p_x<0.2$ GeV

-   $\Delta p_y<0.2$ GeV

-   $\theta_{X\pi}<2^\circ$

-   $0.096<M_{\gamma\gamma}<0.168$ GeV

-   $MM^2(epX)<0.5$ GeV$^2$

Exclusive distributions after all exclusivity cut except $MM^2(epX)<0.5$
GeV are shown on Fig. [2.30](#fig:finalexclusive){reference-type="ref"
reference="fig:finalexclusive"}

![Exclusive distributions after all exclusivity cuts
.](figures/eppi0.exclusive.pdf "fig:"){#fig:finalexclusive
width="0.32\\linewidth"} ![Exclusive distributions after all exclusivity
cuts .](figures/eppi0.exclusive.pdf "fig:"){#fig:finalexclusive
width="0.32\\linewidth"} ![Exclusive distributions after all exclusivity
cuts .](figures/eppi0.exclusive.pdf "fig:"){#fig:finalexclusive
width="0.32\\linewidth"}

Results
=======

Kinematic coverage and binning
------------------------------

r0.35 ![image](figures/eppi0.inb.root.bins.pdf){width="0.97\\linewidth"}

The $Q^2$ vs $x_B$ 2D distribution is shown on
Fig. [\[fig:Q2vsxb\]](#fig:Q2vsxb){reference-type="ref"
reference="fig:Q2vsxb"} for exclusive $ep\rightarrow ep\pi^0$ events. 5
$Q^2$ vs $x_B$ bins are chosen to have two lowest $Q^2$ bins with
kinematic values similar to CLAS6 data. Each of $\{Q^2,x_B\}$ bin was
split into 3 $-t$ bins, and each of 3D $\{Q^2,x_B,-t\}$ bins was split
into 9 equidistant $\phi$ bins.

-   $2<Q^2<2.56$ GeV

    -   3 $\left<-t\right>$ bins:
        $[0, 0.39], [0.39, 0.71], [0.71, 2]$ GeV$^2$

-   $2.56<Q^2<3.8$ GeV

    -   3 $\left<-t\right>$ bins:
        $[0, 0.47], [0.47, 0.87], [0.87, 2]$ GeV$^2$

-   $3.8<Q^2<4.8$ GeV

    -   3 $\left<-t\right>$ bins:
        $[0, 0.57], [0.57, 0.99], [0.99, 2]$ GeV$^2$

-   $4.8<Q^2<6$ GeV

    -   3 $\left<-t\right>$ bins:
        $[0, 0.67], [0.67, 1.09], [1.09, 2]$ GeV$^2$

-   $6<Q^2<11$ GeV

    -   3 $\left<-t\right>$ bins:
        $[0, 0.91], [0.91, 1.37], [1.37, 2]$ GeV$^2$

5 2D distributions of $-t$ vs $\phi$ for each of $\{Q^2,x_B\}$ bins are
shown on Fig. [3.5](#fig:tphibins){reference-type="ref"
reference="fig:tphibins"}.

![The distribution for $-t$ vs $\phi$ for 5 $\{Q^2,x_B\}$ bins of
inbending dataset.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:tphibins
width="0.32\\linewidth"} ![The distribution for $-t$ vs $\phi$ for 5
$\{Q^2,x_B\}$ bins of inbending
dataset.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:tphibins
width="0.32\\linewidth"} ![The distribution for $-t$ vs $\phi$ for 5
$\{Q^2,x_B\}$ bins of inbending
dataset.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:tphibins
width="0.32\\linewidth"}

![The distribution for $-t$ vs $\phi$ for 5 $\{Q^2,x_B\}$ bins of
inbending dataset.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:tphibins
width="0.32\\linewidth"} ![The distribution for $-t$ vs $\phi$ for 5
$\{Q^2,x_B\}$ bins of inbending
dataset.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:tphibins
width="0.32\\linewidth"}

. [\[fig:tphibins\]]{#fig:tphibins label="fig:tphibins"}

Beam Spin Asymmetry
-------------------

$$BSA=\frac{1}{P_b}\frac{n^+-n^-}{n^++n^-}$$ where $P_b$ is average beam
polarization, $n^{+(-)}$ is the number of exclusive events in each 4D
$\{Q^2,x_B,-t,\phi\}$ bin with sideband background subtracted.

### Sideband background subtraction

Exclusivity cuts provide a very effective way to clean the data sample
but a fraction of background events still pass all exclusivity cuts and
needs to be taken into account. These events are clearly visible on the
plot of invariant mass of two photons as a linear background underneath
gaussian peak, as shown on
Fig. [3.20](#fig:mgginq2xbtt){reference-type="ref"
reference="fig:mgginq2xbtt"}. The number of events are counted in
$[-5\sigma,-3\sigma]$ and $[3\sigma,5\sigma]$ regions and multiplied by
1.5 to estimate the number of events underneath the $[-3\sigma,3\sigma]$
region of gaussian peak. The total number of exclusive events is taken
as:
$$n=N^{[-3\sigma,3\sigma]}-1.5\left(N^{[-5\sigma,-3\sigma]}+N^{3\sigma,5\sigma}\right)$$

![The distribution for $M_{\gamma\gamma}$ events for each of 15
$\{Q^2,x_B,-t\}$ bins of inbending dataset. Each row corresponds to
individual $\{Q^2,x_B\}$ bin with 3 $-t$
bins.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:mgginq2xbtt
width="0.32\\linewidth"} ![The distribution for $M_{\gamma\gamma}$
events for each of 15 $\{Q^2,x_B,-t\}$ bins of inbending dataset. Each
row corresponds to individual $\{Q^2,x_B\}$ bin with 3 $-t$
bins.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:mgginq2xbtt
width="0.32\\linewidth"} ![The distribution for $M_{\gamma\gamma}$
events for each of 15 $\{Q^2,x_B,-t\}$ bins of inbending dataset. Each
row corresponds to individual $\{Q^2,x_B\}$ bin with 3 $-t$
bins.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:mgginq2xbtt
width="0.32\\linewidth"}

![The distribution for $M_{\gamma\gamma}$ events for each of 15
$\{Q^2,x_B,-t\}$ bins of inbending dataset. Each row corresponds to
individual $\{Q^2,x_B\}$ bin with 3 $-t$
bins.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:mgginq2xbtt
width="0.32\\linewidth"} ![The distribution for $M_{\gamma\gamma}$
events for each of 15 $\{Q^2,x_B,-t\}$ bins of inbending dataset. Each
row corresponds to individual $\{Q^2,x_B\}$ bin with 3 $-t$
bins.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:mgginq2xbtt
width="0.32\\linewidth"} ![The distribution for $M_{\gamma\gamma}$
events for each of 15 $\{Q^2,x_B,-t\}$ bins of inbending dataset. Each
row corresponds to individual $\{Q^2,x_B\}$ bin with 3 $-t$
bins.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:mgginq2xbtt
width="0.32\\linewidth"}

![The distribution for $M_{\gamma\gamma}$ events for each of 15
$\{Q^2,x_B,-t\}$ bins of inbending dataset. Each row corresponds to
individual $\{Q^2,x_B\}$ bin with 3 $-t$
bins.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:mgginq2xbtt
width="0.32\\linewidth"} ![The distribution for $M_{\gamma\gamma}$
events for each of 15 $\{Q^2,x_B,-t\}$ bins of inbending dataset. Each
row corresponds to individual $\{Q^2,x_B\}$ bin with 3 $-t$
bins.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:mgginq2xbtt
width="0.32\\linewidth"} ![The distribution for $M_{\gamma\gamma}$
events for each of 15 $\{Q^2,x_B,-t\}$ bins of inbending dataset. Each
row corresponds to individual $\{Q^2,x_B\}$ bin with 3 $-t$
bins.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:mgginq2xbtt
width="0.32\\linewidth"}

![The distribution for $M_{\gamma\gamma}$ events for each of 15
$\{Q^2,x_B,-t\}$ bins of inbending dataset. Each row corresponds to
individual $\{Q^2,x_B\}$ bin with 3 $-t$
bins.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:mgginq2xbtt
width="0.32\\linewidth"} ![The distribution for $M_{\gamma\gamma}$
events for each of 15 $\{Q^2,x_B,-t\}$ bins of inbending dataset. Each
row corresponds to individual $\{Q^2,x_B\}$ bin with 3 $-t$
bins.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:mgginq2xbtt
width="0.32\\linewidth"} ![The distribution for $M_{\gamma\gamma}$
events for each of 15 $\{Q^2,x_B,-t\}$ bins of inbending dataset. Each
row corresponds to individual $\{Q^2,x_B\}$ bin with 3 $-t$
bins.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:mgginq2xbtt
width="0.32\\linewidth"}

![The distribution for $M_{\gamma\gamma}$ events for each of 15
$\{Q^2,x_B,-t\}$ bins of inbending dataset. Each row corresponds to
individual $\{Q^2,x_B\}$ bin with 3 $-t$
bins.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:mgginq2xbtt
width="0.32\\linewidth"} ![The distribution for $M_{\gamma\gamma}$
events for each of 15 $\{Q^2,x_B,-t\}$ bins of inbending dataset. Each
row corresponds to individual $\{Q^2,x_B\}$ bin with 3 $-t$
bins.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:mgginq2xbtt
width="0.32\\linewidth"} ![The distribution for $M_{\gamma\gamma}$
events for each of 15 $\{Q^2,x_B,-t\}$ bins of inbending dataset. Each
row corresponds to individual $\{Q^2,x_B\}$ bin with 3 $-t$
bins.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:mgginq2xbtt
width="0.32\\linewidth"}

### Results

The sideband background is subtracted for each helicity state and each
$\{Q^2,x_B,-t,\phi\}$ 4D bin, and beam spin asymmetry is calculated for
each bin as shown on Fig. [3.35](#fig:bsaq2xbtt){reference-type="ref"
reference="fig:bsaq2xbtt"}

![Beam spin asymmetry as a function of $\phi$ for each of 15
$\{Q^2,x_B,-t\}$ bins for inbending dataset. Each row corresponds to
individual $\{Q^2,x_B\}$ bin with 3 $-t$ bins. Fit with $\alpha sin\phi$
function.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:bsaq2xbtt
width="0.32\\linewidth"} ![Beam spin asymmetry as a function of $\phi$
for each of 15 $\{Q^2,x_B,-t\}$ bins for inbending dataset. Each row
corresponds to individual $\{Q^2,x_B\}$ bin with 3 $-t$ bins. Fit with
$\alpha sin\phi$
function.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:bsaq2xbtt
width="0.32\\linewidth"} ![Beam spin asymmetry as a function of $\phi$
for each of 15 $\{Q^2,x_B,-t\}$ bins for inbending dataset. Each row
corresponds to individual $\{Q^2,x_B\}$ bin with 3 $-t$ bins. Fit with
$\alpha sin\phi$
function.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:bsaq2xbtt
width="0.32\\linewidth"}

![Beam spin asymmetry as a function of $\phi$ for each of 15
$\{Q^2,x_B,-t\}$ bins for inbending dataset. Each row corresponds to
individual $\{Q^2,x_B\}$ bin with 3 $-t$ bins. Fit with $\alpha sin\phi$
function.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:bsaq2xbtt
width="0.32\\linewidth"} ![Beam spin asymmetry as a function of $\phi$
for each of 15 $\{Q^2,x_B,-t\}$ bins for inbending dataset. Each row
corresponds to individual $\{Q^2,x_B\}$ bin with 3 $-t$ bins. Fit with
$\alpha sin\phi$
function.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:bsaq2xbtt
width="0.32\\linewidth"} ![Beam spin asymmetry as a function of $\phi$
for each of 15 $\{Q^2,x_B,-t\}$ bins for inbending dataset. Each row
corresponds to individual $\{Q^2,x_B\}$ bin with 3 $-t$ bins. Fit with
$\alpha sin\phi$
function.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:bsaq2xbtt
width="0.32\\linewidth"}

![Beam spin asymmetry as a function of $\phi$ for each of 15
$\{Q^2,x_B,-t\}$ bins for inbending dataset. Each row corresponds to
individual $\{Q^2,x_B\}$ bin with 3 $-t$ bins. Fit with $\alpha sin\phi$
function.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:bsaq2xbtt
width="0.32\\linewidth"} ![Beam spin asymmetry as a function of $\phi$
for each of 15 $\{Q^2,x_B,-t\}$ bins for inbending dataset. Each row
corresponds to individual $\{Q^2,x_B\}$ bin with 3 $-t$ bins. Fit with
$\alpha sin\phi$
function.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:bsaq2xbtt
width="0.32\\linewidth"} ![Beam spin asymmetry as a function of $\phi$
for each of 15 $\{Q^2,x_B,-t\}$ bins for inbending dataset. Each row
corresponds to individual $\{Q^2,x_B\}$ bin with 3 $-t$ bins. Fit with
$\alpha sin\phi$
function.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:bsaq2xbtt
width="0.32\\linewidth"}

![Beam spin asymmetry as a function of $\phi$ for each of 15
$\{Q^2,x_B,-t\}$ bins for inbending dataset. Each row corresponds to
individual $\{Q^2,x_B\}$ bin with 3 $-t$ bins. Fit with $\alpha sin\phi$
function.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:bsaq2xbtt
width="0.32\\linewidth"} ![Beam spin asymmetry as a function of $\phi$
for each of 15 $\{Q^2,x_B,-t\}$ bins for inbending dataset. Each row
corresponds to individual $\{Q^2,x_B\}$ bin with 3 $-t$ bins. Fit with
$\alpha sin\phi$
function.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:bsaq2xbtt
width="0.32\\linewidth"} ![Beam spin asymmetry as a function of $\phi$
for each of 15 $\{Q^2,x_B,-t\}$ bins for inbending dataset. Each row
corresponds to individual $\{Q^2,x_B\}$ bin with 3 $-t$ bins. Fit with
$\alpha sin\phi$
function.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:bsaq2xbtt
width="0.32\\linewidth"}

![Beam spin asymmetry as a function of $\phi$ for each of 15
$\{Q^2,x_B,-t\}$ bins for inbending dataset. Each row corresponds to
individual $\{Q^2,x_B\}$ bin with 3 $-t$ bins. Fit with $\alpha sin\phi$
function.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:bsaq2xbtt
width="0.32\\linewidth"} ![Beam spin asymmetry as a function of $\phi$
for each of 15 $\{Q^2,x_B,-t\}$ bins for inbending dataset. Each row
corresponds to individual $\{Q^2,x_B\}$ bin with 3 $-t$ bins. Fit with
$\alpha sin\phi$
function.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:bsaq2xbtt
width="0.32\\linewidth"} ![Beam spin asymmetry as a function of $\phi$
for each of 15 $\{Q^2,x_B,-t\}$ bins for inbending dataset. Each row
corresponds to individual $\{Q^2,x_B\}$ bin with 3 $-t$ bins. Fit with
$\alpha sin\phi$
function.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:bsaq2xbtt
width="0.32\\linewidth"}

The relation between beam spin asymmetry and structure functions is
following:
$$BSA = \sqrt{2\epsilon(1-\epsilon)}\frac{\sigma_{LT'}}{\sigma_{0}}$$

where $\epsilon$ is beam energy dependent, so to compare results with
measurements from other experiments we should extract the ratio of
structure functions:
$$\frac{\sigma_{LT'}}{\sigma_{0}} = \frac{BSA}{\sqrt{2\epsilon(1-\epsilon)}}$$

The ratio of structure functions is shown on
Fig. [3.40](#fig:slts0inq2xb){reference-type="ref"
reference="fig:slts0inq2xb"} for each of 5 $\{Q^2,x_B\}$ bins as a
function of $-t$. The BSA measurements from CLAS 6GeV experiments are
plotted for comparison for existing low $\{Q^2,x_B\}$ bins.

![$\frac{\sigma_{LT'}}{\sigma_T}$ as a function of $-t$ for 5
$\{Q^2,x_B\}$ bins. Black markers are for the inbending dataset, red
markers are for outbending dataset, blue markers are for BSA
measurements from
CLAS6.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:slts0inq2xb
width="0.32\\linewidth"} ![$\frac{\sigma_{LT'}}{\sigma_T}$ as a function
of $-t$ for 5 $\{Q^2,x_B\}$ bins. Black markers are for the inbending
dataset, red markers are for outbending dataset, blue markers are for
BSA measurements from
CLAS6.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:slts0inq2xb
width="0.32\\linewidth"} ![$\frac{\sigma_{LT'}}{\sigma_T}$ as a function
of $-t$ for 5 $\{Q^2,x_B\}$ bins. Black markers are for the inbending
dataset, red markers are for outbending dataset, blue markers are for
BSA measurements from
CLAS6.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:slts0inq2xb
width="0.32\\linewidth"}

![$\frac{\sigma_{LT'}}{\sigma_T}$ as a function of $-t$ for 5
$\{Q^2,x_B\}$ bins. Black markers are for the inbending dataset, red
markers are for outbending dataset, blue markers are for BSA
measurements from
CLAS6.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:slts0inq2xb
width="0.32\\linewidth"} ![$\frac{\sigma_{LT'}}{\sigma_T}$ as a function
of $-t$ for 5 $\{Q^2,x_B\}$ bins. Black markers are for the inbending
dataset, red markers are for outbending dataset, blue markers are for
BSA measurements from
CLAS6.](figures/eppi0.inb.root.bsa.pdf "fig:"){#fig:slts0inq2xb
width="0.32\\linewidth"}

Simulations
===========

NOTES TO SELF: physics motivation data sets before event selection PID
exclusive cuts results to show 1 slide of what needs to go from here to
cross section

Generator and Simulations
-------------------------

Simulations were processed to better understand the results of the
exclusive data analysis. GEMC was used to process generated events
through the CLAS12 fall 2018 RG-A configuration. Specifically, a
generator based off the GK model and CLAS6 data - aao_norad[^1] - was
used to generate 4 million DV$\pi^0$P events and ran through GEMC with
the fall 2018 inbending configuration. Following the standard decoding
and reconstruction code flow, the resultant .hipo files were then
ready[^2] to be analyzed the same way that the data was.

The results from the simulation are compared to the results from
processing the 174 runs of 2018 Fall inbending data[^3] through the same
analysis scripts. For the sake of comparison, the vertical scale of the
simulated results is scaled by the ratio of the total number of observed
exclusive events from data to those from the simulation. Further note
that we do not expect a good match between data and simulation before
exclusivity cuts, because this simulation contained no background.
Finally, this study only considers events wherein the proton was
detected in the forward detector; the central detector is excluded
entirely at this point in time.\
Overall, the simulation and data show a good level of agreement both in
terms of kinematics and exclusivity. As the agreement is reasonable,
effort can proceed to undergo acceptance and other studies to work
towards an absolute cross section determination.

Comparison to Data: Basic Kinematics
------------------------------------

Here we show some example plots of basic particle kinematics. The polar
and azimuthal angle distributions of the protons and electrons agreed
well.

![Electron (top) and proton (bottom) phi distributions, before
exclusivity cuts (left) and after (right) for data (blue) and simulation
(red)](figures/Simulation/kinematics_basic/hist_electron_phi_nocut_fd_Double.pdf){width="100%"}

![Electron (top) and proton (bottom) phi distributions, before
exclusivity cuts (left) and after (right) for data (blue) and simulation
(red)](figures/Simulation/kinematics_basic/hist_electron_phi_excut_fd_Double.pdf){width="100%"}

![Electron (top) and proton (bottom) phi distributions, before
exclusivity cuts (left) and after (right) for data (blue) and simulation
(red)](figures/Simulation/kinematics_basic/hist_proton_phi_nocut_fd_Double.pdf){width="100%"}

![Electron (top) and proton (bottom) phi distributions, before
exclusivity cuts (left) and after (right) for data (blue) and simulation
(red)](figures/Simulation/kinematics_basic/hist_proton_phi_excut_fd_Double.pdf){width="100%"}

![Electron (top) and proton (bottom) theta distributions, before
exclusivity cuts (left) and after (right) for data (blue) and simulation
(red)](figures/Simulation/kinematics_basic/hist_electron_theta_nocut_fd_Double.pdf){width="100%"}

![Electron (top) and proton (bottom) theta distributions, before
exclusivity cuts (left) and after (right) for data (blue) and simulation
(red)](figures/Simulation/kinematics_basic/hist_electron_theta_excut_fd_Double.pdf){width="100%"}

![Electron (top) and proton (bottom) theta distributions, before
exclusivity cuts (left) and after (right) for data (blue) and simulation
(red)](figures/Simulation/kinematics_basic/hist_proton_theta_nocut_fd_Double.pdf){width="100%"}

![Electron (top) and proton (bottom) theta distributions, before
exclusivity cuts (left) and after (right) for data (blue) and simulation
(red)](figures/Simulation/kinematics_basic/hist_proton_theta_excut_fd_Double.pdf){width="100%"}

Comparison to Data: Kinematics - Scattering Variables
-----------------------------------------------------

The distributions of kinematic variables $x_B$, $Q^2$, W, and t all
again showed reasonable agreement between data and simulations. Notably,
here we can see that the distributions from the simulations vary
considerably from the data before any exclusivity cuts, but as mentioned
previously this is expected as the simulation has no background. There
is good agreement after exclusivity cuts.

### Bjorken X and $Q^2$ Distributions

![$x_B$ (top) and $Q^2$ (bottom) distributions, before exclusivity cuts
(left) and after (right) for data (blue) and simulation
(red)](figures/Simulation/kinematics_advanced/hist_xb_nocut_fd_Double.pdf){width="100%"}

![$x_B$ (top) and $Q^2$ (bottom) distributions, before exclusivity cuts
(left) and after (right) for data (blue) and simulation
(red)](figures/Simulation/kinematics_advanced/hist_xb_excut_fd_Double.pdf){width="100%"}

![$x_B$ (top) and $Q^2$ (bottom) distributions, before exclusivity cuts
(left) and after (right) for data (blue) and simulation
(red)](figures/Simulation/kinematics_advanced/hist_q2_nocut_fd_Double.pdf){width="100%"}

![$x_B$ (top) and $Q^2$ (bottom) distributions, before exclusivity cuts
(left) and after (right) for data (blue) and simulation
(red)](figures/Simulation/kinematics_advanced/hist_q2_excut_fd_Double.pdf){width="100%"}

### W and t Distributions

The outgoing 4-momenta W and the squared momentum transferred to the
proton t similarly show reasonable overlap after exclusivity cuts are
made. The W distribution before exclusivity cuts appears to be very
different between data and simulation, but this is just because the
simulated results had to be scaled up by a large factor to be visible in
comparison with the real data, which has a significant amount of
background before cuts.

![W (top) and t (bottom) distributions, before exclusivity cuts (left)
and after (right) for data (blue) and simulation
(red)](figures/Simulation/kinematics_advanced/hist_w_nocut_fd_Double.pdf){width="100%"}

![W (top) and t (bottom) distributions, before exclusivity cuts (left)
and after (right) for data (blue) and simulation
(red)](figures/Simulation/kinematics_advanced/hist_w_excut_fd_Double.pdf){width="100%"}

![W (top) and t (bottom) distributions, before exclusivity cuts (left)
and after (right) for data (blue) and simulation
(red)](figures/Simulation/kinematics_advanced/hist_kinematic_t_nocut_fd_Double.pdf){width="100%"}

![W (top) and t (bottom) distributions, before exclusivity cuts (left)
and after (right) for data (blue) and simulation
(red)](figures/Simulation/kinematics_advanced/hist_kinematic_t_excut_fd_Double.pdf){width="100%"}

Comparison to Data: Reconstructed Pion and Exclusivity
------------------------------------------------------

### Pion Mass and Energy

The pion mass distribution shows particularly good overlap between data
and simulation, indicating that the method of reconstruction for pions
is performing well.

![Pion mass (top) and energy (bottom) distributions, before exclusivity
cuts (left) and after (right) for data (blue) and simulation
(red)](figures/Simulation/exclusivity/hist_pion_mass_prexcut_fd_Double.pdf){width="100%"}

![Pion mass (top) and energy (bottom) distributions, before exclusivity
cuts (left) and after (right) for data (blue) and simulation
(red)](figures/Simulation/exclusivity/hist_pion_mass_excut_fd_Double.pdf){width="100%"}

![Pion mass (top) and energy (bottom) distributions, before exclusivity
cuts (left) and after (right) for data (blue) and simulation
(red)](figures/Simulation/exclusivity/hist_pion_energy_prexcut_fd_Double.pdf){width="100%"}

![Pion mass (top) and energy (bottom) distributions, before exclusivity
cuts (left) and after (right) for data (blue) and simulation
(red)](figures/Simulation/exclusivity/hist_pion_energy_excut_fd_Double.pdf){width="100%"}

### Missing Mass

Figure [4.6](#fig:MM){reference-type="ref" reference="fig:MM"} shows
missing mass distributions for (epX) and (ep$\gamma \gamma$) systems.
(epX) is calculated by summing the four-momenta of the incoming electron
and proton, and subtracting the four-momenta of the outgoing electron
and proton. For an exclusive $ep\pi^0$ event, the missing mass squared
of (epX) should equal just the $\pi^0$ mass squared, 0.02 GeV$^2$.
(ep$\gamma \gamma$) is calculated similarly; summing the four-momenta of
the incoming electron and proton, and subtracting the four-momenta of
the outgoing electron, proton, and two photons constituting the
candidate reconstructed $\pi^0$. For an exclusive event, the missing
mass should be exactly zero. In both cases, the data and simulation are
close to the expected value, and show a high degree of overlap.

![Missing mass squared (epX) (top row and middle row (zoomed on middle
row)) and missing mass squared (ep$\gamma \gamma$ distributions, before
exclusivity cuts (left) and after (right) for data (blue) and simulation
(red)](figures/Simulation/exclusivity/hist_missing_mass_squared_epX_prexcut_fd_Double.pdf){#fig:MM
width="100%"}

![Missing mass squared (epX) (top row and middle row (zoomed on middle
row)) and missing mass squared (ep$\gamma \gamma$ distributions, before
exclusivity cuts (left) and after (right) for data (blue) and simulation
(red)](figures/Simulation/exclusivity/hist_missing_mass_squared_epX_excut_fd_Double.pdf){#fig:MM
width="100%"}

![Missing mass squared (epX) (top row and middle row (zoomed on middle
row)) and missing mass squared (ep$\gamma \gamma$ distributions, before
exclusivity cuts (left) and after (right) for data (blue) and simulation
(red)](figures/Simulation/exclusivity/hist_missing_mass_squared_epX_zoomed_prexcut_fd_Double.pdf){#fig:MM
width="100%"}

![Missing mass squared (epX) (top row and middle row (zoomed on middle
row)) and missing mass squared (ep$\gamma \gamma$ distributions, before
exclusivity cuts (left) and after (right) for data (blue) and simulation
(red)](figures/Simulation/exclusivity/hist_missing_mass_squared_epX_zoomed_excut_fd_Double.pdf){#fig:MM
width="100%"}

![Missing mass squared (epX) (top row and middle row (zoomed on middle
row)) and missing mass squared (ep$\gamma \gamma$ distributions, before
exclusivity cuts (left) and after (right) for data (blue) and simulation
(red)](figures/Simulation/exclusivity/hist_missing_mass_squared_epgg_prexcut_fd_Double.pdf){#fig:MM
width="100%"}

![Missing mass squared (epX) (top row and middle row (zoomed on middle
row)) and missing mass squared (ep$\gamma \gamma$ distributions, before
exclusivity cuts (left) and after (right) for data (blue) and simulation
(red)](figures/Simulation/exclusivity/hist_missing_mass_squared_epgg_excut_fd_Double.pdf){#fig:MM
width="100%"}

Missing Energy
--------------

Finally, [4.10](#fig:ME){reference-type="ref" reference="fig:ME"} shows
the missing energy distributions for the (epX) and (ep$\gamma \gamma$)
systems. For exclusive $ep\pi^0$ events, $MM_{ep\gamma\gamma}$ = 0, and
we do indeed see a peak centered around 0 for this distribution, with a
strong agreement between data and simulation.

![Missing energy (epx) (top) and missing energy (epgg) (bottom)
distributions, before exclusivity cuts (left) and after (right) for data
(blue) and simulation
(red)](figures/Simulation/exclusivity/hist_missing_energy_epx_prexcut_fd_Double.pdf){#fig:ME
width="100%"}

![Missing energy (epx) (top) and missing energy (epgg) (bottom)
distributions, before exclusivity cuts (left) and after (right) for data
(blue) and simulation
(red)](figures/Simulation/exclusivity/hist_missing_energy_epx_excut_fd_Double.pdf){#fig:ME
width="100%"}

![Missing energy (epx) (top) and missing energy (epgg) (bottom)
distributions, before exclusivity cuts (left) and after (right) for data
(blue) and simulation
(red)](figures/Simulation/exclusivity/hist_missing_energy_epgg_prexcut_fd_Double.pdf){#fig:ME
width="100%"}

![Missing energy (epx) (top) and missing energy (epgg) (bottom)
distributions, before exclusivity cuts (left) and after (right) for data
(blue) and simulation
(red)](figures/Simulation/exclusivity/hist_missing_energy_epgg_excut_fd_Double.pdf){#fig:ME
width="100%"}

Appendix
========

Cross check between our results
-------------------------------

Bobby and I have made the comparison of exclusive events on event by
event basis:

                                              Total number of events   events with $n_e\ge1$, $n_p\ge1$ in FD   DV$\pi$P events with $p$ in FD
  ------------------------------------------ ------------------------ ---------------------------------------- --------------------------------
  EB + Exclusivity                                                                                             
  \(35510297\)                                                                                                 
  \(22975374\)                                                                                                 
  \(25174\)                                                                                                    
  EB + min $E_\gamma$ + noFT + Exclusivity                                                                     
  \(35510297\)                                                                                                 
  \(22975374\)                                                                                                 
  \(21429\)                                                                                                    
  Bobby's result, Andrey's result                                                                              

Other Simulation Results
------------------------

### Lepton-Hadron Angle

![Angle between lepton and hadron planes, before exclusivity cuts (left)
and after (right) for data (blue) and simulation
(red)](figures/Simulation/exclusivity/hist_lept_had_angle_prexcut_fd_Double.pdf){width="100%"}

![Angle between lepton and hadron planes, before exclusivity cuts (left)
and after (right) for data (blue) and simulation
(red)](figures/Simulation/exclusivity/hist_lept_had_angle_excut_fd_Double.pdf){width="100%"}

[^1]: https://github.com/drewkenjo/aao_norad

[^2]: /volatile/clas12/kenjo/cache/

[^3]: /cache/clas12/rg-a/production/recon/fall2018/torus-1/pass1/v0/dst/train/skim8/
