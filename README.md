# Cheng Xie

**Phone:** +86 177 7914 4045  
**Email:** 17779144045@163.com  

## Research Interests
- Reinforcement learning for large language models (RLHF/RLAIF), preference optimization (e.g., DPO/PPO/GRPO-style training), reward modeling, and controllable alignment.
- Efficient inference for online/iterative RL training (sampling throughput, latency, vLLM internals, prefix caching, chunked prefill) and training–inference co-design.
- Distributed LLM training and optimization on GPU/NPU clusters (DP/TP/PP, mixed precision, profiling-driven performance tuning).

## Education
**B.Eng., Computer Science and Technology**, Nanchang University (Double First-Class), China  
*Sep 2017 – Jun 2021*  
Selected coursework: Data Structures, Computer Networks, Operating Systems, Computer Architecture, Database Systems, Compiler Principles, Linux Programming.

## Professional Experience
**Huawei Technologies Co., Ltd. (Ascend Computing)** — *Ascend AI Developer Engineer*  
*Sep 2024 – Jan 2026*

**Shanghai Yanding Information Technology Co., Ltd.** — *C++ Software Engineer*  
*Nov 2023 – Sep 2024*

**China General Nuclear Digital Technology Co., Ltd.** — *Software Development Engineer*  
*Jul 2021 – Oct 2023*

## Selected Research & Engineering Projects

### Direct Preference Optimization (DPO/RLHF) for Vevo Zero-Shot Voice Imitation (Current on-going)
*(Feb 2026 – Present)*  
- Built an **automated preference alignment pipeline** for the Flow-Matching acoustic model in Vevo, enabling significantly higher-quality controllable voice conversion and TTS.  
- Designed and implemented an end-to-end **audio preference data generation & filtering system** that produces exactly one chosen and one rejected sample per utterance.
- Performed **Direct Preference Optimization (DPO)** fine-tuning on the Flow-Matching Transformer, teaching the model to strongly prefer natural, stable, and speaker-faithful generations.  
- For more details, please refering to this [link](https://github.com/XieCh0801/Amphion/tree/main/models/vc/vevo). 

### LLM Post-training & RL Alignment (DeepSeek-R1 reproduction on Qwen2.5-32B reasoning alignment)  
*Oct 2024 – Jan 2026*
- Studied and operationalized post-training and alignment paradigms (DPO, PPO, GRPO and related variants) into an end-to-end pipeline: data → sampling → optimization → evaluation.
- Conducted controlled comparisons of training recipes and analyzed outcomes via reproducible experiments (fixed data slices, fixed seeds, consistent evaluation).
- Investigated coupling between inference efficiency and RL training cost (sampling throughput, initialization overhead, and their impact on wall-clock training).

### vLLM Inference Stack Upgrade ([MindSpeed-RL](https://gitcode.com/Ascend/MindSpeed-RL) / Verl-NPU)  
*Oct 2024 – Jan 2026*
- Upgraded and adapted vLLM versions for RL training workloads; identified breaking changes, implemented compatibility shims, and built regression test cases.
- Performed accuracy and metric regression checks across versions; traced infra-induced discrepancies and delivered fixes/workarounds.
- Analyzed vLLM initialization/execution path and integrated inference features (e.g., prefix caching, chunked prefill) to improve sampling efficiency.

### xPO Multi-Reward RLVR Training Paradigm (MindSpeed-RL)  
*Oct 2024 – Jan 2026*
- Designed and implemented a multi-reward mixing mechanism for RLVR training, including reward aggregation, weighting strategies, interfaces, and monitoring.
- Ran ablations to quantify how reward compositions affect convergence, preference alignment, and generalization; summarized findings into reusable docs and templates.

### Distributed Pretraining & Performance Optimization with Megatron-Core  
*Nov 2023 – Sep 2024*
- Implemented distributed training scripts with DP/TP/PP configurations; reasoned about communication–computation overlap, gradient synchronization, and stability.
- Diagnosed bottlenecks with profiling tools (communication, kernels, memory footprint, convergence anomalies) and executed validated optimizations.
- Built a regression workflow to track loss/throughput/memory with reproducibility.

## Additional Systems Projects

### Computer Vision Quality Inspection for Camera & ADAS  
*Nov 2023 – Sep 2024*
- Developed and maintained image-quality modules (uniformity/blemish detection, flare/flicker analysis, ghost detection automation) using OpenCV and industry standards.

### High-Concurrency Keyword Suggestion Search Engine (C++)  
*Aug 2022 – Sep 2023*
- Built a multi-module web search engine with Reactor + epoll + thread pool; implemented inverted indexing, TF-IDF weighting, SimHash deduplication, and suggestion via edit distance.

### Enterprise Cloud Storage Service (C/C++)  
*Sep 2021 – Jul 2022*
- Implemented concurrent file upload/download management with epoll/thread pool; supported resumable transfers, “instant upload” via MD5, and MySQL-backed virtual file systems.

## Technical Skills
- **Programming:** C/C++ (STL, C++11), Python (training scripts, evaluation and tooling), basic Java.
- **ML/RL:** DPO/PPO/GRPO-style alignment training, reward modeling/preference learning concepts, evaluation design, training stability and monitoring.
- **Systems:** Linux, multithreading, TCP/IP, IO multiplexing (select/poll/epoll), Reactor pattern.
- **Distributed Training:** DP/TP/PP parallelism, mixed precision, profiling-driven optimization; GPU/NPU adaptation.
- **Databases & Tools:** MySQL (indexes, transactions, isolation levels), basic Redis; git, gcc/gdb, make/cmake, VS Code.
