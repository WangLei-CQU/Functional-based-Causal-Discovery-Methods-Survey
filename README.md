# Functional-based-Causal-Discovery-Methods-Survey

This is the repository of function-based causal discovery methods.

# Table of Contents
-[Repository for FCM-Based Algorithms](#FCM-Based-repository)

-[Functional-based Causal Discovery Methods](#FCM-Based-Methods)

## Repository for FCM-Based Algorithms <a name="FCM-Based-repository"></a>

| Repository         | Available FCM-based algorithms                                                                                                                                                                               |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Lingam](https://sites.google.com/view/sshimizu06/lingam)         | ICA-LiNGAM , DirectLiNGAM , MultiGroupDirectLiNGAM , VAR-LiNGAM , VARMALiNGAM , longitudinal LiNGAM , CAM , RESIT , RCD , MD-LiNA , LiM                             | 
| [gCastle](https://github.com/huawei-noah/trustworthyAI)       | ANM , ICA-LiNGAM , DirectLiNGAM , PNL                                                                                                                                                       |
| [CDT](https://github.com/FenTechSolutions/CausalDiscoveryToolbox)            | CAM , CGNN , SAM , IGCI , ICA-LiNGAM , ANM , RECI                                                                                                                             |
| [causal-learn](https://github.com/py-why/causal-learn)   | ICA-LiNGAM , DirectLiNGAM , ANM , PNL , CAM , VARMALiNGAM , longitudinal LiNGAM , MultiGroupDirectLiNGAM , RCD                                                         |
| [dodiscover](https://github.com/py-why/dodiscover)    | CAM , DAS , NoGAM , SOCRE                                                                                                                                                                  |

## Functional-based Causal Discovery Methods <a name="FCM-Based-Methods"></a>

**Overview of Approaches Based on Functional Causal Models**

Methods based on additive noise are further divided into Linear Non-Gaussian Acyclic Models (upper part) and Nonlinear Additive Noise Models (lower part).

Each column represents assumptions regarding:
- Function type, categorized as Linear, Nonlinear, or Arbitrary type
- Variable count, categorized as Multivariate, Bivariate, or overlap (both Multivariate and Bivariate)
- Disturbance type assumptions, categorized as Gaussian, Non-Gaussian, or Arbitrary type
- Whether the no confounding assumption (Sufficiency, Suff. (abbr)) is satisfied
- Whether the faithfulness assumption (Faith. (abbr), ✓ -- denote related assumption) is satisfied
- Whether the Acyclicity (Ac. (abbr)) assumption is satisfied
- Methods output, categorized as DAG and causal direction (Causal-Effect, CE).


| Category                                 | Methods (Abbr) | Year | Functional | count-Variable | Disturbance | Suff. | Faith. | Ac. | Output |
|------------------------------------------|-----------------|------|------------|----------------|-------------|-------|--------|-----|--------|
| CD based on Addition Noise Model          | ICA-LiNGAM      | 2006 | Linear     | Multivariate   | Non-Gaussian | ✓     | ✓      | ✓   | DAG    |
|                                          | LvLiNGAM        | 2008 | Linear     | Multivariate   | Non-Gaussian | ✗     | ✓      | ✓   | DAG    |
|                                          | VAR-LiNGAM      | 2010 | Linear     | Multivariate   | Non-Gaussian | ✓     | ✓      | ✓   | DAG    |
|                                          | DirectLiNGAM    | 2011 | Linear     | Multivariate   | Non-Gaussian | ✓     | ✓      | ✓   | DAG    |
|                                          | LrLiNGAM        | 2013 | Linear     | Bivariate      | Non-Gaussian | ✓     | ✓      | ✓   | CE     |
|                                          | Pclingam        | 2012 | Linear     | Multivariate   | Non-Gaussian | ✓     | ✓      | ✓   | DAG    |
|                                          | RCD             | 2020 | Linear     | Multivariate   | Non-Gaussian | ✗     | ✓      | ✓   | DAG    |
|                                          | MLCLiNGAM       | 2021 | Linear     | Multivariate   | Non-Gaussian | ✗     | ✓      | ✓   | DAG    |
|                                          | LiM             | 2022 | Linear     | Multivariate   | Non-Gaussian | ✓     | ✓      | ✓   | DAG    |
|                                          | LiNGLaH         | 2022 | Linear     | Multivariate   | Non-Gaussian | ✗     | ✓      | ✓   | DAG    |
|                                          | ANM             | 2008 | Arbitrary  | Bivariate      | Arbitrary    | ✓     | ✓      | ✓   | CE     |
|                                          | PNL             | 2009 | Nonlinear  | Bivariate      | Arbitrary    | ✓     | ✓      | ✓   | CE     |
|                                          | RESIT           | 2014 | Nonlinear  | Overlap         | Gaussian     | ✓     | ✓      | ✓   | Overlap |
|                                          | CAM             | 2014 | Arbitrary  | Multivariate   | Gaussian     | ✓     | ✓      | ✓   | DAG    |
|                                          | SCL             | 2016 | Nonlinear  | Bivariate      | Non-Gaussian | ✓     | ✓      | ✓   | CE     |
|                                          | NonSENS         | 2020 | Nonlinear  | Bivariate      | Arbitrary    | ✓     | ✓      | ✓   | CE     |
|                                          | CGNN            | 2018 | Nonlinear  | Multivariate   | Arbitrary    | ✓     | ✓      | ✓   | DAG    |
|                                          | CCAM & CCANM    | 2019 | Nonlinear  | Bivariate      | Arbitrary    | ✗     | ✓      | ✓   | CE     |
|                                          | AbPNL           | 2020 | Nonlinear  | Bivariate      | Arbitrary    | ✓     | ✓      | ✓   | CE     |
|                                          | Multi-PNL        | 2022 | Nonlinear  | Multivariate   | Arbitrary    | ✓     | ✓      | ✓   | DAG    |
|                                          | SAM             | 2022 | Nonlinear  | Multivariate   | Arbitrary    | ✓     | ✓      | ✓   | DAG    |
|                                          | MissDAG         | 2022 | Nonlinear  | Multivariate   | Arbitrary    | ✓     | ✓      | ✓   | DAG    |
|                                          | SCORE           | 2022 | Nonlinear  | Multivariate   | Gaussian     | ✓     | ✓      | ✓   | DAG    |
|                                          | NoGAM           | 2023 | Nonlinear  | Multivariate   | Arbitrary    | ✓     | ✓      | ✓   | DAG    |
|                                          | DAS             | 2023 | Nonlinear  | Multivariate   | Gaussian     | ✓     | ✓      | ✓   | DAG    |
|                                          | DiffAN          | 2023 | Nonlinear  | Multivariate   | Gaussian     | ✓     | ✓      | ✓   | DAG    |
| Information Geometric                     | GPI             | 2010 | Arbitrary  | Bivariate      | Gaussian     | ✓     | ✓      | ✓   | CE     |
|                                          | IGCI            | 2012 | Arbitrary  | Bivariate      | Arbitrary    | ✓     | ✓      | ✓   | CE     |
|                                          | RECI            | 2018 | Arbitrary  | Bivariate      | Arbitrary    | ✓     | ✓      | ✓   | CE     |
|                                          | FOM             | 2020 | Arbitrary  | Bivariate      | Gaussian     | ✓     | ✓      | ✓   | CE     |
|                                          | FIGCI           | 2022 | Arbitrary  | Bivariate      | Arbitrary    | ✓     | ✓      | ✓   | CE     |
| Hybrid Assumption Methods                  | CANM            | 2011 | Nonlinear  | Bivariate      | Gaussian     | ✓     | ✓      | ✗   | CE     |
|                                          | LiNG-D          | 2012 | Linear     | Multivariate   | Non-Gaussian | ✓     | ✓      | ✗   | DAG    |
|                                          | GDSEEV          | 2014 | Linear     | Multivariate   | Gaussian     | ✓     | ✓      | ✓   | DAG    |
|                                          | CCSCM           | 2023 | Nonlinear  | Bivariate      | Gaussian     | ✗     | ✓      | ✗   | CE     |

Causal discovery methods based on the Functional Causal Model (FCM) can be broadly categorized into Additive Noise-based Methods, Information Geometric Methods, and Hybrid Assumption Methods.

-[Causal Discovery based on Additive Noise Model Methods](#ANM-methods)

-[Causal Discovery based on Information Geometric Methods](#IG-methods)

-[Causal Discovery based on Hybrid Assumption Methods](#HS-methods)

### Causal Discovery based on Additive Noise Model Methods <a name="ANM-methods"></a>

|Category | Abbreviation | Paper Name | Year
| ---------------------------------|------------------|-------------------------------------------------------------------------------------------|----------------------------------
|Linear Non-Gaussian Acyclic Models|
|                                  | ICA-LiNGAM       | 
|                                  | LvLiNGAM         |
|                                  | VAR-LiNGAM       |
|                                  |                  |
|Nonlinear Additive Noise Models   |
|                                  |



### Causal Discovery based on Information Geometric Methods <a name="IG-methods"></a>

### Causal Discovery based on Hybrid Assumption Methods <a name="HS-methods"></a>

| Abbreviation | Paper Name | 
