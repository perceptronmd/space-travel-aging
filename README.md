# space-travel-aging

## Abstract

Question: 
* how exactly does going to space age you? 
* Specifically, which proteins are most likely to be involved? 

Reason why we should do this:
1. telomere shortening during spaceflight and then subsequent lengthening after spaceflight (e.g., NASA Twins paper) is a good signal that going to space "ages" you. 
2. Currently, that's about the limit of our knowledge about how exactly space travel promotes the aging process but there does not appear to be a consensus on how certain organs age vs others. 
3. By assessing specific proteins/gene expression that are implicated in aging and then comparing this to how these organ-specific gene expressions change before/during/after space travel, then we would have a better idea about which specific tissues are more likely to age faster/worse. This can be translated into proactive care strategies before and after space missions.

Problem formulation:
1. amongst the proteins that are most implicated in biological aging, which of them increase/decrease as you go into space?
2. How does this look when you stratify across organs/tissues?

How we do the analysis:
1. Aging clock on UK biobank data proteomics dataset of 52K healthy individuals
2. Take the top 20 proteins contributory to biological aging (either positively or negatively) and see which ones overlap with differential gene expression in space travel in human (Inspiration, NASA Twins) and mouse studies

Conclusions: space travel is associated with differential expression of genes that are implicated in biological aging. There are putative signals for accelerated aging of adipose tissue as well as decelerated aging in liver tissues. 

## Figures

When assessing proteins contributing to younger age, there is strong evidence of underenrichment in adipose tissue (post-spaceflight) and overenrichment in liver tissue. ($score = (1-OR) / Pval$); vertical axis shows the score on log scale, $dir * log10((1-OR) / Pval)$, $dir=+1$ if OR>1, $dir=-1$ otherwise.

![image](https://github.com/perceptronmd/space-travel-aging/assets/72681336/d1222b7f-aac4-4ebf-abd9-9bc9c405f11f)


![image](https://github.com/perceptronmd/space-travel-aging/assets/72681336/1c245d7f-8158-48aa-aa26-1a76c486cce9)



These are the proteins involved, with contribution score computed from SHAP analysis of top 20 proteins used in the aging clock (deep neural network model).
Contributes to older age

| Contributes to Older Age | Contributes to Younger Age |
|---------------------------|----------------------------|
| LTBP2                     | PAEP                       |
| EDA2R                     | BCAN                       |
| SCARF2                    | ADAMTS15                   |
| NEFL                      | CDON                       |
| GFAP                      | FASLG                      |
| CCDC80                    | ROBO1                      |
| EFEMP1                    |                            |
| HAVCR1                    |                            |
| CXCL17                    |                            |
| CDHR2                     |                            |
| WNT9A                     |                            |
| CDCP1                     |                            |
| CRTAC1                    |                            |
| CCN5                      |                            |


![image](https://github.com/perceptronmd/space-travel-aging/assets/72681336/5cf872b0-b03e-4612-b4a5-9fe96cf41f83)


