# Semantic Outlier Removal with Embedding Models and LLMs

<div align="center">

[![Website](https://img.shields.io/badge/Project-Page-blue.svg)](https://meakbiyik.com/sore/)
[![Paper](https://img.shields.io/badge/arXiv-2506.16644-b31b1b.svg)](https://arxiv.org/abs/2506.16644)
[![ACL 2025](https://img.shields.io/badge/ACL-2025-blue.svg)](https://2025.aclweb.org/)
[![Dataset](https://img.shields.io/badge/Dataset-Coming%20Soon-orange.svg)]()

</div>

This repository will host the code and evaluation datasets for our paper **"Semantic Outlier Removal with Embedding Models and LLMs"**, accepted at ACL 2025. It includes the implementation of our novel content extraction method, **SORE**, and the SORE-SMALL and SORE-LARGE datasets used for evaluation.

**Please note:** The code and datasets are not yet available in this repository but will be uploaded shortly to facilitate further research.

<div align="center">
<img src="https://meakbiyik.com/assets/img/sore-1400.webp" alt="SORE Pipeline" style="max-width:auto; max-height:300px;" />
</div>

## Overview

Modern NLP pipelines require robust methods to clean web documents, removing extraneous content like ads, navigation bars, and legal disclaimers while preserving the core message. Traditional methods that rely on HTML structure often struggle with diverse website layouts and multiple languages. While Large Language Models (LLMs) offer higher quality, they come with significant computational costs and latency, making them challenging for large-scale production systems.

To bridge this gap, we introduce **SORE (Semantic Outlier Removal)**, a cost-effective and transparent system that leverages multilingual sentence embeddings to achieve near-LLM precision at a fraction of the cost. SORE works by:
* **Identifying core content** using the document's metadata (e.g., title) as a semantic anchor.
* **Detecting outliers** by flagging text segments that are either too semantically distant from the core content or too close to predefined categories of unwanted content (e.g., "ads," "legal disclaimers").

This approach is language-agnostic, scalable, and provides clear explanations for why content is removed, making it ideal for industrial applications.

In this repository, you will eventually find:

* **Code:** The production-ready implementation of the SORE algorithm and its evaluation scripts.
* **SORE Datasets:** The `SORE-SMALL` and `SORE-LARGE` datasets used in our experimental evaluation, complete with ground-truth main content for benchmarking extraction methods.

## Abstract

Modern text processing pipelines demand robust methods to remove extraneous content while preserving a document's core message. Traditional approaches such as HTML boilerplate extraction or keyword filters often fail in multilingual settings and struggle with context-sensitive nuances, whereas Large Language Models (LLMs) offer improved quality at high computational cost. We introduce SORE (Semantic Outlier Removal), a cost-effective, transparent method that leverages multilingual sentence embeddings and approximate nearest-neighbor search to identify and excise unwanted text segments. By first identifying core content via metadata embedding and then flagging segments that either closely match predefined outlier groups or deviate significantly from the core, SORE achieves near-LLM extraction precision at a fraction of the cost. Experiments on HTML datasets demonstrate that SORE outperforms structural methods and yield high precision in diverse scenarios. Our system is currently deployed in production, processing millions of documents daily across multiple languages while maintaining both efficiency and accuracy. To facilitate further research, we will publicly release our implementation and evaluation datasets.

## Citation

If you use our work, please consider citing our paper:

```bibtex
@inproceedings{akbiyik2025sore,
  title={Semantic Outlier Removal with Embedding Models and LLMs},
  author={Akbiyik, Eren and Almeida, Jo{\~a}o and Melis, Rik and Sriram, Ritu and Petrescu, Viviana and Vilhj{\'a}lmsson, Vilhj{\'a}lmur},
  booktitle={Proceedings of the 63rd Annual Meeting of the Association for Computational Linguistics},
  year={2025},
  publisher={Association for Computational Linguistics}
}
