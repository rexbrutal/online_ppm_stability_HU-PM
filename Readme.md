# Measuring Stability of Online Process Outcome Prediction Frameworks
## Suhwan Lee <sup>1</sup>, Marco Comuzzi<sup>2</sup>, Xixi Lu<sup>1</sup>, Hajo A. Reijers<sup>1</sup>

<sup>1</sup> Utrecht University, Utrecht, The Netherlands

<sup>2</sup> Ulsan National Institute of Science and Technology, Ulsan, Republic of Korea

## Motivation
To highlight the need for more nuanced performance metrics in outcome-based predictive process monitoring, we introduce a classification of business scenarios along two dimensions: the _frequency_ of and the _risk_ associated with the decisions taken using a predictive monitoring model.

<p align="center">
    <img src='./img/matrix.png'></img>
</p>

## The four meta-measures

1. Frequency of significant performance drop

Given the sequence of performance values $\theta = \langle p_1, ..., p_n \rangle$ and the drops $\mathcal{D}(\theta) = \{D_1, ..., D_m\}$, the (normalized) frequency $\mathbb{F}$ of significant performance drops is defined as follows:

<p align="center">
<img src=https://latex2png.com/pngs/267efd56023439c6aa5dded1628b17bc.png></img>
</p>

1. Stability of performance

Given the sequence of the standard deviations $\langle \varphi_1, ..., \varphi_n \rangle$, the average of the sequence of standard deviations $\mathbb{S}_{perf}$ is defined as follows: 
<p align="center">
<img src=https://latex2png.com/pngs/6b7a2493257ece2b8c7cd164078ff7dc.png></img>
</p>

3. Magnitude of performance drop

The magnitude of performance drop is the difference between a drop point $p_{i}$ and the moving average $ma_i$, i.e., $\lvert p_i - ma_i \rvert$. 
We then define the maximum magnitude $\mathbb{M}\_{max}$ and the average magnitude $\mathbb{M}\_{avg}$ of performance drop as follows:
<p align="center">
<img src=https://latex2png.com/pngs/5a68b7f18098af3b6762f8f81051e1ac.png></img>

<img src=https://latex2png.com/pngs/059edf0c13a65fd5369b4da093b8ec82.png></img>
</p>

4. Recovery rate

The recovery rate of a significant drop $D_{i}$ is calculated by counting the number of drop points in a drop, i.e., $\lvert D\_{i} \rvert$. Having defined the recovery rate of a significant drop, the recovery ability of the predictive framework is measured by the average of the recovering rate of all drops, given the performance result $\theta$. It is calculated using the average of the collected recovery rate. 

The average recovery rate ($\mathbb{R}_{avg}$) of the performance result $\theta$ is defined as follows:
<p align="center">
<img src=https://latex2png.com/pngs/a65f835e5a380c61e305980581bdb6c1.png></img>
</p>

<h1>
<a href="https://github.com/ghksdl6025/online_ppm_stability/blob/master/Experiment_results.md">Empirical result</a>
</h1>