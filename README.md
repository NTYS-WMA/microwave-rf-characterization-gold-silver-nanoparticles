# Microwave RF Characterization of Aqueous Gold and Silver Nanoparticle Solutions Using USRP N210 Measurements and HFSS Simulation

This repository hosts a technical report on the microwave RF characterization of aqueous gold and silver nanoparticle solutions using software-defined radio measurements and electromagnetic simulation.

The project investigates whether Ultra-High Frequency (UHF) radio sensing can detect concentration-dependent differences in aqueous nanoparticle samples, motivated by the longer-term possibility of developing more accessible and non-invasive sensing approaches for health diagnostics. The study combines HFSS simulation, physical RF measurements using a USRP N210 SDR, signal-processing techniques, and machine learning classification to evaluate whether gold and silver nanoparticle solutions produce measurable RF signatures.

> This repository contains the PDF report only. Source code, raw measurement data, and simulation files are not included. If you are interested in the underlying methodology, data, or simulation workflow, please feel free to contact me through my GitHub profile or by opening an issue in this repository.

## Report

📄 **Download / View the Report:**
[`microwave-rf-characterization-aqueous-gold-silver-nanoparticles-usrp-n210-hfss.pdf`](./microwave-rf-characterization-aqueous-gold-silver-nanoparticles-usrp-n210-hfss.pdf)

## Abstract

Chronic Kidney Disease (CKD) motivates interest in sensing approaches that could support earlier and more accessible monitoring outside conventional laboratory workflows. As an initial feasibility study toward this broader goal, this project investigates whether UHF radio sensing can detect concentration-dependent differences in aqueous gold and silver nanoparticle solutions, viewed as candidate contrast-agent systems, by measuring transmitted and reflected radio waves.

The study shows that measurable concentration-dependent RF signatures can be extracted under controlled laboratory conditions, although the trends are not consistently detected across all experimental settings. Nevertheless, the measured data supports multiclass classification across the different experimental setups, suggesting that future work could refine the experimental parameters and improve the prospects of RF sensing as a viable and accessible diagnostic tool.

## Project Scope

The report covers:

* HFSS simulation of UHF response for nanoparticle samples
* Transmission and reflection RF measurement setups
* USRP N210 and SBX-40 software-defined radio measurement workflow
* RF signal processing using I/Q phasors
* Baseband offset correction and carrier frequency offset correction
* Standard sample bracketing for improved measurement robustness
* Experimental comparison of aqueous gold and silver nanoparticle solutions
* Statistical analysis of concentration-dependent RF magnitude and phase trends
* Random forest classification of nanoparticle type and concentration level

## Technical Summary

The study first uses HFSS simulation to explore the expected RF response of nanoparticle solutions across the 1.5–2.5 GHz UHF range. Based on the simulation results, 1.8 GHz is selected as the main operating frequency for physical experiments.

Physical measurements are then conducted using an Ettus USRP N210 with an SBX-40 daughterboard. Both transmission and reflection configurations are tested. The RF signals are processed as complex I/Q phasors, from which magnitude and phase are extracted. Because the expected sample-induced RF differences are weak, the methodology includes several correction and normalization steps, including offset-frequency demodulation, carrier frequency offset correction, phasor aggregation, and standard sample bracketing.

The experimental results show that measurable RF differences can be extracted across nanoparticle types and concentration levels, although the observed trends are not uniformly monotonic across all setups. A random forest classifier is then used to evaluate whether the processed RF features contain enough discriminative information for multiclass classification.

## Main Findings

* Aqueous gold and silver nanoparticle solutions produced measurable RF magnitude and phase differences under controlled laboratory conditions.
* HFSS simulations suggested that the 1.8 GHz region was suitable for further physical testing.
* Transmission and reflection measurements showed concentration-dependent RF behaviour, although not all trends were consistently monotonic.
* Processed magnitude and phase features supported multiclass classification across the experimental settings.
* The strongest classification performance was observed in the reflection measurement setting for gold nanoparticle samples.
* The results suggest that UHF RF sensing may be a promising exploratory direction, but further work is needed to improve measurement stability, refine the physical setup, and validate the approach on more biologically representative samples.

## Keywords

USRP N210, SBX-40, software-defined radio, SDR sensing, RF sensing, microwave RF characterization, UHF sensing, gold nanoparticles, silver nanoparticles, aqueous nanoparticle solutions, AuNP, AgNP, HFSS simulation, RF attenuation, RF phase measurement, I/Q signal processing, carrier frequency offset correction, standard sample bracketing, random forest classification, non-invasive sensing, chronic kidney disease.

## Citation

If referencing this work, please cite it as:

```bibtex
@techreport{toh2026rfnanoparticles,
  title  = {Microwave RF Characterization of Aqueous Gold and Silver Nanoparticle Solutions Using USRP N210 Measurements and HFSS Simulation},
  author = {Toh, Yun Sheng Nelson},
  year   = {2026},
  institution = {National University of Singapore},
  type   = {Capstone Project Report}
}
```

## Author

**Toh Yun Sheng Nelson**
Master of Computing
National University of Singapore
2026

## Notes

This report is an exploratory feasibility study. It should not be interpreted as a clinically validated diagnostic method. The results are intended to support further investigation into RF-based sensing methods, nanoparticle contrast-agent systems, and accessible non-invasive diagnostic workflows.
