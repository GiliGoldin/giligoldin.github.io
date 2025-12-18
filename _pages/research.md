---
title: "Research"
permalink: /research/
author_profile: true
---
My research focuses on natural language processing, computational linguistics, and AI, with an emphasis on multilingual and morphologically rich languages. 

My PhD research has focused on the computational analysis of political discourse in Hebrew. I develop data-driven NLP models and annotated datasets to study polarization, stylistic variation, gender differences, and the truthfulness and reliability of parliamentary speech.

Below, I list selected publications from my PhD, together with brief abstracts and illustrative figures.


---

## 📄 Unveiling Affective Polarization Trends in Parliamentary Proceedings (2025)

**Authors:** Gili Goldin, Ella Rabinovich, Shuly Wintner

**Venue:** Accepted to Computational Linguistics (MIT Print)

**Links:** [PDF](https://arxiv.org/pdf/2512.05231) • [Code](https://github.com/HaifaCLG/Polarization) • [Dataset (Hebrew VAD Lexicon)](https://huggingface.co/datasets/GiliGold/Hebrew_VAD_lexicon)  • [Dataset (VAD_Knesset_corpus)](https://huggingface.co/datasets/GiliGold/VAD_KnessetCorpus)

**Abstract.**  
Recent years have seen an increase in polarized discourse worldwide, on various platforms. We propose a novel method for quantifying polarization, based on the emotional style of the discourse rather than on differences in ideological stands. Using measures of Valence, Arousal and Dominance, we detect signals of emotional discourse and use them to operationalize the concept of affective polarization. Applying this method to a recently released corpus of proceedings of the Knesset, the Israeli parliament (in Hebrew), we find that the emotional style of members of government differs from that of opposition members; and that the level of affective polarization, as reflected by this style, is significantly increasing with time.

<img src="{{ '/images/papers/polarizaion/flow-color-3-encoder.png' | relative_url }}"
     alt="VAD prediction combined model flow"
     style="width: 60%; display: block; margin: 0 auto;">

*Figure 1: The Encoder LLM receives a sentence as input and
generates its sentence embedding. This embedding is then used as input for the regression
models, which predict the Valence (V), Arousal (A) and Dominance (D) scores for the sentence.*




<img src="{{ '/images/papers/polarizaion/model-diagram_color-3.png' | relative_url }}"
     alt="Knesset-multi-e5-large model diagram"
     style="width: 60%; display: block; margin: 0 auto;">

*Figure 2:The Knesset-multi-e5-large model, the chosen LLM for extracting sentence embeddings
(see Figure 1). It was created by fine-tuning the encoder part of the multilingual-e5-large
model on the Knesset data, and then combining the tuned encoder with the original
sentence-transformer.*

<div style="display: flex; gap: 20px; justify-content: center;">
  <img src="{{ '/images/papers/polarizaion/v-var-avg-over-all-committeess-per-knesset.png' | relative_url }}" 
       alt="Figure 1" style="width: 45%;">
  <img src="{{ '/images/papers/polarizaion/a-mean-avg-over-all-committeess-per-knesset.png' | relative_url }}" 
       alt="Figure 2" style="width: 45%;">
</div>

<p style="text-align: center;">
  <em>Figure 3: Average A-mean and V-var over all committees, over time (Knesset session). Dashed lines
represent the automatically computed trend lines.</em>
</p>




---

## 📄 Another Paper Title (Year)

**Authors:** …  
**Venue:** …

**Abstract.**  
…

![Another figure](/images/papers/paper2_plot.png)

