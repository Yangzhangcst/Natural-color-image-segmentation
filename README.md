# Natural/color image segmentation
A paper list of natural/color image segmentation.

*Last updated: 2020/07/04

#### Update log
*2020/March* - update all of recent papers and make some diagram about history of natural/color image segmentation.  
*2020/July* - update some recent papers and codes.  

##

## Table of Contents
- [Datasets](https://github.com/Yangzhangcst/Natural-color-image-segmentation/blob/master/README.md#Datasets)
- [Metrics](https://github.com/Yangzhangcst/Natural-color-image-segmentation/blob/master/README.md#Metrics)
- [Performance tables](https://github.com/Yangzhangcst/Natural-color-image-segmentation/blob/master/README.md#Performance-tables)
- [Paper list](https://github.com/Yangzhangcst/Natural-color-image-segmentation/blob/master/README.md#paper-list)

##

## Datasets

The papers related to datasets used mainly in natural/color image segmentation are as follows.

- **[`[BSDS300]`](http://www.eecs.berkeley.edu/Research/Projects/CS/vision/grouping/segbench)** Berkeley segmentation dataset 300 includes 300 natural images and the ground truth data. Each image has a ﬁxed size of 481×321 pixels. 

- **[`[BSDS500]`](https://www2.eecs.berkeley.edu/Research/Projects/CS/vision/grouping/resources.html)** Berkeley segmentation dataset 500 is  an improved version of BSDS300 dataset. the BSDS500 contains 500 natural images. Each image is annotated by 5 different people on average.

- **[`[MSRC]`](https://www.microsoft.com/en-us/research/project/image-understanding/?from=http%3A%2F%2Fresearch.microsoft.com%2Fvision%2Fcambridge%2Frecognition%2F)** Microsoft Research Cambridge v2 dataset  contains 591 images and 23 object classes with accurate pixel-wise labeled images.

##

## Metrics

The papers related to metrics used mainly in natural/color image segmentation are as follows.

- **[PRI]** Probabilistic rand index 
- **[VOI]** Variation of information
- **[GCE]** Global consistency error
- **[BDE]** Boundary displacement error 
- **[SC]** Segmentation Cover
- **[F]** F-measure 


##

## Performance tables

Speed  is related to the hardware spec(e.g. CPU, GPU, RAM, etc), so it is hard to make an equal comparison. We select six indexs namely PRI, VoI, GCE, BDE, SC, and F-measure to make comparison. The closer   the segmentation result is to the ground truth, the higher the PRI, SC and F-measure are, and the smaller the other three measures are.

### BSDS300 (\*test set)

|   Method  | PRI | VoI | GCE | BDE | SC | F | Published | Year |
|:---------:|:---:|:---:|:---:|:---:|:--:|:---------:|:------------:|--------------|
| **2DNLMeKGSA** | 0.6079 | 2.8078 | 0.3352 | 10.2407 |  |  | EAAI | 2018 |
| **gPb-Hoiem\***  (in [HO-CC]) | 0.614 | 2.847 |  | 13.533 | 0.353 | | IJCV | 2007 |
| **FH** (in [CCP]) | 0.7139 | 3.3949 | 0.1746 | 16.67 |	0.51 |  | IJCV | 2004 |
| **2DKLMPSO** | 0.7154 | 5.6802 | 0.4173 | 9.9382  |  |  | APS | 2016 |
| **Ncut** | 0.7242 | 2.9061 | 0.2232 |  17.15  | 0.53 (in[LSI]) |  | TPAMI | 2000 |
|     **WCP**     | 0.7496 | 2.4399 | 0.2392 | 15.7416 |              |                |   ICIP    | 2013 |
|    **FRFCM**    |  0.75  |  2.62  |  0.36  |  12.87  | 0.46 |  | TFS | 2018 |
| **MNCut** | 0.7559 | 2.4701 | 0.1925 |  15.10  |              | 0.595\* (in [HO-CC]) | CVPR | 2005 |
| **LDCQP** | 0.7592 | 2.1212 |        | 13.8691 |              |                | ICDMW | 2015 |
| **CTM** | 0.760  |  2.02  |  0.19  |  8.99   |              |                 |   CVIU    | 2008 |
|         **SuperParsing**         | 0.7628 | 2.0387 | 0.2178 |  15.05  |              |                 |   ECCV    | 2010 |
|    **JSEG** (in [UHIS_FEM]) | 0.7756 | 2.3217 | 0.1989 |  14.40  |              |                 |   TPAMI   | 2001 |
|             **SDTV**             | 0.7758 | 1.8165 | 0.1768 |  16.24  |     0.57     |                 |   ICCV    | 2009 |
|           **UHIS_FEM**           | 0.7769 | 2.3067 | 0.2215 |  10.66  |              |                 |    PR     | 2017 |
| **FusionTP** (in [UHIS_FEM]) | 0.7771 | 3.3089 | 0.3654 | 13.2428 |              |                 |   NIPS    | 2012 |
|          **SFFCM**           |  0.78  |  2.02  |  0.26  |  12.90  |     0.55     |                 |    TFS    | 2019 |
|           **CCP**            |  0.79  |  2.89  |  0.13  |  10.21  |     0.47     |                 |   ICCV    | 2015 |
|             **FBTS**             |  0.79  |  2.10  |        |         |              |      0.62       |    TIP    | 2015 |
|           **TDC**            | 0.7926 | 2.0870 | 0.1835 | 13.1710 |              |                 |   CVPR    | 2014 |
| **Context-sensitive**  (in [GL-GRAPH]) | 0.7937 | 3.9174 | 0.4165 | 9.9046  |              |                 |   TPAMI   | 2010 |
|     **Meanshift**  (in [CCP])     | 0.7958 | 1.9725 | 0.1888 |  14.41  |     0.54     | 0.512\* (in [HO-CC]) |   TPAMI   | 2002 |
|        **NTP** (in [GL-GRAPH])        | 0.7974 | 2.1130 | 0.2171 |  13.58  |              |                 |   CVPR    | 2008 |
| **LSI** | 0.80 |  |  |  | 0.59 | | PR | 2016 |
| **CMMH** | 0.80 | 2.16 |        | 10.20 |              |                | BMVC | 2018 |
| **GCEBFM** |  0.80  |  2.10  |  0.19  |  8.73   |              |                   | ICIP | 2016 |
| **MOBFM** | 0.80 | 1.98 | 0.20 | 8.25 | | | ICPR | 2016 |
| **PRIF** | 0.80 | 1.97 | 0.21 | 8.45 | | | TIP | 2010 |
| **FMBFM** | 0.80 | 1.88 | 0.20 | 9.30 | |  | IJSIP | 2014 |
| **ATP** | 0.8039 | 2.0210 | 0.2066 | 13.7700 | | | TIP | 2014 |
| **TBES** (in [UHIS_FEM]) | 0.8070 | 1.7050 | 0.1812 | 10.71 | | 0.64  (in [FBTS]) | IJCV | 2011 |
| **H\_+R\_Better** | 0.8073 | 1.8260 | 0.2079 | 12.16 | | | PR | 2018 |
| **Co-transduction** (in [GL-GRAPH]) | 0.8083 | 2.3644 | 0.2681 | 14.1972 | | | TIP | 2012 |
| **Corr-Cluster\*** | 0.81 | 1.83 |        | 11.19 | 0.60 | 0.71 | TIP | 2013 |
| **RIS-HL** | 0.8137 | 1.8232 | 0.1805 | 13.07 | 0.59 | | BMVC | 2014 |
| **HO-CC\*** | 0.8140 | 1.7430 |        | 10.3770 | 0.599 | 0.722 | TPAMI | 2014 |
| **LFPA** | 0.8146 | 1.8545 | 0.1809 | 12.21 | 0.53 | | TPAMI | 2013 |
| **TSESC** | 0.8205 | 1.9520 | 0.1998 | 12.09 | | | CVPR | 2011 |
| **TPG** | 0.8227 | 1.7696 |        |         | | | CVPR | 2011 |
| **gPb-owt-ucm\***  (in [SASFinal]) | 0.825 | 1.971 | | 9.995 | 0.579 | 0.726 | TPAMI | 2011 |
| **ISM** | 0.83 | 2.16 | 0.1650 | 11.65 | | | MTA | 2016 |
| **FSHA** | 0.83 | 1.71 |        |         | | | ICIAP | 2015 |
| **SAS** | 0.8319 | 1.6849 | 0.1779 | 11.29 | 0.61 (in [SASFinal]) | | CVPR | 2012 |
| **GTD** | 0.8331 | 1.6390 | 0.1655 | 10.3720 | | | IJCAI | 2015 |
| **L0-GRAPH** | 0.8355 | 1.9935 | 0.2297 | 11.19 | | | ICIP | 2013 |
| **GL-GRAPH** | 0.8384 | 1.8012 | 0.1934 | 10.6633 | | | TIP | 2015 |
| **CCP-LAM** | 0.8404 | 1.5715 | 0.1635 | 10.20 | 0.68 | | ICCV | 2015 |
| **SASFinal** | 0.8437 | 1.4977 |  |  | 0.6301 | | ICIP | 2014 |
| **CCP-LAS** | 0.8442 | 1.5871 | 0.1582 | 10.4600 | 0.68 | | ICCV | 2015 |
| **AASP-GRAPH** | 0.8446 | 1.6485 | 0.1737 | 14.6416 |  | | ICME | 2019 |
| **EA-Graph** | 0.8459 | 1.6774 | 0.1845 | 11.2638 | | | IEICE-TIS | 2019 |
| **SHST** | 0.8470 | 1.4500 | 0.1470 | 18.29 | | | IVCNZ | 2016 |
| **CCM** | 0.8500 | 1.6300 | 0.1790 | 12.30 | | | ICIP | 2014 |
| **CDS** | 0.8539 | 1.5712 | 0.1572 | 10.18 | 0.68 | | TIP | 2017 |
| **ISCC** | 0.86 | 1.66 | | | 0.65 | | Neurocom. | 2016 |


### BSDS500 (\*test set)

|   Method  | PRI | VoI | GCE | BDE | SC | F | Published | Year |
|:---------:|:---:|:---:|:---:|:---:|:--:|:---------:|:------------:|--------------|
| **HTFCM** | 0.6745 |        | 0.4165 | 14.4682 | 0.3546 |  | PR | 2011 |
| **HAFCM** | 0.7435 | | 0.2515 | 15.4481 | 0.442 | | ASC | 2013 |
| **RFHA** | 0.7511 | | 0.235 | 14.3887 | 0.4224 | | ASC | 2013 |
| **MNCut\***(in [LMS_GLA]) | 0.758 | 2.327 |  |  | 0.428 | 0.598 | CVPR | 2005 |
| **FRFCM** | 0.76 | 2.67 | 0.37 | 12.35 | 0.45 | | TFS | 2018 |
| **MMGR-AFCF** | 0.76 | 2.05 | 0.22 | 12.95 | 0.54 | | TFS | 2020 |
|        **HPCQ**         | 0.7787 | | 0.2104 | 12.8726 | 0.5356 | | IET-IP | 2014 |
|          **SFFCM**          | 0.78 | 2.06 |  0.26  |  12.8   |      0.54      | | TFS | 2019 |
| **HVAA** | 0.7866 | | 0.2077 | 12.5658 | 0.5334 | | ISOCC | 2018 |
| **Canny-UCM\*** (in [LMS_GLA]) | 0.79 | 2.19 |  |  | 0.49 | 0.6 | CVPRW | 2006 |
| **FH\*** (in [LMS_GLA]) | 0.791 | 2.159 |  |  | 0.527 | 0.622 | IJCV | 2004 |
| **Quick  Shift\*** (in [LMS_GLA]) | 0.792 | 2.17 |  |  | 0.518 | 0.599 | ECCV | 2008 |
| **SAS\*** (in [LMS_GLA]) | 0.801 | 1.917 |  |  | 0.525 | 0.643 | CVPR | 2012 |
| **CCP\*** (in [LMS_GLA]) | 0.802 | 2.277 | | | 0.528 | 0.665 | ICCV | 2015 |
| **LFPA\*** (in [LMS_GLA]) | 0.805 | 1.859 |  |  | 0.529 | 0.67 | TPAMI | 2013 |
| **LMS_GLA\*** | 0.807 | 1.981 | | | 0.555 | 0.643 | TCSVT | 2017 |
| **fPb-UCM\*** (in [LMS_GLA]) | 0.819 | 1.698 | | | 0.582 | 0.69 | TPAMI | 2013 |
| **gPb-owt-ucm\***(in [HO-CC]) | 0.825 | 1.971 |  | 9.995 | 0.579 | 0.726 | TPAMI | 2011 |
| **PW-CC\*** | 0.826 | 1.859 | | 9.812 | 0.589 | 0.728 | TPAMI | 2014 |
| **HO-CC\*** | 0.8280 | 1.7910 | | 9.7700 | 0.5950 | 0.73 | TPAMI | 2014 |
| **LRR(CH)** | 0.8295 | 1.7475 | |  | 0.5905 |  | ICCV | 2011 |
| **MCG** | 0.83 | 1.57 |  |  | 0.61 | | TPAMI | 2017 |
|      **SAS** (in [ISCC])      | 0.84 | 1.71 | | | 0.6 | | CVPR | 2012 |
| **CCM** | 0.841 | 2.04 | 0.236 | 10.78 | | | ICIP | 2014 |
| **SHST** | 0.845 | 1.47 | 0.148 | 19 |  | | IVCNZ | 2016 |
| **AMR** | 0.85 | 1.62 | | | 0.63 | | TIP | 2019 |
| **MLAP** | 0.8538 | 1.5311 | | | 0.6411 | | ICCV | 2011 |
| **ISCC** | 0.86 | 1.7 | | | 0.64 | | Neurocom. | 2016 |


### MSRC (\*test set)

|   Method  | PRI | VoI | GCE | BDE | SC | F | Published | Year |
|:---------:|:---:|:---:|:---:|:---:|:--:|:---------:|:------------:|--------------|
| **Supervised-Ncut\*** (in [HO-CC]) | 0.601 | 3.101 |  | 13.498 | 0.287 |  | NIPS | 2009 |
| **gPb-Hoiem\***  (in [HO-CC]) | 0.614 | 2.847 |  | 13.533 | 0.353 | | IJCV | 2007 |
| **MNCut\*** (in [HO-CC]) | 0.628 | 2.765 |  | 11.941 | 0.341 |  | CVPR | 2005 |
| **FRFCM** | 0.71 | 1.79 | 0.3 | 12.23 | 0.58 | | TFS | 2018 |
| **SuperParsing** (in [RIS-HL]) | 0.71 | 1.4 |      |        |        | | ECCV | 2010 |
|          **SFFCM**          | 0.73 | 1.58 |  0.25  | 12.49 |      0.62      | | TFS | 2019 |
| **Meanshift\***  (in [HO-CC]) | 0.734 | 1.649 |  | 13.944 | 0.606 | | TPAMI | 2002 |
| **TBES**  (in [RIS-HL]) | 0.76 | 1.49 |  |  |  | | IJCV | 2011 |
| **Corr-Cluster\*** | 0.773 | 1.648 |  | 9.194 | 0.632 |  | TIP | 2013 |
| **gPb-owt-ucm\*** (in [HO-CC]) | 0.779 | 1.675 |  | 9.8 | 0.628 |  | TPAMI | 2011 |
| **Joint-kernel** | 0.78 | 1.62 | |  |  |  | ACCV | 2012 |
| **RIS-HL** | 0.78 | 1.29 | |  |  |  | BMVC | 2014 |
| **HO-CC\*** | 0.784 | 1.594 | | 9.04 | 0.648 |  | TPAMI | 2014 |
| **LRR** | 0.7912 | 1.3002 | |  | 0.6932 |  | ICCV | 2011 |
| **SAS\*** (in [ISCC]) | 0.80 | 1.39 |  |  | 0.67 |      | CVPR | 2012 |
| **MLAP** | 0.8306 | 1.1656 | | | 0.7556 | | ICCV | 2011 |
| **ISCC** | 0.85 | 1.27 | | | 0.74 | | Neurocom. | 2016 |
##

## Paper list

- **[Ncut]** Jianbo, S. and J. Malik (2000). "Normalized cuts and image segmentation." **IEEE Transactions on Pattern Analysis and Machine Intelligence** 22(8): 888-905. [**[code]**](https://www.cis.upenn.edu/~jshi/software/)
- **[JSEG]** Deng, Y. and B. S. Manjunath (2001). "Unsupervised segmentation of color-texture regions in images and video." **IEEE Transactions on Pattern Analysis and Machine Intelligence** 23(8): 800-810.
- **[Meanshift]** Comaniciu, D. and P. Meer (2002). "Mean shift: a robust approach toward feature space analysis." **IEEE Transactions on Pattern Analysis and Machine Intelligence** 24(5): 603-619.
- **[FH]** Felzenszwalb, P. F. and D. P. Huttenlocher (2004). "Efficient graph-based image segmentation." **International Journal of Computer Vision** 59(2): 167-181. [**[code]**](http://cs.brown.edu/people/pfelzens/segment/)
- **[MNCut]** Cour, T., et al. (2005). Spectral segmentation with multiscale graph decomposition. **IEEE Conference on Computer Vision and Pattern Recognition** 1124-1131.
- **[Canny-UCM]** Arbelaez, P. (2006). Boundary extraction in natural images using ultra-metric contour maps. **IEEE Conference on Computer Vision and Pattern Recognition Workshop**: 182-182.
- **[gPb-Hoiem]** Hoiem, D., et al. (2007). "Recovering surface layout from an Image." **International Journal of Computer Vision** 75: 151–172.
- **[NTP]** Jingdong, W., et al. (2008). Normalized tree partitioning for image segmentation. **IEEE Conference on Computer Vision and Pattern Recognition**: 1-8.
- **[Quickshift]** Vedaldi, A. and S. Soatto (2008). Quick shift and kernel methods for mode seeking. **European Conference on Computer Vision**: 705-718. [**[code]**](http://www.vlfeat.org/overview/quickshift.html)
- **[CTM]** Yang, A. Y., et al. (2008). "Unsupervised segmentation of natural images via lossy data compression." **Computer Vision and Image Understanding** 110(2): 212-225.  [**[code]**](http://perception.csl.uiuc.edu/coding/image_segmentation/)
- **[SDTV]** Donoser, M., et al. (2009). Saliency driven total variation segmentation. **IEEE International Conference on Computer Vision**: 817-824.
- **[PRIF]** Mignotte, M. (2010). "A label field fusion Bayesian model and its penalized maximum rand estimator for image segmentation." **IEEE Transactions Image Processing** 19(6): 1610-1624. [**[code]**](http://www.iro.umontreal.ca/~mignotte/ResearchMaterial/PRIF-SourceCode/ProgPRIF.tar)
- **[SuperParsing]** Tighe, J. and S. Lazebnik (2010). SuperParsing: Scalable nonparametric image parsing with superpixels. **European Conference on Computer Vision**: 352-365.
- **[Context-sensitive]** Xiang, B., et al. (2010). "Learning context-sensitive shape similarity by graph transduction." **IEEE Transactions on Pattern Analysis and Machine Intelligence** 32(5): 861-874.
- **[gPb-owt-ucm]** Arbelaez, P., et al. (2011). "Contour detection and hierarchical image segmentation." **IEEE Transactions on Pattern Analysis and Machine Intelligence** 33(5): 898-916. [**[code]**](http://www.eecs.berkeley.edu/Research/Projects/CS/vision/grouping/resources.html)
- **[LRR & MLAP]** Cheng, B., et al. (2011). Multi-task low-rank affinity pursuit for image segmentation. **IEEE International Conference on Computer Vision**: 2439-2446.  
- **[TBES]** Mobahi, H., et al. (2011). "Segmentation of natural images by texture and boundary compression." **International Journal of Computer Vision** 95(1): 86-98.
- **[TPG]** Yang, X. and L. J. Latecki (2011). Affinity learning on a tensor product graph with applications to shape and image retrieval. **IEEE Conference on Computer Vision and Pattern Recognition**: 2369-2376. 
- **[Co-transduction]** Bai, X., et al. (2012). "Co-transduction for shape retrieval." **IEEE Transactions Image Processing** 21(5): 2747-2757.
- **[Joint Kernel]** Kim, J., et al. (2012). Joint kernel learning for supervised image segmentation. **Asian Conference on Computer Vision**.
- **[SAS]** Zhenguo, L., et al. (2012). Segmentation using superpixels: A bipartite graph partitioning approach. **IEEE Conference on Computer Vision and Pattern Recognition**: 789-796.
- **[FusionTP]** Zhou, Y., et al. (2012). Fusion with diffusion for robust visual tracking. **Advances in Neural Information Processing Systems**. 
- **[Corr-Cluster]** Kim, S., et al. (2013). "Task-specific image partitioning." **IEEE Transactions Image Processing** 22(2): 488-500.
- **[LFPA]** Kim, T. H., et al. (2013). "Learning full pairwise affinities for spectral segmentation." **IEEE Transactions on Pattern Analysis and Machine Intelligence** 35(7): 1690-1703.
- **[HAFCM]** Tan, K. S., et al. (2013). "Novel initialization scheme for Fuzzy C-Means algorithm on color image segmentation." **Applied Soft Computing** 13(4): 1832-1852.
- **[RFHA]** Tan, K. S., et al. (2013). "Color image segmentation using adaptive unsupervised clustering approach." **Applied Soft Computing** 13(4): 2017-2036.
- **[L0-GRAPH]** Wang, X., et al. (2013). A Graph-cut approach to image segmentation using an affinity graph based on &#x2113;\_0-sIncorporating texture information into region-based unsupervised image segmentation using textural superpixelsparse representation of features. **IEEE International Conference on Image Processing**: 4019-4023.
- **[WCP]** Wang, X., et al. (2013). Graph-based image segmentation using weighted color patch. **IEEE International Conference on Image Processing**: 4064-4068.
- **[HPCQ]** Cho, S. I., et al. (2014). "Human Perception-based image segmentation using optimising of colour quantisation." **IET Image Processing** 8(12): 761-770.
- **[CCM]** Gu, X., et al. (2014). Improving superpixel-based image segmentation by incorporating color covariance matrix manifolds. **IEEE International Conference on Image Processing**: 4403-4406.
- **[SASFinal]** Hsu, C.-Y., et al. (2014). Incorporating texture information into region-based unsupervised image segmentation using textural superpixels. **IEEE International Conference on Image Processing**: 4323-4327.
- **[ATP]** Jingdong, W., et al. (2014). "Regularized tree partitioning and its application to unsupervised image segmentation." **IEEE Transactions Image Processing** 23(4): 1909-1922.
- **[HO-CC]** Kim, S., et al. (2014). "Image segmentation using higher-order correlation clustering." **IEEE Transactions on Pattern Analysis and Machine Intelligence** 36(9): 1761-1774.
- **[FMBFM]** Mignotte, M. and C. Hélou (2014). "A Precision-recall criterion based consensus model for fusing multiple segmentations." **International Journal of Signal Processing, Image Processing and Pattern Recognition** 7(3): 61-82. [**[code]**](http://www.iro.umontreal.ca/~mignotte/ResearchMaterial/FMBFM-SourceCode/ProgFMBFM.tar.gz)
- **[RIS-HL]** Wu, J., et al. (2014). Reverse image segmentation: A high-level solution to a low-level task. **British Machine Vision Conference**. 
- **[LDCQP]** Chakeri, A. and L. O. Hall (2015). Large data clustering using quadratic programming: A comprehensive quantitative analysis. **IEEE International Conference on Data Mining Workshop**: 806-813. 
- **[CCP]** Fu, X., et al. (2015). Robust image segmentation using contour-guided color palettes. **IEEE International Conference on Computer Vision**: 1618-1625. [**[code]**](https://github.com/fuxiang87/MCL_CCP)
- **[FSHA]** Verdoja, F. and M. Grangetto (2015). Fast superpixel-based hierarchical approach to image segmentation. **International Conference on Image Analysis and Processing**: 364-374.
- **[GL-GRAPH]** Wang, X., et al. (2015). "A Global/local affinity graph for image segmentation." **IEEE Transactions Image Processing** 24(4): 1399-1411. [**[code]**](https://github.com/xiaofanglegoc/global-local-affinity-graph)
- **[FBTS]** Yuan, J., et al. (2015). "Factorization-based texture segmentation." **IEEE Transactions Image Processing** 24(11): 3488-3497.
- **[GTD]** Yu Z., et al. (2015). Generalized transitive distance with minimum spanning random forest. **International Joint Conference on Artificial Intelligence (IJCAI)**: 2205-2211.
- **[ISM]** Li, X., et al. (2016). "An integrated similarity metric for graph-based color image segmentation." **Multimedia Tools and Applications** 75(6): 2969-2987.
- **[LSI]** Dong, L., et al. (2016). "LSI: Latent semantic inference for natural image segmentation." **Pattern Recognition** 59: 282-291 
- **[SHST]** Gu, X., et al. (2016). A Hierarchical segmentation tree for superpixel-based image segmentation. **International Conference on Image and Vision Computing New Zealand(IVCNZ)**: 1-6.
- **[ISCC]** Huang, D., et al. (2016). "Ensembling over-segmentations: From weak evidence to strong segmentation." **Neurocomputing** 207: 416-427.
- **[GCEBFM]** Khelifi, L. and M. Mignotte (2016). GCE-based model for the fusion of multiples color image segmentations. **IEEE International Conference on Image Processing**: 2574-2578.
- **[MOBFM]** Khelifi, L. and M. Mignotte (2016). A multi-objective approach based on TOPSIS to solve the image segmentation combination problem. **IEEE International Conference on Pattern Recognition**: 4220-4225.
- **[2DKLMPSO]** Zhao, X., et al. (2016). "A multilevel image thresholding segmentation algorithm based on two-dimensional K–L divergence and modified particle swarm optimization." **Applied Soft Computing** 48: 151-159.
- **[LMS_GLA]** Cho, H., et al. (2017). "Image segmentation using linked mean-shift vectors and global/local attributes." **IEEE Transactions on Circuits and Systems for Video Technology** 27(10): 2132-2140.
- **[MCG]** Pont-Tuset, J., et al. (2017). "Multiscale combinatorial grouping for image segmentation and object proposal generation." **IEEE Transactions on Pattern Analysis and Machine Intelligence** 39(1): 128-140.
- **[UHIS_FEM]** Yin, S., et al. (2017). "Unsupervised hierarchical image segmentation through fuzzy entropy maximization." **Pattern Recognition** 68: 245-259.
- **[CDS]** Fu, X.,et al. (2017). "Image segmentation using contour, surface, and depth cues." **IEEE International Conference on Image Processing**: 81-85.
- **[HVAA]** Lee, H. S. and Y. Hwan Kim (2018). Human visual attention analysis-based image segmentation using Color Histogram. **International SoC Design Conference (ISOCC)**: 76-77.
- **[FRFCM]** Lei, T., et al. (2018). "Significantly fast and robust fuzzy C-means clustering algorithm based on morphological reconstruction and membership filtering." **IEEE Transactions on Fuzzy Systems** 26(5): 3027-3041. [**[code]**](https://github.com/jiaxhsust/Significantly-Fast-and-Robust-FCM-Based-on-Morphological-Reconstruction-and-Membership-Filtering)
- **[H\_+R\_Better]** Li, K., et al. (2018). "Iterative image segmentation with feature driven heuristic four-color labeling." **Pattern Recognition** 76: 69-79.
- **[2DNLMeKGSA]** Mittal, H. and M. Saraswat (2018). "An optimum multi-level image thresholding segmentation using non-local means 2D histogram and exponential Kbest gravitational search algorithm." **Engineering Applications of Artificial Intelligence** 71: 226-235.
- **[AMR]** Lei, T., et al. (2019). "Adaptive morphological reconstruction for seeded image segmentation." **IEEE Transactions Image Processing** 28(11): 5510-5523. [**[code]**](https://github.com/jiaxhsust/Adaptive-Morphological-Reconstruction-for-Seeded-Image-Segmentation)
- **[SFFCM]** Lei, T., et al. (2019). "Superpixel-based fast fuzzy C-means clustering for color image segmentation." **IEEE Transactions on Fuzzy Systems** 27(9): 1753-1766. [**[code]**](https://github.com/jiaxhsust/Superpixel-based-Fast-Fuzzy-C-Means-Clustering-for-Color-Image-Segmentation)
- **[EA-GRAPH]** Sun, G., et al. (2019). "An enhanced affinity graph for image segmentation." **IEICE Transactions on Information and Systems** E102.D(5): 1073-1080.
- **[AASP-GRAPH]** Zhang, Y., et al. (2019).  "An adaptive affinity graph with subspace pursuit for natural image segmentation,"  **IEEE International Conference on Multimedia and Expo**: 802-807. [**[code]**](https://github.com/Yangzhangcst/AASP-Graph)
- **[MMGR-AFCF]** Lei, T., et al. (2020). "Automatic Fuzzy Clustering Framework for Image Segmentation." **IEEE Transactions on Fuzzy Systems**. [**[code]**](https://github.com/jiaxhsust/Automatic-Fuzzy-Clustering-Framework-for-Image-Segmentation)


##

## Citing
If you find this repository useful in your research, please consider citing:
```
@INPROCEEDINGS{AASP-Graph,  
  author={Y. {Zhang} and H. {Zhang} and Y. {Guo} and K. {Lin} and J. {He}},  
  booktitle={IEEE International Conference on Multimedia and Expo (ICME)},   
  title={An Adaptive Affinity Graph with Subspace Pursuit for Natural Image Segmentation},   
  year={2019}，  
  pages={802-807},}
```
```
@INPROCEEDINGS{AF-Graph,  
  author={Y. {Zhang} and M. {Liu} and J. {He} and F. {Pan} and Y. {Guo}},  
  booktitle={arXiv:2006.13542},   
  title={Affinity Fusion Graph-based Framework for Natural Image Segmentation},   
  year={2020}}
```

## Contact & Feedback

If you have any suggestions about this project, feel free to contact me.

- [e-mail: yzhangcst@smail.nju.edu.cn]
