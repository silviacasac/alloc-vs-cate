# Good Allocations from Bad Estimates

This repository contains the empirical evaluation code for the low-accuracy allocation algorithm presented in the paper "Good Allocations from Bad Estimates" by Sílvia Casacuberta and Moritz Hardt.

## Abstract
Conditional average treatment effect (CATE) estimation is the de facto gold standard for targeting a treatment to a heterogeneous population. The method estimates treatment effects up to an error $\epsilon > 0$ in each of $M$ different strata of the population, targeting individuals in decreasing order of estimated treatment effect until the budget runs out. In general, this method requires $O(M/\epsilon^2)$ samples. This is best possible if the goal is to estimate all treatment effects up to an $\epsilon$ error. 
In this work, we show how to achieve the same total treatment effect as CATE with only $O(M/\epsilon)$ samples for natural distributions of treatment effects. The key insight is that coarse estimates suffice for near-optimal treatment allocations. In addition, we show that budget flexibility can further reduce the sample complexity of allocation.
Finally, we evaluate our algorithm on various real-world RCT datasets. In all cases, it finds nearly optimal treatment allocations with surprisingly few samples. Our work highlights the fundamental distinction between treatment effect estimation and treatment allocation: the latter requires far fewer samples.

## Datasets
We test our allocation algorithm on the following five real-world RCTs:
1. Tennessee’s Student Teacher Achievement Ratio (STAR) project dataset (Pate-Bain et al. 1997).
2. Targeting the Ultra Poor (TUP) in India dataset (Banerjee et al. 2021).
3. National Supported Work (NSW) demonstration dataset (LaLonde 1986).
4. Acupuncture dataset (Vickers et al. 2024).
5. Postoperative Pain dataset (McHardy et al. 1999).

## Notebooks
Each of the five datasets is analyzed using two notebooks:
- `*_1.ipynb`:  
  Sample-size analysis. Evaluates how the allocation value varies as a function of the number
  of samples drawn from the RCT.

- `*_2.ipynb`:  
  Budget analysis. Evaluates the allocation performance across different budget levels
  (fraction of units selected).

## Citation
