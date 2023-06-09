# An unbiased ratio estimator

[Zeyang Sun](http://astro.sjtu.edu.cn/zh/staff/students/40-),
[Pengjie Zhang](http://astro.sjtu.edu.cn/zh/staff/people/13-),
[Fuyu Dong](https://orcid.org/0000-0003-0296-0841),
[Ji Yao](http://astro.sjtu.edu.cn/zh/staff/postdoctoral-researchers/26-),
[Huanyuan Shan](http://www.shao.cas.cn/2020Ver/yjdw/zgj/index_81441.html?json=http://sourcedb.shao.cas.cn/zw/zjrck/201905/t20190507_5289672.json),
[Eric Jullo](https://www.researchgate.net/profile/Eric-Jullo),
[Jean-Paul Kneib](https://people.epfl.ch/jean-paul.kneib),
[Boyan Yin](https://www.phys.virginia.edu/People/personal.asp?UID=by3fn)

In certain cases of astronomical data analysis, the meaningful physical quantity to extract is the ratio $R$ between two data sets. Examples include the lensing ratio, the interloper rate in spectroscopic redshift samples, the decay rate of gravitational potential and $E_G$ to test gravity. However, simply taking the ratio of the two data sets is biased, since it renders (even statistical) errors in the denominator into systematic errors in $R$. Furthermore, it is not optimal in minimizing statistical errors of $R$. 

Based on the Bayesian analysis and the usual assumption of Gaussian error in the data, we derive an analytical expression of the posterior PDF $P(R)$. This result enables fast and unbiased $R$ measurement, with minimal statistical errors. Furthermore, it relies on no underlying model other than the proportionality relation between the two data sets. Even more generally, it applies to the cases where the proportionality relation holds for the underlying physics/statistics instead of the two data sets directly. It also applies to the case of multiple ratios ($R$ $\rightarrow$ $\mathbf R $=($R_1,R_2,...$)).

The main result of this work is the analytical expression of the PDF $P(R)$ (Eq.8 in paper).

## Resources

Code:
- [Unbiased ratio estimator](codes/Unbiased_ratio_estimator.py): original repository

Paper:
- An unbiased method of measuring the ratio of two data sets, 2022. [[paper](https://arxiv.org/abs/2210.13717), [slides](slides/lensing_ratio_SunZeyang_20230603.pdf)]

## Notebooks

The below notebooks contain examples to play with the unbiased ratio estimator. Look at the first one if you want to use the method with your own data.

1. [The simplest case of the ratio estimator](notebook/The_simplest_case.ipynb). The easiest example to run if the physically meaningful $R$ is directly the ratio of two data sets, but not there underlying model. Meanwhile, the measurement errors in ${\bf d}_1, {\bf d}_2$ are uncorrelated. That is to say, the mapping matrix ${\bf A}_1 = {\bf I}, {\bf A}_2 = R{\bf I}$.

2. [The case when the two data sets are correlated](notebook/Correlated_data_sets.ipynb). The difference with the first notebook is, the measurement errors in ${\mathbf d}_1, {\mathbf d}_2$ are correlated.

## Reproducing the results of the paper

See the [codes](notebook/Lensing_ratio_example.ipynb).

Follow the below steps to reproduce the paper's results. While the instructions are simple, your data sets should prepare in advance.

1. **Get the main data sets ${\bf d}_1, {\bf d}_2$**.

2. **Data pre-precessing $w^{g\gamma_t}$, $w^{g\kappa_{\rm CMB}}$, $w_{tem}^{g\gamma_t}$, $w^{g\kappa_{\rm CMB}}_{tem}$**.

3. **Run the code** `unbiased_R_estimator`.

## Citation

Please consider citing our paper if you find it useful.

```
@ARTICLE{2022arXiv221013717S,
       author = {{Sun}, Zeyang and {Zhang}, Pengjie and {Yao}, Ji and {Dong}, Fuyu and {Shan}, Huanyuan and {Jullo}, Eric and {Kneib}, Jean-Paul and {Yin}, Boyan},
        title = "{An unbiased method of measuring the ratio of two data sets}",
      journal = {arXiv e-prints},
     keywords = {Astrophysics - Cosmology and Nongalactic Astrophysics},
         year = 2022,
        month = oct,
          eid = {arXiv:2210.13717},
        pages = {arXiv:2210.13717},
archivePrefix = {arXiv},
       eprint = {2210.13717},
 primaryClass = {astro-ph.CO},
       adsurl = {https://ui.adsabs.harvard.edu/abs/2022arXiv221013717S},
      adsnote = {Provided by the SAO/NASA Astrophysics Data System}
}
```

