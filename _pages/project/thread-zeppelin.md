---
layout: page
title: "Thread Zeppelin"
permalink: /projects/thread-zeppelin/
---

<div class="project-meta">
  <strong>Role:</strong> Product Owner &nbsp;|&nbsp; 
  <strong>Timeline:</strong> September 2025 – May 2026 &nbsp;|&nbsp; 
  <strong>Type:</strong> Capstone Project — University of Maine
</div>

## Overview

Generative Artificial Intelligence has become increasingly important due to its ability to generate human-like text, summarize information, and answer complex questions across many domains. The team, Thread Zeppelin, examined three small language models and explored how different training approaches influence model behavior and task performance. We adapted Mistral 7B Instruct, Gemma 7B it, and OLMo Hybrid 7B using prompt engineering and fine tuning. We used a dataset provided by the Advance Structures and Composites Center (ASCC) at the University of Maine along with Kaggle for cloud training, GitHub for version control, and Hugging Face for accessing pretrained models and utilizing the Transformers library for implementation and experimentation. We found Mistral was the fastest model in both training and inference by a significant margin. The team was accepted and presented at the 2026 University of Maine Student Symposium.

## My Role

As Product Owner, I led the research and evaluation of technical approaches
for adapting large language models (LLMs) to summarize large datasets.

## Research & Approach

The core research questions was whether small lanugage models could meaningfully summarize structured manufacturing data and whether the method used to adapt them made a measureable difference in output quality. For this we used Mistral 7B Instruct, Gemma 7B it, and OLMo Hybrid 7B as our models and prompt engineering and fine-tuning for our adaptation methods.

We began by testing prompt engineering using three variants: a basic prompt, a structure prompt with explicit formatting instructions, and a one-shot prompt that included a worked example. We then applied fine-tuning using LoRA (Low-Rank Adapatation) to all three models using idetically hyperparameters so that any differences in output quality could be attributed to the models themselves rather than the training configuration. We studied retrieval-augemented generation but did not implement it as the dataset was small enough to fit directly into a prompt and adding a retrieval layer would have introduced confounding variables.

The dataset was derived from manufacturing records provided by the ASCC, including print telemetry CSVs, ROS machine logs, and operator check-sheets. Because only one real operator check-sheet with natural-language notes existed, 21 synthetic operator-style records were generated from real telemetry data to supplement the training set. All training and inference ran on Kaggle's free GPU T4 × 2 tier to keep hardware conditions identical across all three models.

## Symposium Presentation

This project was accepted and presented at the **University of Maine Student Symposium**,
where the team communicated technical findings to a broad, mixed audience.

## Technologies Used

- Python, PyTourch, Hugging Face Transformers
- PEFT (LoRA adapters), TRL (SFTTrainer), bitsandbytes (4-bit quantization)
- Mistral Instruct 7B, Gemma 7B it, OLMo Hybrid 7B
- Kaggle GPU T4 x 2 (training and inference environment)
- GitHub (version control and public reproducibility)

## Challenges & What I Learned

The most significant technical challenge was input formatting. Each model required a different format. Mistral has a well-structured chat template that automated formatting handled cleanly. Gemma does not support separate system messages, so system content had to be merged into the user turn before training. OLMo has no instruction-tuned chat template at all, which required building plain-text formatting from scratch. All three models ended up trained on different input formats despite using identical hyperparameters everywhere else. That made it harder to isolate model architecture as the variable.

The dataset was a challenge as well. Only one real operator check-sheet with natural-language notes existed. Twenty-one synthetic records had to be generated to make fine-tuning feasible. The limited variety in the synthetic note pool is a known limitation of the results.

The biggest takeaway was that adaptation method matters more than model choice at the same parameter scale. Fine-tuning on 36 records produced consistently cleaner summaries than the best prompt-engineering baseline across all three models. The other takeaway was about team structure. Shared technical understanding is not overhead. Earlier cross-team involvement in the LLM work may have changed the project's trajectory significantly.

## Gallery / Materials

<div class="project-gallery">
  <!-- Add poster, slides, or demo screenshots here once available.
  <img src="/assets/images/thread-zeppelin/poster.png" alt="Symposium poster" />
  -->
</div>

## Links

<div class="project-links">
  <a href="https://github.com/grelmu/thread-zeppelin" target="_blank">GitHub Repo</a>
  <!-- <a href="[poster or paper PDF URL]" target="_blank">Research Poster</a> -->
  <!-- <a href="[presentation slides URL]" target="_blank">Slides</a> -->
</div>
