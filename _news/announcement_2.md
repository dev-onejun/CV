---
layout: post
title: "I successfully defended my Master's thesis at the University of Texas at Arlington! 🎓 ✨"
date: 2026-04-17 09:00:00-0500
inline: false
related_posts: false
---

**Title.** *Universal Sound Separation: Distance-Aware Mixture Simulation, Co-occurrence Conditioning, and Chain-of-Inference*

**Advisor.** Dr. Kenny Q. Zhu

**Committee.** Dr. Vassilis Athitsos, Dr. Shirin Nilizadeh

---

#### Abstract

Universal Sound Separation (USS) — the task of disentangling arbitrary sound sources from a single-channel acoustic mixture — remains an open challenge due to the ill-posed nature of the problem and the distributional gap between synthetic training data and real-world recordings. This thesis addresses three distinct bottlenecks in the USS pipeline: training data realism, inference strategy, and conditioning richness.

We first present two knowledge-guided approaches to sound source separation. The first is a *distance-aware* mixing strategy that leverages Large Language Models (LLMs) to assign plausible loudness relationships between audio sources during training data synthesis. By querying an LLM about the natural acoustic distance between sound events, we generate Mixtures of Mixtures (MoMs) that better approximate real-world acoustic scenes. Human evaluation shows that models trained with this strategy are preferred over randomly-trained baselines in up to 75% of comparisons on three real-world benchmark categories. The second is a *co-occurrence conditioning* framework that injects information about non-target sounds present in a mixture into the encoder of AudioSep via FiLM modulation, complementing the standard target conditioning. We propose a CLAP-based estimation procedure that approximates co-occurrence embeddings at inference time from only the mixture and the target text, matching the practical setting of USS; an exploratory evaluation shows improved separation on five of six USS benchmarks.

We then introduce Chain-of-Inference (CoI), a *training-free* multi-step inference framework motivated by the human auditory system's sensitivity to sudden changes in the acoustic scene and structurally analogous to Chain-of-Thought prompting in language models. CoI iteratively re-introduces a proportion of the original mixture — governed by cosine similarity between the current output and the input — progressively decomposing the separation problem into easier sub-problems. Without any additional training, CoI consistently improves AudioSep across all five evaluated tasks and SAM-Audio on four of five. An interactive online demonstration system is released alongside this work, allowing users to experience the perceptual improvements on arbitrary audio.

Taken together, these contributions show that USS performance can be improved from two distinct angles: incorporating external knowledge — LLM commonsense priors and contrastive audio-text embeddings — to improve training data and conditioning, and exploiting underutilised capacity already present in frozen models through principled inference-time refinement.

---

The full thesis is available [here]({{ '/assets/pdf/thesis.pdf' | relative_url }}).
