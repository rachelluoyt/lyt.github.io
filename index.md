---
layout: default
---

NLP models have recently achieved outstanding performances and are thus gained prevalent applications in real world. With this popularity, it is important to make sure these models could adapt well in the dynamic circumstances. More specifically, robustness with respect to domain shifts is supposed to be considered when developing models. Because the same large pretrained language models are often applied to different tasks or fields. It would be inefficient and impractical if we train the model with corresponding inputs every time we apply them to a different domain. We want large models can be easily reused. Improvement on models to ensure they are robust against change of inputs has been a hot topic for study.

# Introduction

Prompt tuning and prefix tuning are two effective mechanisms to leverage frozen language models to perform downstream tasks. Robustness reflects models' resilience of output under a change or noise in the input. In this project, we analyze the robustness of natural language models using various tuning methods with respect to a domain shift (i.e. training on a domain but evaluating on out-of-domain data). We apply both prompt tuning and prefix tuning on T5 models for reading comprehension (i.e. question-answering) and GPT-2 models for table-to-text generation.

# Datasets & Evaluation Metrics
- GPT-2 Table-to-Text generations
  - Train on **[WebNLG](https://aclanthology.org/W16-6626/).**
  - Test on **[DART](https://arxiv.org/abs/2007.02871).**
  - Evaluate with **[BLEU](https://aclanthology.org/P02-1040.pdf).**

- T5 Qustion & Answering
  - Train on **[SQuAD](https://arxiv.org/abs/1606.05250).**
  - Test on **[DuoRC](https://arxiv.org/abs/1804.07927).**
  - Evaluate with **[EM/F1](https://arxiv.org/abs/1910.09753).**



###### Results

|\2. Configuration|\2. In-Domaain|\2. Out-of-Domain|
|Size  | #Tkns| EM|F1|EM|F1|
|:-------------|:------------------|:------|
|small|1| 17.86 | 56.88|2.27|25.17


