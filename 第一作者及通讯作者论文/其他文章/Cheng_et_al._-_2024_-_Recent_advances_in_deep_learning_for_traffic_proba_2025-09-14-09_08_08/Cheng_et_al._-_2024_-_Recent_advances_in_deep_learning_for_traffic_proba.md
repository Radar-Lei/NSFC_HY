# Recent advances in deep learning for traffic probabilistic prediction

Long Cheng, Da Lei & Sui Tao

To cite this article: Long Cheng, Da Lei & Sui Tao (2024) Recent advances in deep learning for traffic probabilistic prediction, Transport Reviews, 44:6, 1129-1135, DOI: 10.1080/01441647.2024.2408840

To link to this article: https://doi.org/10.1080/01441647.2024.2408840

# Recent advances in deep learning for traffic probabilistic prediction

Long Cheng ${}^{a, b}$ , Da Lei ${}^{a, b}$ and Sui Tao ${}^{c}$

${}^{a}$ Jiangsu Key Laboratory of Urban ITS, School of Transportation, Southeast University, Nanjing, People’s Republic of China; ${}^{b}$ School of Transportation, Laboratory of Transport Industry of Comprehensive Transportation Theory (Nanjing Modern Multimodal Transportation Laboratory), Southeast University, Nanjing, People's Republic of China; 'Faculty of Geographical Science, Beijing Normal University, Beijing, People's Republic of China

## 1. Introduction

Traffic prediction is an essential task in today's transportation management schemes, allowing the identification and prediction of crucial information such as the volume of traffic, speed, travel demand, time-of-travel, and movement trajectories (Ermagun & Levinson, 2018; Huang et al., 2023). In fact, these forecasts are a vital component in traffic planning and control, and ensuring efficient, safe and convenient travelling (Liu et al., 2022; Steentoft et al., in press). As has been identified, traffic prediction is of great importance in view of effective resource allocation, better traffic control, and better planning of travel and freight logistics (Cui et al., 2023). That will reduce the duration of travel, fuel consumption and result in lower environmental impacts (Sun et al., 2021). Now, in the context of autonomous vehicles and smart cities, traffic prediction has been subjected to the routing of individual vehicles for city-wide traffic management strategies (Pang et al., 2021; Xu, Di, Yang, et al., 2023).

Deep learning (DL) has attracted attention in the field of traffic prediction over the past decade and has far surpassed traditional forecasting methods by successfully learning the complex spatial and temporal dependencies in traffic data. Despite these, most deep learning-based models in the current literature make deterministic predictions, providing only single-point estimates about future traffic states. This paradigm ignores the intrinsic variability and uncertainty of traffic systems that can lead to suboptimal decisions and unexpected outcomes (C. Li et al., 2024). Recognising the deficiencies of deterministic models has driven interest in the recent application of deep probabilistic modelling in traffic prediction. Probabilistic models differ from deterministic methods because, instead of forecasting a single future state, they evaluate the probability of a number of possible outcomes and quantify the uncertainties associated with the forecast of these outcomes, which could benefit decision-making under uncertainty and equip traffic managers and systems to better predict and mitigate potential adverse conditions (Murça, 2021; Yu et al., 2020). Compared to conventional probabilistic prediction methods such as Gaussian mixture models (GMM) and Monte Carlo (MC) sampling, deep learning models have demonstrated superior accuracy and generalisability in probabilistic traffic prediction (Murça, 2021).

---

CONTACT Da Lei & greatradar@gmail.com [C] School of Transportation, 2 Southeast University Road, Jiangning District, Nanjing, Jiangsu Province, 211189, P.R.China

© 2024 Informa UK Limited, trading as Taylor & Francis Group

---

This editorial provides a concise review focussing on the recent advancements in deep learning techniques for probabilistic traffic prediction. We will explore the methodologies used to quantify uncertainty, discuss their practical implications, and consider potential future directions in the field. By integrating probabilistic models, traffic management can progress towards more robust and resilient systems, adept at handling the dynamic and uncertain nature of real-world traffic environments (Fei et al., 2020; H. Li et al., 2023).

## 2. Deep learning methods in traffic probabilistic prediction

Probabilistic traffic prediction is a significant departure from previous deterministic prediction approaches in the sense that it provides a forecast with a range of possible traffic states and their corresponding probabilities. Probabilistic methods are crucial to mitigate the intrinsic uncertainties that exist in traffic systems, enhancing the dependability and precision of the results. Various techniques in this regard include Bayesian Deep Learning (BDL), Deep Gaussian Processes (DGPs), Quantile Regression (QR), and diffusion models. Bayesian deep learning views the model parameters as random variables instead of fixed elements; therefore, the model can express uncertainty regarding its predictions by giving probabilities for different traffic states (Liu et al., 2022; Pang et al., 2021; Sengupta et al., 2024). On the other hand, deep Gaussian processes represent a nonparametric approach that assumes the traffic flow follows a Gaussian distribution. This is particularly useful in approximating the expected traffic state and its associated uncertainties, especially when data is scarce (Steentoft et al., in press; Yang & Klabjan, 2021). In contrast, quantile regression predicts different percentiles of the traffic states, thus providing a range of possible solutions, rather than just an expected single mean value (H. Li et al., 2023). Furthermore, by noising the observed data in a specific way and training a neural network to denoise it, diffusion models are adept at generating plausible values for prediction targets, effectively estimating the probability distribution of potential outcomes rather than offering single-point estimates (Lei et al., 2024a).

The probabilistic approach can be further enriched by Ensemble Learning (EL) and Prediction Intervals (PIs) to integrate the predictions from various models for better prediction performance with uncertainty quantification (Mallick et al., 2024). In ensemble learning, several predictive models are combined to capture heterogeneous features of the data, providing more accurate forecasts using the mean or variance of the outputs from each predictive model (Noureldin et al., 2023; Olivier et al., 2023). PIs offer a range within which the true traffic condition is likely to fall, improving the prediction reliability (Y. Li et al., 2022, 2023). Additionally, Transformer models with attention mechanisms and Graph Convolutional Networks (GCNs) are often used in traffic probabilistic predictions to improve the model's focus and the learning of spatial dependency, respectively (Huang et al., 2023; Qian et al., 2024). Transformer-based models selectively focus on relevant data points, such as nearby road conditions or historical patterns, while GCNs represent road networks as graphs to learn traffic influence across connected road segments (Karim & Nower, 2024; Kong et al., 2023; Xu, Di, Yang, et al., 2023; Yu et al., 2020; Zhou et al., 2020).

Handling missing data and incorporating external factors are also critical in refining probabilistic traffic predictions. Models designed to impute missing values ensure reliability even with incomplete data sets (Xu, Di, Ding, et al., 2023). Moreover, incorporating inputs like weather conditions, events, and road closures allows models to adjust predictions based on external influences (Y. Li et al., 2022; Pang et al., 2021). The evaluation of these probabilistic models necessitates metrics that account for the predictive uncertainty, using tools such as the Prediction Interval Coverage Probability (PICP), Mean Interval Score (MIS), and Continuous Ranked Probability Score (CRPS) (Y. Li et al., 2022; Zhang et al., 2020). By integrating these diverse techniques, researchers and practitioners can develop comprehensive and dependable probabilistic traffic prediction models, which are crucial for informed decision-making in traffic planning, management and control. In Table 1, we present a selection of recent deep learning applications in traffic probabilistic prediction.

Table 1. A selection of recent deep learning applications in traffic probabilistic prediction.

<table><tr><td>Authors</td><td>Data</td><td>Method*</td><td>Target</td></tr><tr><td>Liu et al. (2022)</td><td>Freeway incident data, traffic sensor data</td><td>BDL</td><td>Incident detection</td></tr><tr><td>Steentoft et al. (in press)</td><td>Urban mobility flows, population data</td><td>DGPs</td><td>Mobility flow predictions</td></tr><tr><td>Pang et al. (2021)</td><td>Aircraft flight plans, weather data</td><td>BDL</td><td>Air traffic trajectory prediction</td></tr><tr><td>Xu, Di, Yang, et al. (2023)</td><td>Bike-sharing data</td><td>Transformer</td><td>Supply-demand prediction</td></tr><tr><td>Olivier et al. (2023)</td><td>Ambulance travel time data</td><td>BDL</td><td>Travel time prediction</td></tr><tr><td>G. Li et al. (2024)</td><td>Trajectory data</td><td>EL</td><td>Trajectory prediction</td></tr><tr><td>C. Li et al. (2024)</td><td>Ride-sourcing demand data</td><td>Transformer</td><td>Ride-sourcing demand prediction</td></tr><tr><td>Yu et al. (2020)</td><td>Road traffic speed data</td><td>GCNs</td><td>Traffic speed forecasting</td></tr><tr><td>Fei et al. (2020)</td><td>Vehicle trajectory data</td><td>EL</td><td>Vehicle trajectory prediction</td></tr><tr><td>H. Li et al. (2023)</td><td>Taxi GPS data</td><td>QR</td><td>Travel time prediction</td></tr><tr><td>S. Wang et al. (in press)</td><td>Vehicle trajectory data</td><td>EL</td><td>Trajectory prediction</td></tr><tr><td>Kong et al. (2023)</td><td>Traffic flow data</td><td>BDL</td><td>Traffic flow prediction</td></tr><tr><td>Qian et al. (2024)</td><td>Traffic speed data</td><td>GCNs</td><td>Traffic speed forecasting</td></tr><tr><td>Mallick et al. (2024)</td><td>Traffic flow data</td><td>DGPs</td><td>Traffic flow prediction</td></tr><tr><td>C. Li et al. (2020)</td><td>Public transit demand data</td><td>GCNs</td><td>Travel demand prediction</td></tr><tr><td>Y. Li et al. (2022)</td><td>Long-term traffic flow data</td><td>PIs</td><td>Traffic flow prediction</td></tr><tr><td>Y. Li et al. (2023)</td><td>Electric vehicle charging demand data</td><td>PIs</td><td>EV charging demand</td></tr><tr><td>Huang et al. (2023)</td><td>Electric vehicle charging data</td><td>Transformer</td><td>EV charging demand forecasting</td></tr><tr><td>Hu et al. (2022)</td><td>Traffic interaction data</td><td>GCNs</td><td>Traffic interactions prediction</td></tr><tr><td>Q. Wang et al. (2024)</td><td>Travel demand data</td><td>GCNs</td><td>Travel demand prediction</td></tr><tr><td>Tang et al. (2022)</td><td>Autonomous vehicle data</td><td>EL</td><td>Traffic flow prediction</td></tr><tr><td>Zhou et al. (2020)</td><td>Traffic speed data</td><td>GCNs</td><td>Traffic speed prediction</td></tr><tr><td>Sengupta et al. (2024)</td><td>Multi-source traffic data</td><td>BDL</td><td>Traffic flow prediction</td></tr><tr><td>Lei et al. (2024a)</td><td>Traffic flow with missing data</td><td>Diffusion model</td><td>Traffic flow prediction</td></tr><tr><td>de Nailly et al. (in press)</td><td>Pedestrian count data</td><td>PIs</td><td>Pedestrian count prediction</td></tr><tr><td>Zechin and Cybis (2023)</td><td>Traffic breakdown data</td><td>BDL</td><td>Traffic breakdown prediction</td></tr><tr><td>Karim and Nower (2024)</td><td>Traffic flow data</td><td>GCNs</td><td>Traffic flow prediction</td></tr><tr><td>Xu, Di, Ding, et al. (2023)</td><td>Traffic speed data</td><td>DGPs</td><td>Traffic speed prediction</td></tr><tr><td>Wu et al. (2021)</td><td>Spatiotemporal traffic data</td><td>BDL</td><td>Traffic flow prediction</td></tr><tr><td>Zhuang et al. (2022)</td><td>Sparse travel demand data</td><td>GCNs</td><td>Travel demand prediction</td></tr></table>

*BDL: Bayesian Deep Learning, DGPs: Deep Gaussian Processes, EL: Ensemble Learning, GCNs: Graph Convolutional Networks, QR: Quantile Regression, Pls: Prediction Intervals.

## 3. Practical implications and future directions

### 3.1. Practical implications

Probabilistic traffic prediction using deep learning models could bring significant practical value to real-world applications in multiple aspects of Intelligent Transportation Systems (ITS). Recognising the intrinsic uncertainty in traffic systems, the use of deep probabilistic models could provide a deeper understanding of traffic dynamics and guide better decision-making for transportation agencies (Fei et al., 2020). In particular, traffic management can use a probabilistic congestion forecast to take proactive control actions, such as dynamic speed limits, ramp metering, and re-routing, and therefore mitigate congestion before it actually happens (Chen et al., 2023). In public transport, the probabilistic prediction of the Estimated Time of Arrival (ETA) can be used to refine passenger information systems, allowing travellers to make better-informed decisions regarding departure times and route choices (Chen et al., 2023; Ricard et al., 2022). Moreover, the probabilistic predictions could facilitate improved risk assessment in safety-critical applications such as autonomous driving by providing probabilities for different traffic scenarios, allowing systems to anticipate and mitigate potential hazards more effectively (Liu et al., 2022; Tang et al., 2022). In addition, navigation applications can use probabilistic prediction outcomes to provide multiple routing solutions based on the computation of some confidence bounds so that the user can choose between shorter routes that might have delays and longer but more certain routes (Sun et al., 2021). Probabilistic traffic prediction could also help calibrate traffic simulation models to better represent the variability encountered in reality and test traffic management strategies under conditions of uncertainty (Olivier et al., 2023). Still, more widely, probabilistic models can be used to improve public transport planning by modelling the probability of delays; therefore, it helps transit agencies optimize schedules, allocate resources more effectively and give passengers estimates of arrival times that are more reliable (C. Li et al., 2020; Lyons & Marsden, 2021; Q. Wang et al., 2024).

### 3.2. Future directions

While significant advancements have been made in probabilistic traffic prediction using deep learning techniques, there remain several promising research directions that need further exploration. Efficient probabilistic deep models are expected to be developed while considering the interplay between various modes of transportation, including cars, public transportation, walking, and cycling, to facilitate intelligent multimodal transport systems (Lei et al., 2024b). The results of probabilistic prediction using deep learning should be extended toward long-term reliable predictions that could be used for effective strategic planning and infrastructure development. Furthermore, more scholarly focus is needed to improve the interpretability of deep probabilistic models, allowing a deeper understanding of the factors that influence predictions and the assessment of uncertainties (Noureldin et al., 2023). In addition, there is an emerging demand for deep probabilistic models capable of adapting in real time, with the ability to make updated predictions and reassess uncertainties based on newly obtained data - an essential feature for effective traffic management systems. Pang et al. (2021). Improving data efficiency with deep probabilistic models, despite having limited amounts of training data, is of great importance in some resource-limited environments. Integrating probabilistic traffic prediction using deep learning with other ITS applications, such as connected vehicles and autonomous driving systems, could also contribute to creating more efficient and safer transportation systems (Zechin & Cybis, 2023).

In addition, some deep Bayesian methods are quite computationally intensive under the large-scale datasets available now for uncertainty quantification in traffic predictions (G. Li et al., 2024). This creates an imperative need for developing more efficient and scalable deep Bayesian inference techniques for practical applications (Wu et al., 2021). Combining different sources of data such as loop detectors, GPS devices, cameras, and social media could also result in much more precise and reliable predictions in probabilistic traffic prediction using deep learning. Furthermore, it is essential to develop deep probabilistic modelling techniques that can capture the dynamics of traffic flow influenced by various factors, including weather conditions, accidents, special events, and driver behaviour (de Nailly et al., in press). Lastly, it is crucial to integrate uncertainty estimates into decision-making frameworks for traffic planning and management to ensure robust and optimal solutions (Hu et al., 2022). For example, real-time traffic management systems can leverage these uncertainty estimates to implement more resilient control strategies that proactively adapt to unforeseen events and minimize disruptions.

## Disclosure statement

No potential conflict of interest was reported by the author(s).

## Funding

This research is supported by the National Natural Science Foundation of China (No. 52372301), the Fundamental Research Funds for the Central Universities (No. RF1028623146 and 2242023R40027), and the Key Laboratory of Transport Industry of Comprehensive Transportation Theory (Nanjing Modern Multimodal Transportation Laboratory) (No. MTF2023006). References

Chen, X., Cheng, Z., Jin, J. G., Trépanier, M., & Sun, L. (2023). Probabilistic forecasting of bus travel time with a Bayesian Gaussian mixture model. Transportation Science, 57(6), 1516-1535.

Cui, H., Meng, Q., Teng, T. H., & Yang, X. (2023). Spatiotemporal correlation modelling for machine learning-based traffic state predictions: State-of-the-art and beyond. Transport Reviews, 43(4), 780-804. https://doi.org/10.1080/01441647.2023.2171151

de Nailly, P., Côme, E., Oukhellou, L., Samé, A., Ferrière, J., & Merad-Boudia, Y. (In Press). Deep probabilistic forecasting of multivariate count data with sums and shares distributions: A case study on pedestrian counts in a multimodal transport hub. IEEE Transactions on Intelligent Transportation Systems.

Ermagun, A., & Levinson, D. (2018). Spatiotemporal traffic forecasting: Review and proposed directions. Transport Reviews, 38(6), 786-814. https://doi.org/10.1080/01441647.2018.1442887

Fei, C., He, X., & Ji, X. (2020). Multi-modal vehicle trajectory prediction based on mutual information. IET Intelligent Transport Systems, 14(3), 148-153. https://doi.org/10.1049/itr2.v14.3

Hu, Y., Zhan, W., & Tomizuka, M. (2022). Scenario-transferable semantic graph reasoning for interaction-aware probabilistic prediction. IEEE Transactions on Intelligent Transportation Systems, 23 (12), 23212-23230. https://doi.org/10.1109/TITS.2022.3206233

Huang, X., Wu, D., & Boulet, B. (2023). Metaprobformer for charging load probabilistic forecasting of electric vehicle charging stations. IEEE Transactions on Intelligent Transportation Systems, 24(10), 10445-10455. https://doi.org/10.1109/TITS.2023.3276947

Karim, A. A., & Nower, N. (2024). Probabilistic spatio-temporal graph convolutional network for traffic forecasting. Applied Intelligence, 54, 7070-7085.

Kong, J., Fan, X., Jin, X., Lin, S., & Zuo, M. (2023). A variational Bayesian inference-based en-decoder framework for traffic flow prediction. IEEE Transactions on Intelligent Transportation Systems, 25(3), 2966-2975. https://doi.org/10.1109/TITS.2023.3276216

Lei, D., Xu, M., & Wang, S. (2024a). A conditional diffusion model for probabilistic estimation of traffic states at sensor-free locations. Transportation Research Part C: Emerging Technologies, 166, Article 104798. https://doi.org/10.1016/j.trc.2024.104798

Lei, D., Xu, M., & Wang, S. (2024b). A deep multimodal network for multi-task trajectory prediction. Information Fusion, 113, Article 102597.

Li, C., Bai, L., Liu, W., Yao, L., & Waller, S. T. (2020). Graph neural network for robust public transit demand prediction. IEEE Transactions on Intelligent Transportation Systems, 23(5), 4086-4098. https://doi.org/10.1109/TITS.2020.3041234

Li, Y., Chai, S., Wang, G., Zhang, X., & Qiu, J. (2022). Quantifying the uncertainty in long-term traffic prediction based on PI-ConvLSTM network. IEEE Transactions on Intelligent Transportation Systems, 23(11), 20429-20441. https://doi.org/10.1109/TITS.2022.3193184

Li, Y., Chai, S., Zhang, X., Wang, G., Zhu, R., & Chung, E. (2023). STPNet: Quantifying the uncertainty of electric vehicle charging demand via long-term spatiotemporal traffic flow prediction intervals. IEEE Transactions on Intelligent Transportation Systems, 24(12), 15018-15034.

Li, C., Geng, M., Chen, Y., Cai, Z., Zhu, Z., & Chen, X. M. (2024). Demand forecasting and predictability identification of ride-sourcing via bidirectional spatial-temporal transformer neural processes. Transportation Research Part C: Emerging Technologies, 158, Article 104427.

Li, G., Li, Z., Knoop, V. L., & van Lint, H. (2024). Unravelling uncertainty in trajectory prediction using a non-parametric approach. Transportation Research Part C: Emerging Technologies, 163, Article 104659.

Li, H., Wang, Z., Li, X., Wang, H., Man, Y., & Shi, J. (2023). Travel time probability prediction based on constrained LSTM quantile regression. Journal of Advanced Transportation, 2023(1), Article 9910142.

Liu, G., Jin, H., Li, J., Hu, X., & Li, J. (2022). A Bayesian deep learning method for freeway incident detection with uncertainty quantification. Accident Analysis & Prevention, 176, Article 106796. https://doi.org/10.1016/j.aap.2022.106796

Lyons, G., & Marsden, G. (2021). Opening out and closing down: The treatment of uncertainty in transport planning's forecasting paradigm. Transportation, 48(2), 595-616. https://doi.org/10.1007/s11116-019-10067-x

Mallick, T., Macfarlane, J., & Balaprakash, P. (2024). Uncertainty quantification for traffic forecasting using deep-ensemble-based spatiotemporal graph neural networks. IEEE Transactions on Intelligent Transportation Systems, 25(8), 9141-9152.

Murça, M. C. R. (2021). Identification and prediction of urban airspace availability for emerging air mobility operations. Transportation Research Part C: Emerging Technologies, 131, Article 103274.

Noureldin, M., Abuhmed, T., Saygi, M., & Kim, J. (2023). Explainable probabilistic deep learning framework for seismic assessment of structures using distribution-free prediction intervals. Computer-Aided Civil and Infrastructure Engineering, 38(12), 1677-1698. https://doi.org/10.1111/ mice.v38.12

Olivier, A., Mohammadi, S., Smyth, A. W., & Adams, M. (2023). Bayesian neural networks with physics-aware regularization for probabilistic travel time modeling. Computer-Aided Civil and Infrastructure Engineering, 38(18), 2614-2631. https://doi.org/10.1111/mice.v38.18

Pang, Y., Zhao, X., Yan, H., & Liu, Y. (2021). Data-driven trajectory prediction with weather uncertainties: A Bayesian deep learning approach. Transportation Research Part C: Emerging Technologies, 130, Article 103326. https://doi.org/10.1016/j.trc.2021.103326

Qian, W., Nielsen, T. D., Zhao, Y., Larsen, K. G., & Yu, J. J. (2024). Uncertainty-aware temporal graph convolutional network for traffic speed forecasting. IEEE Transactions on Intelligent Transportation Systems, 25(8), 8578-8590.

Ricard, L., Desaulniers, G., Lodi, A., & Rousseau, L. M. (2022). Predicting the probability distribution of bus travel time to measure the reliability of public transport services. Transportation Research Part C: Emerging Technologies, 138, Article 103619. https://doi.org/10.1016/j.trc.2022.103619

Sengupta, A., Mondal, S., Das, A., & Guler, S. I. (2024). A Bayesian approach to quantifying uncertainties and improving generalizability in traffic prediction models. Transportation Research Part C: Emerging Technologies, 162, Article 104585. https://doi.org/10.1016/j.trc.2024.104585

Steentoft, A., Lee, B. S., & Schläpfer, M. (In Press). Quantifying the uncertainty of mobility flow predictions using Gaussian processes. Transportation.

Sun, W., Schmöcker, J. D., & Nakamura, T. (2021). On the tradeoff between sensitivity and specificity in bus bunching prediction. Journal of Intelligent Transportation Systems, 25(4), 384-400. https:// doi.org/10.1080/15472450.2020.1725887

Tang, X., Yang, K., Wang, H., Wu, J., Qin, Y., Yu, W., & Cao, D. (2022). Prediction-uncertainty-aware decision-making for autonomous vehicles. IEEE Transactions on Intelligent Vehicles, 7(4), 849- 862. https://doi.org/10.1109/TIV.2022.3188662

Wang, S., Gao, K., Zhang, L., Liu, Y., & Chen, L. (In Press). Probabilistic prediction of longitudinal trajectory considering driving heterogeneity with interpretability. IEEE Intelligent Transportation Systems Magazine.

Wang, Q., Wang, S., Zhuang, D., Koutsopoulos, H., & Zhao, J. (2024). Uncertainty quantification of spatiotemporal travel demand with probabilistic graph neural networks. IEEE Transactions on Intelligent Transportation Systems, 25(8), 8770-8781.

Wu, D., Gao, L., Chinazzi, M., Xiong, X., Vespignani, A., Ma, Y. A., ... Yu, R. (2021). Quantifying uncertainty in deep spatiotemporal forecasting. In Proceedings of the 27th ACM Sigkdd Conference on Knowledge Discovery & Data Mining (pp. 1841-1851). Association for Computing Machinery

Xu, M., Di, Y., Ding, H., Zhu, Z., Chen, X., & Yang, H. (2023). GNP: Network-wide short-term probabilistic traffic speed prediction and imputation. Communications in Transportation Research, 3, Article 100099. https://doi.org/10.1016/j.commtr.2023.100099

Xu, M., Di, Y., Yang, H., Chen, X., & Zhu, Z. (2023). Multi-task supply-demand prediction and reliability analysis for docked bike-sharing systems via transformer-encoder-based neural processes. Transportation Research Part C: Emerging Technologies, 147, Article 104015. https://doi.org/10.1016/j.trc.2023.104015

Yang, J., & Klabjan, D. (2021). Bayesian active learning for choice models with deep Gaussian processes. IEEE Transactions on Intelligent Transportation Systems, 22(2), 1080-1092. https://doi.org/10.1109/TITS.2019.2962535

Yu, B., Lee, Y., & Sohn, K. (2020). Forecasting road traffic speeds by considering area-wide spatiotemporal dependencies based on a graph convolutional neural network (GCN). Transportation Research Part C: Emerging Technologies, 114, 189-204. https://doi.org/10.1016/j.trc.2020.02.013

Zechin, D., & Cybis, H. B. B. (2023). Probabilistic traffic breakdown forecasting through Bayesian approximation using variational LSTMs. Transportmetrica B: Transport Dynamics, 11(1), 1026- 1044.

Zhang, X., Chan, K. W., Li, H., Wang, H., Qiu, J., & Wang, G. (2020). Deep-learning-based probabilistic forecasting of electric vehicle charging load with a novel queuing model. IEEE Transactions on Cybernetics, 51(6), 3157-3170. https://doi.org/10.1109/TCYB.2020.2975134

Zhou, F., Yang, Q., Zhong, T., Chen, D., & Zhang, N. (2020). Variational graph neural networks for road traffic prediction in intelligent transportation systems. IEEE Transactions on Industrial Informatics, 17(4), 2802-2812. https://doi.org/10.1109/TII.9424

Zhuang, D., Wang, S., Koutsopoulos, H., & Zhao, J. (2022). Uncertainty quantification of sparse travel demand prediction with spatial-temporal graph neural networks. In Proceedings of the 28th ACM Sigkdd Conference on Knowledge Discovery and Data Mining (pp. 4639-4647). Association for Computing Machinery.