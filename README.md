# Functional-based-Causal-Discovery-Methods-Survey

This is the repository of function-based causal discovery methods.

# Table of Contents
-[Repository for FCM-Based Algorithms](#FCM-Based-repository)

-[Functional-based Causal Discovery Methods](#FCM-Based-Methods)

-[Causal Discovery Datasets](#datasets)

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

These methods are built on the independence between noise and causes, utilizing the asymmetry between noise and cause variables to identify the correct causal direction. This category of methods can further be divided into causal discovery methods based on linear functions and non-Gaussian noise  and causal discovery methods based on nonlinear function additive noise models, depending on the type of function and noise characteristics.

####  Causal Discovery based on Linear Non-Gaussian Acyclic Models

1. **ICA-LiNGAM:** [Shimizu S, Hoyer P O, Hyvärinen A, et al. A linear non-Gaussian acyclic model for causal discovery[J]. Journal of Machine Learning Research, 2006, 7(10).](https://www.jmlr.org/papers/volume7/shimizu06a/shimizu06a.pdf?ref=https://codemonkey.link)
 ([Code](https://github.com/cdt15/lingam))

2. **LvLiNGAM**: [Hoyer, P.O., Shimizu, S., Kerminen, A.J., Palviainen, M., 2008b. Estimation of causal effects using linear non-Gaussian causal models with hidden variables. International Journal of Approximate Reasoning 49, 362–378.](https://www.sciencedirect.com/science/article/pii/S0888613X08000212/pdfmd5=2a7ca67d29957e23e3eb545b146aa429&pid=1-s2.0-S0888613X08000212-main.pdf)
([Code](https://www.cs.helsinki.fi/u/phoyer/code/lvlingam.tar.gz))

3. **VAR-LiNGAM:** [Hyvärinen, A., Zhang, K., Shimizu, S., Hoyer, P.O., 2010. Estimation of a structural vector autoregression model using non-gaussianity. Journal of Machine Learning Research 11.](https://www.jmlr.org/papers/volume11/hyvarinen10a/hyvarinen10a.pdf)
([Code](https://github.com/cdt15/lingam/blob/master/lingam))

4. **DirectLiNGAM**: [Shimizu, S., Inazumi, T., Sogawa, Y., Hyvarinen, A., Kawahara, Y., Washio, T., Hoyer, P.O., Bollen, K., Hoyer, P., 2011. DirectLiNGAM: A direct method for learning a linear non-Gaussian structural equation model. Journal of Machine Learning Research-JMLR 12, 1225–1248.](https://www.jmlr.org/papers/volume12/shimizu11a/shimizu11a.pdf)
([Code](https://github.com/cdt15/lingam/tree/master/lingam))

 5. **LrLiNGAM**: [Hyvärinen, A., Smith, S.M., 2013. Pairwise likelihood ratios for estimation of non-Gaussian structural equation models. The Journal of Machine Learning Research 14, 111–152. Publisher: JMLR. org.](https://www.jmlr.org/papers/volume14/hyvarinen13a/hyvarinen13a.pdf)
([Code](https://www.cs.helsinki.fi/u/ahyvarin/code/pwcausal/pwling.zip))


6. **PClingam**：[Hoyer, P.O., Hyvarinen, A., Scheines, R., Spirtes, P.L., Ramsey, J., Lacerda, G., Shimizu, S., 2012. Causal discovery of linear acyclic models with arbitrary distributions. arXiv preprint arXiv:1206.3260.](https://arxiv.org/pdf/1206.3260)
([Code](https://github.com/cmu-phil/tetrad.))

7. **RCD**: [Maeda, T.N., Shimizu, S., 2020. Rcd: Repetitive causal discovery of linear non-gaussian acyclic models with latent confounders, in: International Conference on Artificial Intelligence and Statistics, PMLR. pp. 735–745.](http://proceedings.mlr.press/v108/maeda20a/maeda20a.pdf)
([Code](https://github.com/cdt15/lingam/tree/master/lingam.))

8. **MLCLiNGAM**: [Chen, W., Cai, R., Zhang, K., Hao, Z., 2021. Causal discovery in linear non-gaussian acyclic model with multiple latent confounders. IEEE Transactions on Neural Networks and Learning Systems 33, 2816–2827. Publisher: IEEE.](https://www.researchgate.net/profile/Ruichu-Cai/publication/348360267_Causal_Discovery_in_Linear_Non-Gaussian_Acyclic_Model_With_Multiple_Latent_Confounders/links/603d8dfd4585154e8c6e0687/Causal-Discovery-in-Linear-Non-Gaussian-Acyclic-Model-With-Multiple-Latent-Confounders.pdf)

9. **LiM**: [Zeng, Y., Shimizu, S., Matsui, H., Sun, F., 2022. Causal discovery for linear mixed data, in: Conference on Causal Learning and Reasoning, PMLR. pp. 994–1009.](https://proceedings.mlr.press/v177/zeng22a/zeng22a.pdf)
([Code](https://github.com/cdt15/lingam/tree/master/lingam))

10. **LiNGLaH**: [Xie, F., Huang, B., Chen, Z., He, Y., Geng, Z., Zhang, K., 2022. Identification of linear non-gaussian latent hierarchical structure, in: International Conference on Machine Learning, PMLR. pp. 24370–24387.](https://proceedings.mlr.press/v162/xie22a/xie22a.pdf)
([Code](https://media.icml.cc/Conferences/ICML2022/supplementary/xie22a-supp.zip))	

#### Causal Discovery based on Linear Non-Gaussian Acyclic Models

1. **ANM**: [Hoyer, P., Janzing, D., Mooij, J.M., Peters, J., Schölkopf, B., 2008a. Nonlinear causal discovery with additive noise models. Advances in neural information processing systems 21.](https://proceedings.neurips.cc/paper/2008/file/f7664060cc52bc6f3d620bcedc94a4b6-Paper.pdf)
([Code](https://github.com/huawei-noah/trustworthyAI/tree/master/gcastle/example/anm))

2. **PNL**: [Zhang, K., Hyvarinen, A., 2009. On the identifiability of the post-nonlinear causal model, in: Proceedings of the Twenty-Fifth Conference on Uncertainty in Artificial Intelligence (UAI2009).](https://arxiv.org/pdf/1205.2599)
([Code](https://github.com/huawei-noah/trustworthyAI/tree/master/gcastle/example/pnl))

3. **RESIT**: [Peters J, Mooij J M, Janzing D, et al. Causal discovery with continuous additive noise models[J]. 2014.](https://www.jmlr.org/papers/volume15/peters14a/peters14a.pdf)([Code](https://github.com/cdt15/lingam/tree/master/lingam.))

4. **CAM**: [Bühlmann, P., Peters, J., Ernest, J., 2014. CAM: Causal additive models, high-dimensional order search and penalized regression. The Annals of Statistics 42.](https://projecteuclid.org/journals/annals-of-statistics/volume-42/issue-6/CAM--Causal-additive-models-high-dimensional-order-search-and/10.1214/14-AOS1260.pdf)([Code](https://github.com/py-why/dodiscover/tree/main/dodiscover/toporder))

5. **SCL**: [Nowzohour, C., Bühlmann, P., 2016. Score-based causal learning in additive noise models. Statistics 50, 471–485. Publisher: Taylor & Francis.](https://arxiv.org/pdf/1311.6359)

6. **NonSENS**: [Monti, R.P., Zhang, K., Hyvärinen, A., 2020. Causal discovery with general non-linear relationships using non-linear ica, in: Uncertainty in artificial intelligence, PMLR. pp. 186–195.](http://proceedings.mlr.press/v115/monti20a/monti20a.pdf)

7. **CGNN**: [Goudet, O., Kalainathan, D., Caillou, P., Guyon, I., Lopez-Paz, D., Sebag, M., 2018. Learning functional causal models with generative neural networks. Explainable and interpretable models in computer vision and machine learning , 39–80Publisher: Springer.](https://link.springer.com/content/pdf/10.1007/978-3-319-98131-4_3.pdf?pdf=inline%20link)([Code](https://github.com/FenTechSolutions/CausalDiscoveryToolbox/tree/master/cdt/causality/graph))

8. **CANM**: [Cai, R., Qiao, J., Zhang, K., Zhang, Z., Hao, Z., 2019. Causal discovery with cascade nonlinear additive noise models. arXiv preprint arXiv:1905.09442 .](https://arxiv.org/pdf/1905.09442)([Code](https://github.com/DMIRLAB-Group/CANM))

9. **CCANM**: [Qiao, J., Cai, R., Zhang, K., Zhang, Z., Hao, Z., 2021. Causal Discovery with Confounding Cascade Nonlinear Additive Noise Models. ACM Transactions on Intelligent Systems and Technology 12, 80:1–80:28.](https://dl.acm.org/doi/fullHtml/10.1145/3482879)([Code](https://github.com/FenTechSolutions/CausalDiscoveryToolbox/tree/master/cdt/causality/graph))

10. **AbPNL**: [Uemura, K., Shimizu, S., 2020. Estimation of post-nonlinear causal models using autoencoding structure, in: ICASSP 2020-2020 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP), IEEE. pp. 3312–3316.](https://ieeexplore.ieee.org/abstract/document/9053468/)([Code](https://github.com/rafcc/abpnl/abpnl))

11. **Multi-PNL:** [Uemura, K., Takagi, T., Takayuki, K., Yoshida, H., Shimizu, S., 2022. A multivariate causal discovery based on post-nonlinear model, in: Conference on Causal Learning and Reasoning, PMLR. pp. 826–839.](https://proceedings.mlr.press/v177/uemura22a/uemura22a.pdf)([Code](https://github.com/rafcc/abpnl))

12. **SAM**: [Kalainathan, D., Goudet, O., Guyon, I., Lopez-Paz, D., Sebag, M., 2022. Structural agnostic modeling: Adversarial learning of causal graphs. The Journal of Machine Learning Research 23, 9831–9892. Publisher: JMLRORG.](https://www.jmlr.org/papers/volume23/19-529/19-529.pdf)([Code](https://github.com/Diviyan-Kalainathan/SAM))

13. **MissDAG**: [Gao, E., Ng, I., Gong, M., Shen, L., Huang, W., Liu, T., Zhang, K., Bondell, H., 2022. MissDAG: Causal discovery in the presence of missing data with continuous additive noise models. Advances in Neural Information Processing Systems 35, 5024–5038.](https://proceedings.neurips.cc/paper_files/paper/2022/file/206361867abf7eb01746c3943078da3c-Paper-Conference.pdf)([Code](https://github.com/ErdunGAO/MissDAG))

14. **SCORE**: [Rolland, P., Cevher, V., Kleindessner, M., Russell, C., Janzing, D., Schölkopf, B., Locatello, F., 2022. Score matching enables causal discovery of nonlinear additive noise models, in: International Conference on Machine Learning, PMLR. pp. 18741–18753.](https://proceedings.mlr.press/v162/rolland22a/rolland22a.pdf)([Code](https://github.com/paulrolland1307/SCORE))

15. **NoGAM**: [Montagna, F., Noceti, N., Rosasco, L., Zhang, K., Locatello, F., 2023a. Causal Discovery with Score Matching on Additive Models with Arbitrary Noise. Conference on Causal Learning and Reasoning .](https://arxiv.org/pdf/2304.03265)([Code](https://github.com/py-why/dodiscover/tree/main/dodiscover/toporder))

16. **DAS**: [Montagna, F., Noceti, N., Rosasco, L., Zhang, K., Locatello, F., 2023b. Scalable causal discovery with score matching. arXiv preprint arXiv:2304.03382 .](https://arxiv.org/pdf/2304.03382)([Code](https://github.com/py-why/dodiscover/tree/main/dodiscover/toporder))

17. **DiffAN**: [Sanchez, P., Liu, X., O’Neil, A.Q., Tsaftaris, S.A., 2022. Diffusion models for causal discovery via topological ordering. arXiv preprint arXiv:2210.06201 .](https://arxiv.org/pdf/2210.06201)([Code](https://github.com/vios-s/DiffAN))

### Causal Discovery based on Information Geometric Methods <a name="IG-methods"></a>

These methods utilize the asymmetry in information geometry to identify the causal direction of bivariate relationships. In other words, this class of methods determines causal direction by distinguishing the independence between the distribution of causes and the function mechanisms that map causes to effects.

1. **IGCI**: [Daniusis, P., Janzing, D., Mooij, J., Zscheischler, J., Steudel, B., Zhang, K., Schölkopf, B., 2012. Inferring deterministic causal relations. arXiv preprint arXiv:1203.3475 .](https://arxiv.org/pdf/1203.3475)([Code](https://webdav.tuebingen.mpg.de/causality/igci.tar.gz))

2. **GPI**: [Stegle, O., Janzing, D., Zhang, K., Mooij, J.M., Schölkopf, B., 2010. Probabilistic latent variable models for distinguishing between cause and effect. Advances in neural information processing systems 23.](https://proceedings.neurips.cc/paper/2010/file/c850371fda6892fbfd1c5a5b457e5777-Paper.pdf)([Code](https://webdav.tuebingen.mpg.de/causality/nips2010-gpi-code.tar.gz))

3. **RECI**: [Blöbaum, P., Janzing, D., Washio, T., Shimizu, S., Schölkopf, B., 2019. Analysis of cause-effect inference by comparing regression errors. PeerJ Computer Science 5, e169.](https://peerj.com/articles/cs-169.pdf)([Code](https://github.com/DMIRLAB-Group/FOM))

4. **FOM**: [Cai, R., Ye, J., Qiao, J., Fu, H., Hao, Z., 2020. Fom: Fourth-order moment based causal direction identification on the heteroscedastic data. Neural Networks 124, 193–201.](https://drive.google.com/file/d/1NV2D8KutbMCUTLSIdCh-FJEg2SLKyGel/view)([Code](https://github.com/DMIRLAB-Group/FOM))

5. **FIGCI**: [Zhang, S., Wu, J., Li, Z., Liu, L., Liao, J., Sun, L., 2022. Figci: Flow-based information-geometric causal inference, in: CAAI International Conference on Artificial Intelligence, Springer. pp. 520–531.](https://link.springer.com/chapter/10.1007/978-3-031-20500-2_43)

### Causal Discovery based on Hybrid Assumption Methods <a name="HS-methods"></a>

In certain practical scenarios, causal discovery algorithms often make overly strict assumptions that may not be suitable for specific data. Therefore, addressing how to relax the assumptions in causal discovery is also an important research direction. Below are some methods for breaking the functional causal assumption or combining linear non-Gaussian models.

1. **CANM:** [Mooij, J.M., Janzing, D., Heskes, T., Schölkopf, B., 2011. On causal discovery with cyclic additive noise models. Advances in neural information processing systems 24.](https://proceedings.neurips.cc/paper/2011/file/d61e4bbd6393c9111e6526ea173a7c8b-Paper.pdf)

2. **LiNG-D:** [Lacerda, G., Spirtes, P.L., Ramsey, J., Hoyer, P.O., 2012. Discovering cyclic causal models by independent components analysis. arXiv preprint arXiv:1206.3273 .](https://arxiv.org/pdf/1206.3273)([Code](https://github.com/cmu-phil/py-tetrad))

3. **GDSEEV:** [Peters, J., Bühlmann, P., 2014. Identifiability of Gaussian structural equation models with equal error variances. Biometrika 101, 219–228. Publisher: Oxford University Press.](https://arxiv.org/pdf/1205.2536)([Code](https://academic.oup.com/biomet/article/101/1/219/2364921#supplementary-data.))

4. **CCSCM:** [Nagase, M., Kano, Y., 2023. Cyclic structural causal model with unobserved confounder effect. Communications in Statistics-Theory and Methods 52, 335–345.](https://www.tandfonline.com/doi/abs/10.1080/03610926.2021.1913186)([Code](https://ndownloader.figstatic.com/files/27844229))


## Causal Discovery Datasets<a name="datasets"></a>

1. **Erdős-Rényi (ER) model:** [Erdős, P., Rényi, A., et al., 1960. On the evolution of random graphs. Publ. math. inst. hung. acad. sci 5, 17–60.](https://static.renyi.hu/~p_erdos/1960-10.pdf)

2. **Scale-Free (SF) model :** [Bollobás, B., Borgs, C., Chayes, J.T., Riordan, O., 2003. Directed scale-free graphs., in: SODA, pp. 132–139.](https://www.microsoft.com/en-us/research/publication/2016/11/Directed-scale-free-graphs.pdf)

3. **Synthetic Transcriptional Regulatory Network generator (SynTReN) :** [Van den Bulcke, T., Van Leemput, K., Naudts, B., van Remortel, P., Ma, H., Verschoren, A., De Moor, B., Marchal, K., 2006. Syntren: a generator of synthetic gene expression data for design and analysis of structure learning algorithms. BMC bioinformatics 7, 1–12.](https://link.springer.com/article/10.1186/1471-2105-7-43)

4. **CauseEffectPairs (CEP) dataset:** [Mooij, J.M., Peters, J., Janzing, D., Zscheischler, J., Schölkopf, B., 2016. Distinguishing cause from effect using observational data: methods and benchmarks. The Journal of Machine Learning Research 17, 1103–1204.](https://www.jmlr.org/papers/volume17/14-518/14-518.pdf)  ([Link](https://webdav.tuebingen.mpg.de/cause-effect/))

5. **SACHS dataset :** [Sachs, K., Perez, O., Pe’er, D., Lauffenburger, D.A., Nolan, G.P., 2005. Causal protein-signaling networks derived from multiparameter single-cell data. Science 308, 523–529.](https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=00417e4953374f0e8dc7ee217d15c3b1f95ddba4)([Link](https://www.bnlearn.com/bnrepository/))

6. **LUCAS (LUng CAncer Simple set):** [Guyon, I., Aliferis, C., Cooper, G., Elisseeff, A., Pellet, J.P., Spirtes, P., Statnikov, A., 2008. Design and analysis of the causation and prediction challenge, in: Causation and Prediction Challenge, PMLR. pp. 1–33.](http://proceedings.mlr.press/v3/guyon08a/guyon08a.pdf)([Link](https://www.causality.inf.ethz.ch/data/LUCAS.html))

7. **Functional Magnetic Resonance Imaging dataset (fMRI) :**[Smith, S.M., Miller, K.L., Salimi-Khorshidi, G., Webster, M., Beckmann, C.F., Nichols, T.E., Ramsey, J.D., Woolrich, M.W., 2011. Network modelling methods for fmri. Neuroimage 54, 875–891.](https://www.contrib.andrew.cmu.edu/org/fmri-research/Smith-FMRI-2011.pdf)

8. **Bayesian Network Repository :** This network repository contains multiple datasets with network sizes ranging from small networks (fewer than 20 nodes) to extremely large networks (more than 1000 nodes). It includes commonly used datasets in causal discovery such as [ASIA](http://www.eecis.udel.edu/~shatkay/Course/papers/Lauritzen1988.pdf), [ALARM](https://link.springer.com/chapter/10.1007/978-3-642-93437-7_28) , [CHILD](https://projecteuclid.org/journals/statistical-science/volume-8/issue-3/Bayesian-Analysis-in-Expert-Systems/10.1214/ss/1177010888.pdf), PIGS, and more. The repository is designed to provide researchers and practitioners with a variety of Bayesian network models for analyzing, modeling, and inferring various problems across different domains.([Link](https://www.bnlearn.com/bnrepository/))

