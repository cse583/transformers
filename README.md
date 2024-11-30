# Transformers for Hot Path Prediction

We created a dataset from the PolyBench Benchmark Suite and used it to fine-tune a BERT model to perform hot path prediction.

This repository contains the following files.

| File        | Description |
| ----------- | --------- |
|`CreateDataset.ipynb` | Python notebook used to create the dataset, which is publicly available at Hugging Face [zhaojer/compiler_hot_paths](https://huggingface.co/datasets/zhaojer/compiler_hot_paths) |
|`BERT.ipynb` | Python notebook used to fine-tune the BERT model, which is available at Hugging Face [zhaojer/bert-hot-path-predictor](https://huggingface.co/zhaojer/bert-hot-path-predictor) |

For more details about the dataset and the model, please see their Hugging Face repos.
