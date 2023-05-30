# Measuring Stability of Online Process Outcome Prediction Frameworks
## Suhwan Lee <sup>1</sup>, Marco Comuzzi<sup>2</sup>, Xixi Lu<sup>1</sup>, Hajo A. Reijers<sup>1</sup>

<sup>1</sup> Utrecht University, Utrecht, The Netherlands

<sup>2</sup> Ulsan National Institute of Science and Technology, Ulsan, Republic of Korea

Process mining in online settings is becoming increasingly relevant. In the context of online process predictive monitoring, many approaches have been proposed to predict process outcomes. In contrast, very few have considered the issue of performance evaluation in-depth. In particular, the stability of an online prediction framework is important and influences the selection of the framework. 
Since online models can be updated as new labels become available, performance evaluation of online predictive models can be made continuously, which allows for defining more nuanced performance metrics than in the offline case. 
For instance, it can be interesting to evaluate the frequency at which the accuracy or any confusion matrix-based performance measure falls below a certain acceptable threshold or the rate at which a model can recover to an acceptable performance after a performance drop. 
This paper fills this gap by proposing an evaluation framework for measuring the performance of process outcome predictive models in online settings. We propose four performance meta-measures. Concrete performance measures can be derived by applying the meta-measures to the traditional performance measures commonly used in offline settings. 
The proposed framework is evaluated using artificial and real-world event logs. The evaluation shows how the proposed meta-measures can be used to select a classifier with the desired characteristics for a given predictive task in different contexts and also how to use the proposed metrics to extract more insights about the behavior recorded in an event log.  

## The four meta-measures

1. Frequency of significant performance drop

Given the sequence of performance values $\theta = \langle p_1, ..., p_n \rangle$ and the drops $\mathcal{D}(\theta) = \{D_1, ..., D_m\}$, the (normalized) frequency $\mathbb{F}$ of significant performance drops is defined as follows:


<img src=https://latex2png.com/pngs/267efd56023439c6aa5dded1628b17bc.png></img>

1. Stability of performance

Given the sequence of the standard deviations $\langle \varphi_1, ..., \varphi_n \rangle$, the average of the sequence of standard deviations $\mathbb{S}_{perf}$ is defined as follows: 

<img src=https://latex2png.com/pngs/6b7a2493257ece2b8c7cd164078ff7dc.png></img>

3. Magnitude of performance drop

The magnitude of performance drop is the difference between a drop point $p_{i}$ and the moving average $ma_i$, i.e., $\lvert p_i - ma_i \rvert$. 
We then define the maximum magnitude $\mathbb{M}_{max}$ and the average magnitude $\mathbb{M}_{avg}$ of performance drop as follows:

<img src=https://latex2png.com/pngs/5a68b7f18098af3b6762f8f81051e1ac.png></img>


<img src=https://latex2png.com/pngs/059edf0c13a65fd5369b4da093b8ec82.png></img>

4. Recovery rate

The recovery rate of a significant drop $D_{i}$ is calculated by counting the number of drop points in a drop, i.e., $\lvert D_{i} \rvert$. Having defined the recovery rate of a significant drop, the recovery ability of the predictive framework is measured by the average of the recovering rate of all drops, given the performance result $\theta$. It is calculated using the average of the collected recovery rate. 
% According to the definition of the significant drop, the size of the drop is dependent on the moving average window size $M$. 
% The normalized recovery rate is designed to diminish the influence of moving average window size. 
The average recovery rate ($\mathbb{R}_{avg}$) of the performance result $\theta$ is defined as follows:

<img src=https://latex2png.com/pngs/a65f835e5a380c61e305980581bdb6c1.png></img>

