## Human-in-the-loop Extraction of Interpretable Concepts in Deep Learning Models

Zhenge Zhao, Panpan Xu, Carlos Scheidegger, Liu Ren

### Abstract

The interpretation of deep neural networks (DNNs) has become a key topic as more and more people apply them to solve various problems and making critical decisions. Concept-based explanations have recently become a popular approach for post-hoc interpretation of DNNs. However, identifying human-understandable visual concepts that affect model decisions is a challenging task that is not easily addressed with automatic approaches. We present a novel human-in-the-loop approach to generate user-defined concepts for model interpretation and diagnostics. Central to our proposal is the use of active learning, where human knowledge and feedback are combined to train a concept extractor with very little human labeling effort. We integrate this process into an interactive system, ConceptExtract. Through two case studies, we show how our approach helps analyze model behavior and extract human-friendly concepts for different machine learning tasks and datasets and how to use these concepts to understand the predictions, compare model performance and make suggestions for model refinement. Quantitative experiments show that our active learning approach can accurately extract meaningful visual concepts. More importantly, by identifying visual concepts that negatively affect model performance, we develop the corresponding data augmentation strategy that consistently improves model performance.

## Points

### Related work

우선 이 논문을 이해하기 위해서는 몇 가지 기본 개념이 필요하다.

1. Active Learning 
   - 고전적인 모델링 : 데이터를 전부 레이블링해서 넣는 방식
   - Active Learning : 데이터를 일부 학습하고, 필요한 데이터를 선택해서 레이블링을 하는 방식
2. Concept-based Explanation

### Task

- T1: Summarize model behavior.
- T2: Browse and explore image patches/super-pixels.
- T3: Train and evaluate concept extraction models.
- T4: Analyze how visual concepts affect model decisions.
- T5: Compare different models.

### System

![concept extract](https://i.imgur.com/Lw2WTkx.jpg)

