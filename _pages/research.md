---
layout: page
permalink: /research/
title: research
description: A summary of my research interests and projects

nav: true
nav_order: 6
---

In all my research experience so far, I have been fortunate to find supportive mentors and amazing collaborators. I strongly believe that a collaborative environment is essential for continued growth in research. I hope to continue having insightful interactions with people working in various domains to receive feedback on my research. If you have any thoughts or comments on the projects I am currently working on, I’d love to connect and chat about them!

# Contract Analysis 

As part of my work at TCS Research, I analyzed massive volumes of commercial contract data. Traditionally, organizations have legal experts to review contract drafts to ensure fairness to all stakeholders. Yet, I noticed a critical gap: the interests of non-legal stakeholders, responsible for implementing the contractual clauses, were often overlooked while drafting the contract. To address this disparity, I worked on automatically identifying potentially unfair clauses from the perspective of non-legal stakeholders, a direction scarcely explored in existing literature. A major obstacle at the project’s inception was the lack of a shared understanding of fairness among various stakeholders. To tackle this issue, I conducted a questionnaire-based survey involving subject matter experts to define fairness. Given the lack of a large labeled dataset, I used self-training, a semi-supervised learning paradigm, to detect unfair clauses. Self-training demonstrated a 9% improvement in accuracy over a Chain-of-Thought prompting (CoT) baseline. Analyzing the model predictions made me realize that LLMs struggled to reason accurately over complex contractual language using CoT. This [work](https://aclanthology.org/2023.nllp-1.11/) was accepted at the Natural Legal Language Processing Workshop at EMNLP’23.

In parallel, my interactions with non-legal stakeholders made me realize the enormous effort required to decipher ambiguous terms within contracts to craft actionable project requirements. In response, I designed an automated assistant to generate targeted questions that aid stakeholders in clarifying ambiguities. I realized that directly prompting LLMs to generate questions, based on the entire contract text, was unsuitable for analyzing ambiguities on a document-wide scale due to the complex structure of contracts. Hence, I devised a two-step approach: the first stage involves using a refined prompting technique to generate clarification questions for individual sentences based on their semantic properties. The second stage integrates a retrieval-augmented framework that efficiently filters out questions that can already be resolved using the contract’s existing content. My solution showed promising results in ambiguity detection, outperforming existing techniques with an F2-score margin of 20%. I presented this [work](https://aclanthology.org/2024.lrec-main.672/) at the LREC-COLING 2024 conference in Turin! 

# Data Management for NLP-Centric Software Systems

I frequently encountered data-related challenges such as the unavailability of labeled data and class imbalance during my work on contract analysis. It motivated me to further analyze the issues inherent in dealing with data for LLM-powered document processing systems. I conducted a qualitative study that involved interviewing experienced practitioners in the field. These interactions highlighted multiple challenges that occur during the data collection, processing, and annotation phases, each posing as a road- block to the effective deployment of such systems. Some of these challenges include subjectivity in labeling, the unstructured nature of text, and the use of specialized language. Subsequently, I identified mitigation strategies and best practices currently employed in the real world to deal with the challenges. My [paper](https://dl.acm.org/doi/abs/10.1145/3522664.3528604) based on this study was nominated for the ACM SIGSOFT Distinguished Paper award at CAIN’22. 

Later, I extended this work to focus on data management in Requirements Engineering (RE)-specific use cases. I analyzed how the text data-centric tasks sit together with the traditional RE process. Based on interviews with experts and current literature in the domain, I identified new RE tasks that may be necessary for handling the increasingly important text data-centricity involved in developing software systems. These [findings](https://arxiv.org/abs/2402.16977) are set to appear in the book titled "NLP for Requirements Engineering". 

