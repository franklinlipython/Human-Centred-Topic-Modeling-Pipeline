# Human-Centred Topic Modeling of Online Conflict Discussions

## Project Overview

This project explores topic modeling and reflexive thematic analysis using the Conversations Gone Awry – ChangeMyView (CGA-CMV) corpus developed by Chang and Danescu-Niculescu-Mizil (2019) from Reddit’s (2025) ChangeMyView community. The goal of the assignment was to investigate how Latent Dirichlet Allocation (LDA) can be used to identify recurring themes in online discussions while also critically reflecting on the interpretability and stability of computational topic models.

The project was completed as part of INF2209: Human-Centred Topic Models at the University of Toronto.

---

## Research Objectives

The project focused on:

- Applying topic modeling techniques to large-scale conversational text data
- Evaluating topic quality using coherence metrics
- Assessing model stability across multiple random seeds
- Combining computational topic modeling with reflexive thematic analysis
- Interpreting online conversational dynamics through a human-centred lens

---

## Dataset

The analysis uses the Conversations Gone Awry – ChangeMyView (CGA-CMV) corpus (Chang & Danescu-Niculescu-Mizil, 2019).

This dataset contains Reddit discussions from the ChangeMyView community and was designed to study conversational trajectories and interaction patterns in online discourse.

The corpus was accessed and processed using the ConvoKit toolkit (Chang et al., 2020; Chang et al., 2025).

---

## Methods

### 1. Data Cleaning and Preprocessing

The preprocessing pipeline included:

- Lowercasing text
- Removal of HTML artifacts and quotations
- Contraction handling using the `contractions` Python package (van Kooten, 2021)
- Stopword removal with extended custom stopword lists
- Lemmatization using SpaCy
- Bigram and trigram phrase modeling
- Conversion to Bag-of-Words representations for LDA

### 2. Topic Modeling

Latent Dirichlet Allocation (LDA) models were trained using Gensim (Řehůřek & Sojka, 2010).

The workflow included:

- Testing multiple topic numbers (K-values)
- Computing coherence scores across the K-grid
- Selecting the optimal number of topics based on coherence evaluation
- Training the final LDA model using the selected K-value

### 3. Stability Analysis

To evaluate robustness and reproducibility, the project compared topic models across multiple random seeds.

This included:

- Cross-seed topic alignment
- Jaccard similarity comparisons
- Hungarian matching for topic alignment
- Stability evaluation across repeated model runs

### 4. Reflexive Thematic Analysis

Following topic modeling, selected topics were interpreted qualitatively through reflexive thematic analysis following Braun and Clarke’s (2006) framework.

This stage involved:

- Reviewing top representative documents
- Examining borderline or ambiguous documents
- Interpreting latent themes contextually
- Reflecting on the limitations of computational interpretation
- Connecting quantitative outputs with qualitative meaning-making

---

## Key Findings

The project demonstrated that:

- Topic coherence alone does not guarantee interpretability
- Topic stability varies across random seeds
- Human interpretation remains essential in topic modeling workflows
- Computational and qualitative methods can complement one another effectively
- Online discussions often contain overlapping and context-dependent themes

---

## Notes

This repository is intended for educational and research demonstration purposes.

The analysis emphasizes both the technical and interpretive dimensions of topic modeling, particularly the importance of critical reflection when working with machine-generated themes in human communication data.

---

## References

- Braun, V., & Clarke, V. (2006). *Using thematic analysis in psychology*. Qualitative Research in Psychology, 3(2), 77–101. https://doi.org/10.1191/1478088706qp063oa

- Chang, J. P., Chiam, C., Fu, L., Wang, A. Z., Zhang, J., & Danescu-Niculescu-Mizil, C. (2020). *ConvoKit: A toolkit for the analysis of conversations*. Proceedings of the 21st Annual Meeting of the Special Interest Group on Discourse and Dialogue, 57–60. https://doi.org/10.18653/v1/2020.sigdial-1.8

- Chang, J. P., Chiam, C., Fu, L., Wang, A. Z., Zhang, J., & Danescu-Niculescu-Mizil, C. (2025). *ConvoKit (Version 3.5.0) [Software library]*. https://convokit.cornell.edu/

- Chang, J. P., & Danescu-Niculescu-Mizil, C. (2019). *Trouble on the horizon: Forecasting the derailment of online conversations as they develop*. Proceedings of the 2019 Conference on Empirical Methods in Natural Language Processing and the 9th International Joint Conference on Natural Language Processing, 4743–4754. https://doi.org/10.18653/v1/d19-1481

- Reddit. (2025). *r/changemyview*. https://www.reddit.com/r/changemyview/

- Řehůřek, R., & Sojka, P. (2010). *Software framework for topic modelling with large corpora*. Proceedings of the LREC 2010 Workshop on New Challenges for NLP Frameworks, 46–50. https://doi.org/10.13140/2.1.2393.1847

- van Kooten, P. (2021). *Contractions (Version 0.1.73) [Python package]*. GitHub. https://github.com/kootenpv/contractions
