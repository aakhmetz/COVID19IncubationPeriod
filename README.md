# Incubation period and other epidemiological characteristics of a novel coronavirus disease (COVID-19)

Supporting Materials for Natalie M. Linton, Tetsuro Kobayashi, Yichi Yang, Katsuma Hayashi, Andrei R. Akhmetzhanov, Sung-mok Jung, Baoyin Yuan, Ryo Kinoshita, Hiroshi Nishiura. Incubation Period and Other Epidemiological Characteristics of 2019 Novel Coronavirus Infections with Right Truncation: A Statistical Analysis of Publicly Available Case Data. J. Clin. Med. **2020**, 9, 538. ([doi:10.3390/jcm9020538](http://dx.doi.org/10.3390/jcm9020538))

[See medrxiv version on github](https://github.com/aakhmetz/WuhanIncubationPeriod2020/blob/master/manuscript/Linton%20Kobayashi%20et%20al%20Medrxiv%202020%20-%20version%202.pdf)

**Abstract**
The geographic spread of 2019 novel coronavirus (COVID-19) infections from the epicenter of Wuhan, China, has provided an opportunity to study the natural history of the recently emerged virus. Using publicly available event-date data from the ongoing epidemic, the present study investigated the incubation period and other time intervals that govern the epidemiological dynamics of COVID-19 infections. Our results show that the incubation period falls within the range of 2–14 days with 95% confidence and has a mean of around 5 days when approximated using the best-fit lognormal distribution. The mean time from illness onset to hospital admission (for treatment and/or isolation) was estimated at 3–4 days without truncation and at 5–9 days when right truncated. Based on the 95th percentile estimate of the incubation period, we recommend that the length of quarantine should be at least 14 days. The median time delay of 13 days from illness onset to death (17 days with right truncation) should be considered when estimating the COVID-19 case fatality risk.

There are three main notebooks in this repository:
1. To do statistical inference in Stan for non-truncated likelihood:</br>[A. MCMC simulations in Stan.ipynb](https://nbviewer.jupyter.org/github/aakhmetz/WuhanIncubationPeriod2020/blob/master/scripts/A.%20MCMC%20simulations%20in%20Stan.ipynb)
2. To do statistical inference in Stan for right truncated likelihood and accounting for exponential growth of the epidemic:</br>[B. MCMC simulations in Stan with right truncation.ipynb](https://nbviewer.jupyter.org/github/aakhmetz/WuhanIncubationPeriod2020/blob/master/scripts/B.%20MCMC%20simulations%20in%20Stan%20with%20right%20truncation.ipynb)
3. To get statistics of the posterior distribution, construct the traceplots, and generate two main figures for manuscript:</br>[C. Processing the traces.ipynb](https://nbviewer.jupyter.org/github/aakhmetz/WuhanIncubationPeriod2020/blob/master/scripts/C.%20Processing%20the%20traces.ipynb)

For statistical inference we used [cmdStan](https://mc-stan.org/users/interfaces/cmdstan) (version 2.22.1) and run our simulation on Ubuntu platform. The first two notebooks are written in R language with invoking bash commands. The last notebook is written in Python and utilizes [ArviZ](https://arviz-devs.github.io/arviz/index.html) package (version 0.6.1) for post-processing of the posteriors. 

Andrei R. Akhmetzhanov is thankful to [Ari Hartikainen](https://github.com/ahartikainen) and [Aki Vehtari](https://github.com/avehtari) for [helpful discussion](https://discourse.mc-stan.org/t/likelihood-for-calculating-waic-in-arviz-package/13013) on how to compute WAIC values in cmdStan/ArviZ.

---------
**Thank you for your interest to our work!** 

Few words of caution: We would like to note that our code is not supposed to work out of box, because the links used in the notebooks were user-specific, and our main intent was to show the relevance of the methods used in our paper.
