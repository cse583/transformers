# Transformers for Hot Path Prediction

Programs often spend most of their execution time in a small portion of their code, referred to as "hot paths." Identifying these hot paths is critical for optimizing program performance. For instance, compiler optimizations like loop unrolling can be more aggressively applied to these sections of code.

Traditionally, identifying hot paths requires dynamic profiling, which involves executing the program. However, dynamic profiling is computationally expensive and time-consuming. This study explores the potential of static analysis using machine learning to predict hot paths without executing the program, significantly reducing overhead.

## Approach

We created a custom dataset using the PolyBench Benchmark Suite by implementing and running the [Ball-Larus path profiling algorithm](https://github.com/cse583/ball-larus). This provides the ground truth for our data.

Then, we fine-tuned a state-of-the-art transformer model, BERT, on our dataset. The resulting model achieves an impressive 99% accuracy in static hot path prediction on 4 new programs.

## Files/Directory Description

This repository contains the following files.

| File        | Description |
| ----------- | --------- |
|`CreateDataset.ipynb` | Python notebook used to create the dataset, which is publicly available at Hugging Face [zhaojer/compiler_hot_paths](https://huggingface.co/datasets/zhaojer/compiler_hot_paths) |
|`BERT.ipynb` | Python notebook used to fine-tune the BERT model, which is available at Hugging Face [zhaojer/bert-hot-path-predictor](https://huggingface.co/zhaojer/bert-hot-path-predictor) |

For instructions on the usage of the resulting dataset and model, please see their respective Hugging Face repos.

## Further Reading

Please see our [paper](https://github.com/cse583/transformers/blob/main/CSE_583_Final_Report.pdf).
