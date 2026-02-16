# Japanese-Subject-Predictor-System

This project implements a multi-stage NLP pipeline to predict omitted subjects in Japanese sentences.

## Motivation
Japanese frequently omits explicit subjects, which poses challenges for NLP systems.

## Pipeline Overview
1. Explicit subject detection (spaCy + GiNZA)
2. Subject position prediction (BERT Token Classification)
3. Particle prediction (BERT Sequence Classification)
4. Subject recovery (BERT Masked Language Model)

## Models
All trained models are hosted on Hugging Face Hub [here](https://huggingface.co/Romi121) and automatically downloaded at runtime.

## Usage
See `FindSubjectJapaneseDEMO.ipynb` for a complete example.

## Results
Top-5 accuracy:
- Sentence-level context: 17%
- Paragraph-level context: up to 56%

## Limitations
- No gold-standard evaluation dataset exists
- Task ambiguity even for humans
