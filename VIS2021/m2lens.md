## M2Lens: Visualizing and Explaining Multimodal Models for Sentiment Analysis

**Honorable Mention**

Xingbo Wang, Jianben He, Zhihua Jin, Muqiao Yang, Yong Wang, and Huamin Qu

> Multimodal models, sentiment analysis, explainable machine learning

## Abstract

Multimodal sentiment analysis aims to recognize people's attitudes from multiple communication channels such as verbal content (i.e., text), voice, and facial expressions. It has become a vibrant and important research topic in natural language processing. Much research focuses on modeling the complex intra- and inter-modal interactions between different communication channels. However, current multimodal models with strong performance are often deep-learning-based techniques and work like black boxes. It is not clear how models utilize multimodal information for sentiment predictions. Despite recent advances in techniques for enhancing the explainability of machine learning models, they often target unimodal scenarios (e.g., images, sentences), and little research has been done on explaining multimodal models. In this paper, we present an interactive visual analytics system, M2Lens, to visualize and explain multimodal models for sentiment analysis. M2Lens provides explanations on intra- and inter-modal interactions at the global, subset, and local levels. Specifically, it summarizes the influence of three typical interaction types (i.e., dominance, complement, and conflict) on the model predictions. Moreover, M2Lens identifies frequent and influential multimodal features and supports the multi-faceted exploration of model behaviors from language, acoustic, and visual modalities. Through two case studies and expert interviews, we demonstrate our system can help users gain deep insights into the multimodal models for sentiment analysis.

## Points

### Design Requirements

multimodal sentiment analysis에 관련된 model developers/model users를 target user로 잡았다.

'A' researcher와 5개월간의 인터뷰를 통해 총 4개의 Requirements를 뽑아내었다.

1. **R1: Show the model performance.**
    - Q1: What are the overall error distributions for model predictions?
    - Q2: What are the instances that are predicted with large/small errors?
2. **R2: Reveal the contributions of modalities to the model predictions.**
    - Q3: How does each modality influence the model predictions? 
    - Q4: Which modalities dominate the model predictions?
    - Q5: How do dominant/complementary/conflicting modalities influence the model predictions?
3. **R3: Identify the influences of multimodal features for the model predictions.**
    - Q6: What are the feature sets that significantly contribute to positive/negative sentiment predictions
    - Q7: What features are considered important by the model? Are they plausible for prediction?
4. **R4: Support multi-level and multi-faceted exploration of the multimodal model behaviors.**

### System

![overview interface](https://i.imgur.com/mZMYDwQ.jpg)

Multimodal sentiment analysis를 위한 시각화로 총 5가지의 view로 구성되어 있다.

- User Panel
- Summary View
- Projection View

Projection에서 데이터 마다 다른 표현법을 사용하려고 시도한 게 재밌다.

text는 점으로 표현했지만, video는 face glyph로, audio는 rose chart를 사용했다.

- Template View
- Instance View

### Evaluation

총 3명의 domain expert에게 2가지 Case Study 진행했다.

진행방식이 조금 특이하다고 느끼는데...

- Case 1 : Expert 1만
- Case 2 : Expert 2만
- Expert 3는 interview만

Case Study 1/2도 사용한 모델이 다르다. (Multimodal Transformer과 EF-LSTM)

Expert interview로는 크게 3가지로 피드백을 받았다.

- System workflow
- Visual designs and interaction
- Improvements

## 개인적인 평가

- 다양한 종류의 데이터를 하나의 시각화 시스템으로 표현했다는 점에서 기여.
  - 특히나 종류 간 발생할 수 있는 **dominance, complement, conflict**에 대해 시각적으로 표현했다는 점이 인상적.