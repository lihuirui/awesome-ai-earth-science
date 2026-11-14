# Awesome AI Earth Science（AI 地球科学）

> 精选 **AI for Earth Science / AI Weather & Climate** 论文、代码、数据集与工具库。仅收录可核验的 arXiv / 官方仓库链接；严禁编造标题、作者、年份或 URL。

**仓库：** [lihuirui/awesome-ai-earth-science](https://github.com/lihuirui/awesome-ai-earth-science) · **最近更新：** 2026-11-14（Asia/Shanghai）

**收录原则：** 优先开源与可复现；条目格式对齐 [awesome-time-series-foundation-models](https://github.com/lihuirui/awesome-time-series-foundation-models)。

## Table of Contents

- [Surveys / 综述](#surveys--综述)
- [Reanalysis / Simulation — Deterministic](#reanalysis--simulation--deterministic)
  - [GNN](#gnn)
  - [CNN](#cnn)
  - [Neural Operator](#neural-operator)
  - [Transformer](#transformer)
  - [Other DNN](#other-dnn)
- [Probabilistic / Generative](#probabilistic--generative)
- [Radar Nowcasting / 雷达临近](#radar-nowcasting--雷达临近)
- [Satellite / 卫星](#satellite--卫星)
- [Station / 站点](#station--站点)
- [Multi-source / 多源与同化](#multi-source--多源与同化)
- [Earth Observation Foundation Models / 地球观测基础模型](#earth-observation-foundation-models--地球观测基础模型)
- [Datasets & Benchmarks / 数据集与基准](#datasets--benchmarks--数据集与基准)
- [Toolkits & Platforms / 工具与平台](#toolkits--platforms--工具与平台)
- [Related Awesome Lists / 相关列表](#related-awesome-lists--相关列表)
- [Maintenance](#maintenance)

---

## Surveys / 综述

- **Foundation Models for Weather and Climate** — 参见各模型论文引言与 [WeatherBench 2](https://github.com/google-research/weatherbench2) 相关综述章节（持续补充独立 survey 条目）。
- **Large Models for Time Series and Spatio-Temporal Data: A Survey and Outlook** — Jin et al. (2023) [[Paper](https://arxiv.org/abs/2310.10196)]

---

## Reanalysis / Simulation — Deterministic

再分析 / 数值模拟驱动的确定性预报与气候仿真器。

### GNN

- **Keisler 2022** (2022) [[Paper](https://arxiv.org/abs/2202.07575)] — _Forecasting Global Weather with Graph Neural Networks_
- **GraphCast** (2022) [[Paper](https://arxiv.org/abs/2212.12794)] [[Code](https://github.com/google-deepmind/weathernext)] — _GraphCast: Learning skillful medium-range global weather forecasting_
- **SeaCast** (2024) [[Paper](https://arxiv.org/abs/2410.11807)] — _Regional Ocean Forecasting with Hierarchical Graph Neural Networks_
- **GraphRiverCast** (2026) [[Paper](https://arxiv.org/abs/2602.22293)] — _Learning global river system hydrodynamics with a topology-informed foundation model_

### CNN

- **GAN-UNet**
- **ARCNNv1**
- **DLESyM** (2024) [[Paper](https://arxiv.org/abs/2409.16247)] — _A Deep Learning Earth System Model for Efficient Simulation of the Observed Climate_

### Neural Operator

- **FourCastNet** (2022) [[Paper](https://arxiv.org/abs/2202.11214)] [[Code](https://github.com/NVlabs/FourCastNet)] — _FourCastNet: A Global Data-driven High-resolution Weather Model using Adaptive Fourier Neural Operators_
- **ACE** (2023) [[Paper](https://arxiv.org/abs/2310.02074)] [[Code](https://github.com/ai2cm/ace)] — _ACE: A fast, skillful learned global atmospheric model for climate prediction_
- **NeuralGCM** (2023) [[Paper](https://arxiv.org/abs/2311.07222)] [[Code](https://github.com/neuralgcm/neuralgcm)] — _Neural General Circulation Models for Weather and Climate_
- **ACE2** (2024) [[Paper](https://arxiv.org/abs/2411.11268)] [[Code](https://github.com/ai2cm/ace)] — _ACE2: Accurately learning subseasonal to decadal atmospheric variability and forced responses_
- **LUCIE-3D** (2025) [[Paper](https://arxiv.org/abs/2509.02061)] — _LUCIE-3D: A three-dimensional climate emulator for forced responses_
- **ACE2-SOM** (2024) [[Paper](https://arxiv.org/abs/2412.04418)] [[Code](https://github.com/ai2cm/ace)] — _ACE2-SOM: Coupling an ML atmospheric emulator to a slab ocean and learning the sensitivity of climate to changed CO$_2$_
- **LCG-SFNO** (2026) [[Paper](https://arxiv.org/abs/2611.03411)] — _Low-Rank Clebsch--Gordan Coupling for Equivariant Spherical Forecasting_

### Transformer

- **Pangu-Weather** (2022) [[Paper](https://arxiv.org/abs/2211.02556)] [[Code](https://github.com/198808xc/Pangu-Weather)] — _Pangu-Weather: A 3D High-Resolution Model for Fast and Accurate Global Weather Forecast_
- **FengWu** (2023) [[Paper](https://arxiv.org/abs/2304.02948)] [[Code](https://github.com/OpenEarthLab/FengWu)] — _FengWu: Pushing the Skillful Global Medium-range Weather Forecast beyond 10 Days Lead_
- **FuXi** (2023) [[Paper](https://arxiv.org/abs/2306.12873)] [[Code](https://github.com/tpys/fuxi-weather)] — _FuXi: A cascade machine learning forecasting system for 15-day global weather forecast_
- **ClimaX** (2023) [[Paper](https://arxiv.org/abs/2301.10343)] [[Code](https://github.com/microsoft/ClimaX)] — _ClimaX: A foundation model for weather and climate_
- **Aurora** (2024) [[Paper](https://arxiv.org/abs/2405.13063)] [[Code](https://github.com/microsoft/aurora)] — _A Foundation Model for the Earth System_
- **AIFS** (2024) [[Paper](https://arxiv.org/abs/2406.01465)] — _AIFS -- ECMWF&#39;s data-driven forecasting system_
- **3D-Geoformer**
- **Prithvi-WxC** (2024) [[Paper](https://arxiv.org/abs/2409.13598)] [[Code](https://github.com/NASA-IMPACT/Prithvi-WxC)] — _Prithvi WxC: Foundation Model for Weather and Climate_
- **FengWu-W2S** (2024) [[Paper](https://arxiv.org/abs/2411.10191)] [[Code](https://github.com/OpenEarthLab/FengWu)] — _FengWu-W2S: A deep learning model for seamless weather-to-subseasonal forecast of global atmosphere_
- **WeatherGFT / FGT** (2024) [[Paper](https://arxiv.org/abs/2405.13796)] — _Generalizing Weather Forecast to Fine-grained Temporal Scales via Physics-AI Hybrid Modeling_
- **HighFM** (2026) [[Paper](https://arxiv.org/abs/2604.04306)] — _HighFM: Towards a Foundation Model for Learning Representations from High-Frequency Earth Observation Data_
- **STRATA** (2026) [[Paper](https://arxiv.org/abs/2606.31248)] [[Code](https://github.com/NVlabs/STRATA)] — _Scaling Storm-Resolving Atmospheric AI Simulation to the Entire Planet_

### Other DNN

- **Samudra / Samudra2** (2024) [[Paper](https://arxiv.org/abs/2412.03795)] [[Code](https://github.com/m2lines/Samudra)] — _Samudra: An AI Global Ocean Emulator for Climate_
- **CliMA**
- **WenHai**
- **XiHe** (2024) [[Paper](https://arxiv.org/abs/2402.02995)] — _XiHe: A Data-Driven Model for Global Ocean Eddy-Resolving Forecasting_
- **ResoNet** (2023) [[Paper](https://arxiv.org/abs/2312.10429)] — _ResoNet: Robust and Explainable ENSO Forecasts with Hybrid Convolution and Transformer Networks_
- **AIFL** (2026) [[Paper](https://arxiv.org/abs/2602.16579)] — _AIFL: A Global Daily Streamflow Forecasting Model Using a Deterministic LSTM Pre-trained on ERA5-Land and Fine-tuned on IFS_
- **SamudrACE** (2025) [[Paper](https://arxiv.org/abs/2509.12490)] [[Code](https://github.com/ai2cm/ace)] — _SamudrACE: Fast and Accurate Coupled Climate Modeling with 3D Ocean and Atmosphere Emulators_
- **CTEFNet** (2025) [[Paper](https://arxiv.org/abs/2503.19502)] — _Towards Long-Range ENSO Prediction with an Explainable Deep Learning Model_
- **DualST**
- **FengWu-GHR** (2024) [[Paper](https://arxiv.org/abs/2402.00059)] [[Code](https://github.com/OpenEarthLab/FengWu)] — _FengWu-GHR: Learning the Kilometer-scale Medium-range Global Weather Forecasting_
- **AI-TRANS**
- **NeuralPOM** (2026) [[Paper](https://arxiv.org/abs/2611.02460)] [[Code](https://github.com/ChiyodaMomo01/NeuralPOM)] — _New Wine in an Old Bottle -- NeuralPOM: A Hybrid Ocean Forecast Model with Differentiable Dynamics and Staged Learning_
- **One2N** (2026) [[Paper](https://arxiv.org/abs/2611.12249)] — _One2N: Recursive refinement breaks the resolution barrier for Earth-system AI_
- **Rescene-ESM** (2026) [[Paper](https://arxiv.org/abs/2611.11066)] — _Rescene-ESM: an Earth system model built around a frozen AI weather model_
- **PROLA** (2026) [[Paper](https://arxiv.org/abs/2611.11318)] — _PROLA: Principal-Orthogonal Low-rank Adaptation for Predictive Spatiotemporal Weather Downscaling_

---

## Probabilistic / Generative

集合 / VAE / 扩散等概率与生成式方法。

- **GenCast** (2023) [[Paper](https://arxiv.org/abs/2312.15796)] [[Code](https://github.com/google-deepmind/weathernext)] — _GenCast: Diffusion-based ensemble forecasting for medium-range weather_
- **CorrDiff** (2023) [[Paper](https://arxiv.org/abs/2309.15214)] — _Residual Corrective Diffusion Modeling for Km-scale Atmospheric Downscaling_
- **FuXi-ENS** (2024) [[Paper](https://arxiv.org/abs/2405.05925)] [[Code](https://github.com/tpys/fuxi-weather)] — _FuXi-ENS: A machine learning model for medium-range ensemble weather forecasting_
- **FuXi-S2S** (2023) [[Paper](https://arxiv.org/abs/2312.09926)] [[Code](https://github.com/tpys/fuxi-weather)] — _FuXi-S2S: A machine learning model that outperforms conventional global subseasonal forecast models_
- **FuXi-Extreme** (2023) [[Paper](https://arxiv.org/abs/2310.19822)] [[Code](https://github.com/tpys/fuxi-weather)] — _FuXi-Extreme: Improving extreme rainfall and wind forecasts with diffusion model_
- **OmniCast** (2025) [[Paper](https://arxiv.org/abs/2510.18707)] — _OmniCast: A Masked Latent Diffusion Model for Weather Forecasting Across Time Scales_
- **LaDCast** (2025) [[Paper](https://arxiv.org/abs/2506.09193)] — _LaDCast: A Latent Diffusion Model for Medium-Range Ensemble Weather Forecasting_
- **cBottle** (2025) [[Paper](https://arxiv.org/abs/2505.06474)] [[Code](https://github.com/NVlabs/cBottle)] — _Climate in a Bottle: Towards a Generative Foundation Model for the Kilometer-Scale Global Atmosphere_
- **Marchuk** (2026) [[Paper](https://arxiv.org/abs/2603.24428)] — _Marchuk: Efficient Global Weather Forecasting from Mid-Range to Sub-Seasonal Scales via Flow Matching_
- **AIFS-TC / AIFS ENS** (2026) [[Paper](https://arxiv.org/abs/2608.09959)] — _AIFS-TC: A simple correction competitive with the operational frontier for tropical cyclone intensity forecasting_
- **Feng-Shun / 风顺**
- **WeatherNext 2 / FGN** (2025) [[Paper](https://arxiv.org/abs/2506.10772)] [[Code](https://github.com/google-deepmind/weathernext)] — _Skillful joint probabilistic weather forecasting from marginals_
- **FengWu-Ensemble** [[Code](https://github.com/OpenEarthLab/FengWu)]
- **FourCastNet-3 / FCN3** (2025) [[Paper](https://arxiv.org/abs/2507.12144)] [[Code](https://github.com/NVlabs/FourCastNet)] — _FourCastNet 3: A geometric approach to probabilistic machine-learning weather forecasting at scale_
- **Aurora 1.5** [[Code](https://github.com/microsoft/aurora)]
- **Sonny-ENS** (2026) [[Paper](https://arxiv.org/abs/2611.01614)] — _Sonny-ENS: demystifying machine-learning ensemble weather forecasting_
- **Hybrid ML-Analog Downscaling / 混合机器学习-类比降尺度** (2026) [[Paper](https://arxiv.org/abs/2611.15284)] — _A hybrid machine learning-analog framework for downscaling unprecedented climate extremes_
- **Guided Temperature Diffusion / 观测引导的全球温度扩散模拟** (2026) [[Paper](https://arxiv.org/abs/2611.10882)] — _Guiding future global temperature distributions with simulations and observations_

---

## Radar Nowcasting / 雷达临近

- **NowcastNet**
- **DGMR** (2021) [[Paper](https://arxiv.org/abs/2104.00954)] [[Code](https://github.com/openclimatefix/skillful_nowcasting)] — _Skillful Precipitation Nowcasting using Deep Generative Models of Radar_
- **StormCast** (2024) [[Paper](https://arxiv.org/abs/2408.10958)] — _Kilometer-Scale Convection Allowing Model Emulation using Generative Diffusion Modeling_

---

## Satellite / 卫星

- **Global MetNet** (2025) [[Paper](https://arxiv.org/abs/2510.13050)] [[Code](https://github.com/openclimatefix/metnet)] — _An Operational Deep Learning System for Satellite-Based High-Resolution Global Nowcasting_
- **StormScope** (2026) [[Paper](https://arxiv.org/abs/2601.17268)] — _Skillful Thunderstorm Forecasts Learned Directly from Observations_
- **DDMS** (2024) [[Paper](https://arxiv.org/abs/2404.10512)] — _Four-hour thunderstorm nowcasting using a deep diffusion model of satellite data_
- **Observation-conditioned IMERG / 卫星条件降水生成** (2024) [[Paper](https://arxiv.org/abs/2412.02723)] — _DYffCast: Regional Precipitation Nowcasting Using IMERG Satellite Data. A case study over South America_
- **RainFlow** (2026) [[Paper](https://arxiv.org/abs/2611.09663)] — _RainFlow: Flow Matching for Infrared-Only Quantitative Precipitation Estimation_
- **PARDIG** (2026) [[Paper](https://arxiv.org/abs/2611.13941)] — _PARDIG: Global Precipitation Estimates Learned from Sparse Satellite Observations_
- **Multispectral SWR Nowcasting / 多光谱地表短波辐射临近预报** (2026) [[Paper](https://arxiv.org/abs/2611.12999)] — _Direct Multispectral Satellite Nowcasting of Gridded Surface Solar Radiation_
- **HybridCT** (2026) [[Paper](https://arxiv.org/abs/2611.16255)] — _HybridCT: ML Accelerated Tomography for Climate Relevant 3D Cloud Observations_

---

## Station / 站点

- **STGLDWeather** [[Code](https://github.com/ZhiPengWuBD/STGLD)]

---

## Multi-source / 多源与同化

观测驱动、端到端与同化耦合系统。

- **MetNet / MetNet-2 / MetNet-3** (2023) [[Paper](https://arxiv.org/abs/2306.06079)] [[Code](https://github.com/openclimatefix/metnet)] — _Deep Learning for Day Forecasts from Sparse Observations_
- **Aardvark Weather** (2024) [[Paper](https://arxiv.org/abs/2404.00411)] — _Aardvark weather: end-to-end data-driven weather forecasting_
- **FengWu-4DVar** (2023) [[Paper](https://arxiv.org/abs/2312.12455)] [[Code](https://github.com/OpenEarthLab/FengWu)] — _FengWu-4DVar: Coupling the Data-driven Weather Forecasting Model with 4D Variational Assimilation_
- **FuXi-Weather** (2024) [[Paper](https://arxiv.org/abs/2408.05472)] [[Code](https://github.com/tpys/fuxi-weather)] — _FuXi Weather: A data-to-forecast machine learning system for global weather_
- **FengLei / 风雷**
- **VeinCast** (2026) [[Paper](https://arxiv.org/abs/2608.09286)] — _VeinCast: Physics-Guided Dynamic Field Graphs with Graph-Conditioned Fusion for Global Medium-Range Weather Forecasting_
- **UniCM** [[Code](https://github.com/tsinghua-fib-lab/UniCM-Global-Climate-Modes)]
- **AI-GAMFS** (2024) [[Paper](https://arxiv.org/abs/2412.02498)] — _Advancing global aerosol forecasting with artificial intelligence_
- **LangYa / 琅琊** (2024) [[Paper](https://arxiv.org/abs/2412.18097)] — _LangYa: Revolutionizing Cross-Spatiotemporal Ocean Forecasting_
- **FuXi-TC** (2025) [[Paper](https://arxiv.org/abs/2508.16168)] [[Code](https://github.com/tpys/fuxi-weather)] — _FuXi-TC: A generative framework integrating deep learning and physics-based models for improved tropical cyclone forecasts_
- **FuXi-SHTM** (2025) [[Paper](https://arxiv.org/abs/2504.20852)] [[Code](https://github.com/tpys/fuxi-weather)] — _Machine Learning (ML)-Physics Fusion Model Outperforms Both Physics-Only and ML-Only Models in Typhoon Predictions_
- **3DTCR** (2026) [[Paper](https://arxiv.org/abs/2603.13049)] — _3DTCR: Vortex-following generative reconstruction improves tropical cyclone intensity prediction from global AI weather forecasts_
- **FuXi-CNOPs** (2026) [[Paper](https://arxiv.org/abs/2603.26165)] [[Code](https://github.com/tpys/fuxi-weather)] — _Error Growth Dynamic and Predictability of Tropical Cyclone in Machine Learning Weather Prediction Model_
- **DaYu-TC** (2026) [[Paper](https://arxiv.org/abs/2611.15266)] — _DaYu-TC: a global-regional nested AI system for tropical cyclone forecasting_
- **Aardvark Probabilistic** (2026) [[Paper](https://arxiv.org/abs/2608.30795)] — _Uncertainty-Aware End-to-End AI Weather Forecasting: Disentangling Observation and Model Contributions_
- **RainPro-8** (2025) [[Paper](https://arxiv.org/abs/2505.10271)] — _RainPro-8: An Efficient Deep Learning Model to Estimate Rainfall Probabilities Over 8 Hours_
- **Earth-2 Medium Range / Atlas**
- **玑衡 / Jiheng**

---

## Earth Observation Foundation Models / 地球观测基础模型

- **SatMAE** (2022) [[Paper](https://arxiv.org/abs/2207.08051)] — _SatMAE: Pre-training Transformers for Temporal and Multi-Spectral Satellite Imagery_
- **Prithvi-EO-1** (2023) [[Paper](https://arxiv.org/abs/2310.18660)] [[Code](https://github.com/NASA-IMPACT/Prithvi-EO-2.0)] — _Foundation Models for Generalist Geospatial Artificial Intelligence_
- **Prithvi-EO-2.0** (2024) [[Paper](https://arxiv.org/abs/2412.02732)] [[Code](https://github.com/NASA-IMPACT/Prithvi-EO-2.0)] — _Prithvi-EO-2.0: A Versatile Multi-Temporal Foundation Model for Earth Observation Applications_
- **AnySat** (2024) [[Paper](https://arxiv.org/abs/2412.14123)] — _AnySat: One Earth Observation Model for Many Resolutions, Scales, and Modalities_
- **Clay** [[Code](https://github.com/Clay-foundation/model)]
- **SkySense** (2023) [[Paper](https://arxiv.org/abs/2312.10115)] — _SkySense: A Multi-Modal Remote Sensing Foundation Model Towards Universal Interpretation for Earth Observation Imagery_
- **RingMo-Sense**
- **AlphaEarth Foundations** (2025) [[Paper](https://arxiv.org/abs/2507.22291)] — _AlphaEarth Foundations: An embedding field model for accurate and efficient global mapping from sparse label data_
- **TerraMind** (2025) [[Paper](https://arxiv.org/abs/2504.11171)] — _TerraMind: Large-Scale Generative Multimodality for Earth Observation_
- **SwinRDM** (2023) [[Paper](https://arxiv.org/abs/2306.03110)] — _SwinRDM: Integrate SwinRNN with Diffusion Model towards High-Resolution and High-Quality Weather Forecasting_
- **GeoSAE** (2026) [[Paper](https://arxiv.org/abs/2611.11398)] [[Code](https://github.com/EarthyScience/geosae)] — _Decomposing Earth Embeddings with Sparse Autoencoders_

---

## Datasets & Benchmarks / 数据集与基准

- **ERA5** — ECMWF 再分析（常用 AI 天气训练数据） [[CDS](https://cds.climate.copernicus.eu/)]
- **WeatherBench 2** — 新一代数据驱动全球天气预报基准 [[Code](https://github.com/google-research/weatherbench2)]
- **ClimateBench** — 气候模型仿真基准（见论文与社区仓库，条目随更新补充）
- **DailyWildfireCAN** — 加拿大次日野火蔓延预测数据集与基准 [[Paper](https://arxiv.org/abs/2611.14207)] [[Code](https://github.com/hagerradi/DailyWildFireCAN)]
- **Hydro-Dataset** — 北欧水文多模态开源管线与基础模型基准 [[Paper](https://arxiv.org/abs/2611.10992)]
- **HydroTuring** — 检验水文模型质量、能量与动量守恒的物理探针基准 [[Paper](https://arxiv.org/abs/2611.11563)] [[Code](https://github.com/Flood-Lab/HydroTuring)]
- **EarthVerse** — 面向动态地球系统与自然灾害的科学智能体基准，含 405 项可复现任务、199 个已记录事件与 19 类灾害 [[Paper](https://arxiv.org/abs/2608.23525)] [[Code](https://github.com/CuiZHIQ/Earth-Verse)]

---

## Toolkits & Platforms / 工具与平台

- **Earth2Studio** — NVIDIA AI 天气/气候工作流框架 [[Code](https://github.com/NVIDIA/earth2studio)]
- **PhysicsNeMo** — NVIDIA Physics-ML 训练与微调框架（含 CorrDiff 等组件） [[Code](https://github.com/NVIDIA/physicsnemo)]
- **WeatherNext** — Google DeepMind 天气模型开源代码集合（含 GraphCast / GenCast 等演进） [[Code](https://github.com/google-deepmind/weathernext)]
- **NeuralGCM** — Google 可微动力学 + ML 物理参数化 [[Code](https://github.com/neuralgcm/neuralgcm)]
- **ai-models (ECMWF Lab)** — 用 ECMWF 数据运行 AI 天气预报模型 [[Code](https://github.com/ecmwf-lab/ai-models)]
- **ACE (Ai2)** — Ai2 Climate Emulator 系列 [[Code](https://github.com/ai2cm/ace)]
- **Microsoft Aurora** — 地球系统预报模型实现 [[Code](https://github.com/microsoft/aurora)]
- **TorchGeo** — 地理空间数据集与预训练模型工具库 [[Code](https://github.com/torchgeo/torchgeo)]
- **PhysXAI** (2026) [[Paper](https://arxiv.org/abs/2611.15053)] — _PhysXAI: A Theoretical Framework for Diagnosing Physical Hallucinations in Weather Foundation Models_
- **AI-NWP FP16 Inference / 半精度推理** (2026) [[Paper](https://arxiv.org/abs/2611.09573)] [[Code](https://github.com/sieste/ai-nwp-fp16)] — _Half-precision inference of AI weather prediction models: negligible loss of skill at a fraction of the cost_

---

## Related Awesome Lists / 相关列表

- [awesome-time-series-foundation-models](https://github.com/lihuirui/awesome-time-series-foundation-models)
- [awesome-scientific-time-series-foundation-models-survey](https://github.com/lihuirui/awesome-scientific-time-series-foundation-models-survey)
- [awesome-multimodal-time-series-survey](https://github.com/lihuirui/awesome-multimodal-time-series-survey)

---

## Maintenance

- 欢迎 PR：请附可核验的 Paper / Code 链接；勿提交无法打开的 URL。
- 本仓库由例程每约 3 天增量检索一次（arXiv / GitHub），有实质更新时再推送。
- 详见 [CONTRIBUTING.md](CONTRIBUTING.md)。

## License

[CC0 1.0](LICENSE)（列表内容；各论文与代码遵循其原许可）
