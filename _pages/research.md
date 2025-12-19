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
     style="width: 65%; display: block; margin: 0 auto;">

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

## 📄 An Annotation Scheme for Factuality and its Application to Parliamentary Proceedings (2025)

**Authors:** Gili Goldin, Shira Wigderson, Ella Rabinovich, Shuly Wintner

**Venue:** Proceedings of the 15th International Conference on Recent Advances in Natural Language Processing - Natural Language Processing in the Generative AI Era

**Links:** [PDF](https://acl-bg.org/proceedings/2025/RANLP%202025/pdf/2025.ranlp-1.49.pdf) • [Code](https://github.com/HaifaCLG/Factuality) • [Dataset](https://huggingface.co/datasets/GiliGold/Knesset_check_worthiness)  • 

**Abstract.**  
Factuality assesses the extent to which a language utterance relates to real-world information; it determines whether utterances correspond to facts, possibilities, or imaginary situations, and as such, it is instrumental for fact checking. Factuality is a complex notion that relies on multiple linguistic signals, and has been studied in various disciplines. We present a complex, multi-faceted annotation scheme of factuality that combines concepts from a variety of previous works. We developed the scheme for Hebrew, but we trust that it can be adapted to other languages. We also present a set of almost 5,000 sentences in the domain of parliamentary discourse that we manually annotated according to this scheme. We report on inter-annotator agreement, and experiment with various approaches to automatically predict (some features of) the scheme, in order to extend the annotation to a large corpus.


---

## 📄 The Knesset corpus: an annotated corpus of Hebrew parliamentary proceedings (2025)

**Authors:** Gili Goldin, Nick Howell, Noam Ordan, Ella Rabinovich, Shuly Wintner

**Venue:** Language Resources and Evaluation

**Links:** [PDF](https://link.springer.com/article/10.1007/s10579-025-09833-4) • [Code](https://github.com/HaifaCLG/KnessetCorpus) • [Dataset](https://huggingface.co/datasets/HaifaCLGroup/KnessetCorpus)  • 

**Abstract.**  
We present the Knesset Corpus, a corpus of Hebrew parliamentary proceedings containing over 30 million sentences (over 384 million tokens) from all the (plenary and committee) protocols held in the Israeli parliament in the last three decades. Sentences are annotated with morpho-syntactic information and named entities, and are associated with detailed meta-information reflecting demographic and political properties of the speakers, based on a large database of parliament members and factions that we compiled. We discuss the structure and composition of the corpus and the various processing steps we applied to it. To demonstrate the utility of this novel dataset we present two use cases. We show that the corpus can be used to examine historical developments in the style of political discussions by showing a reduction in lexical richness in the proceedings over time. We also investigate some differences between the styles of male and female speakers. These use cases exemplify the potential of the corpus to shed light on important trends in the Israeli society, supporting research in linguistics, political science, communication, law, etc.




**Diachronic changes in linguistic style**
<img src="{{ '/images/papers/knesset_corpus/ttr-word-frequency-charts.png' | relative_url }}"
     alt="TTR and word freq"
     style="width: 80%; display: block; margin: 0 auto;">
*Figure: Average TTR and word frequency in Knesset plenary and committee sessions.
Statistically significant evidence (at p<0.001) for decreasing TTR was observed for
both committee and plenary sessions, and for increasing word frequency in committee
protocols. Expectedly, higher TTR and conversely, lower word frequency, were found
for the (less formal) plenary sessions.*

**Gender-based differences in verb voice**

<img src="{{ '/images/papers/knesset_corpus/table4.png' | relative_url }}"
     alt="voice differences"
     style="width: 60%; display: block; margin: 0 auto;">
*Table: Usage of verb voice by men and women*


