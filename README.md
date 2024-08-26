# 🚀 Exploring the Power of Unfine-tuned Generative Large Language Models: Gemma 2B's Zero/One/Few Shot Learning Performance 🪄

## Introduction

In Named Entity Recognition (NER) tasks, Transformer-based models like BERT and DeBERTa are often the go-to solutions. When fine-tuned with a well-prepared dataset, these models deliver remarkable results in terms of accuracy, recall, precision, and F1 scores. However, gathering and processing data for NER tasks is typically a time-consuming process, often requiring manual annotation and conversion to the BIO format.

## About Dataset

This dataset includes the official [PII Data Detection](https://www.kaggle.com/competitions/pii-detection-removal-from-educational-data) training dataset from The Learning Agency Lab (`train.json`) and an external dataset version from a related [notebook](https://www.kaggle.com/code/valentinwerner/fix-punctuation-tokenization-external-dataset) (`moredata_dataset_fixed.json` and `pii_dataset_fixed.json`).

### Dataset Description

In the era of abundant educational data from sources like ed tech, online learning, and research, detecting Personally Identifiable Information (PII) is crucial. PII poses risks when releasing educational data publicly, as it could endanger students' privacy. The current manual screening process, while reliable, is costly and limits dataset scalability. Existing automatic PII detection methods, relying on named entity recognition (NER), often struggle with nuanced cases such as distinguishing sensitive names from non-sensitive ones. This competition, hosted by Vanderbilt University in collaboration with The Learning Agency Lab, aims to develop reliable automated PII detection techniques. 


## Experiment Overview

This project explores the performance of Google's pre-trained generative large language model, **Gemma 2B**, in NER tasks without any fine-tuning or additional training. The focus is on evaluating the model's Zero, One, and Few Shot Learning capabilities using a limited number of samples. The experiments were conducted using the publicly available [PII dataset on Kaggle](https://www.kaggle.com/datasets). The model's performance was assessed using F1 scores, with experiments conducted across six scenarios: Zero Shot, One Shot, Three Shot, Five Shot, Seven Shot, and Nine Shot Learning.

## Key Findings

- **Zero-Shot Capabilities:** Even without specific examples, Gemma 2B could identify some named entities just by receiving a task prompt.
- **Improved Performance with More Examples:** As the number of examples provided in the prompt increased, both the inference time and model performance improved.
- **Non-linear Performance:** Interestingly, the performance did not consistently improve with more examples. For instance, using nine examples did not necessarily yield better results than three, five, or seven examples.
- **Generative Model Challenges:** While generative models are powerful, they also introduce challenges, such as generating non-existent entities, which requires careful consideration during application.

## Conclusion

Generative large language models like Gemma 2B, combined with few-shot learning, offer a viable alternative when datasets are scarce or difficult to compile. However, the key is determining the optimal number of examples needed to achieve the best performance. Despite their potential, these models still require caution due to issues like hallucination, where the model generates incorrect entities.

## Visual Report

🌟 Below is a visual report summarizing the experiment's results:

*Include GIF or image here demonstrating the experimental results.*

## Access the Code

🌟 The code used for this experiment is available here: [Kaggle Link](https://www.kaggle.com/code/xiaohualu/perform-gemma2b-ner-by-zero-one-fewshot/edit/run/167873631).

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.
