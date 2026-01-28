# AI Services Overview

This organization hosts a collection of **AI modules and crawlers** used in the medical content monitoring and analysis system.

The system consists of:
- **Content crawlers** for data collection
- **AI modules** for relevance filtering, advertisement classification, and information extraction

All AI repositories follow a similar structure and lifecycle:
**data preparation → training → evaluation → export → deployment inference (ONNX)**.

---

## Crawlers

These repositories are responsible for collecting raw content from different platforms before passing data to the AI processing pipeline.

### Google Crawler
**Purpose:**  
Collect articles and web pages from Google Search based on predefined keywords and topics.

**Repository:**  
👉 [GOOGLE CRAWLER](https://github.com/DuAnSYT/google_crawler)

---

### Facebook Post Crawler
**Purpose:**  
Collect public Facebook posts related to specified keywords or topics.

**Repository:**  
👉 [FACEBOOK POST CRAWLER](https://github.com/DuAnSYT/fb_post_crawler)

---

### Facebook Ads Crawler
**Purpose:**  
Collect Facebook advertisements for monitoring and analysis purposes.

**Repository:**  
👉 [FACEBOOK ADS CRAWLER](https://github.com/DuAnSYT/fb_ads_crawler)

---

## AI Modules

### 1. Relevance Filter
**Purpose:**  
Determine whether a collected article/post is relevant to a given topic or keyword set.

**Technique:**  
Hybrid filtering approach:
- Phase 1: Lexical-based filtering (keyword / rule-based)
- Phase 2: Embedding-based semantic relevance checking

**Repository:**  
👉 [RELEVANCE FILTER](https://github.com/DuAnSYT/relevance-filter)

**Data:**  
👉 [Google Drive](https://drive.google.com/drive/folders/1oQGtsMiQ04UWLLUIK-hGQ9y8YyLiYo0F)

**Model Weights / Artifacts:**  
👉 [Google Drive](https://drive.google.com/drive/folders/1Y0SZsitdKgl--wpnRzhQfVnRSUJ9P1D_)

---

### 2. Medical Ads Classification
**Purpose:**  
Classify whether an article/post is a medical-related advertisement.

**Technique:**  
Text classification model trained on labeled medical advertisement data.

**Repository:**  
👉 [ADS CLASSIFICATION](https://github.com/DuAnSYT/ads_classification)

**Data:**  
👉 [Google Drive](https://drive.google.com/drive/folders/1FVOSfLlnYlvI1y_rHfCyyTj_pqls2k_R)

**Model Weights / Artifacts:**  
👉 [Google Drive](https://drive.google.com/drive/folders/1l6i5l8c7Xy3I48yRknK49bS7Sn8L7kBu)

---

### 3. OCR (Optical Character Recognition)
**Purpose:**  
Extract text content from images collected from advertisements, posters, or scanned documents.

**Technique:**  
Deep learning–based OCR model for Vietnamese text recognition, including:
- Text detection (optional, depending on input)
- Text recognition on cropped image regions

**Repository:**  
👉 [OCR MODULE](https://github.com/DuAnSYT/ocr)

**Data:**  
👉 [Google Drive](https://drive.google.com/drive/folders/1mu7gs7F1NPwbE1rXNxHvndzC7wao18kW)

**Model Weights / Artifacts:**  
👉 [Google Drive](https://drive.google.com/drive/folders/1r8msqPjkj4G9-cB92t0TsJu4mbXbaLi7)

---

### 4. Medical Ads Information Extraction
**Purpose:**  
Extract structured information from medical-related articles/posts, including:
- Facility / clinic name
- Address
- Phone number
- License number (GPHD)
- Medical certificate number (CCHN)
- Doctor name

**Technique:**  
Combination of:
- Named Entity Recognition (NER)
- Rule-based heuristics

**Repository:**  
👉 [MEDICAL INFO EXTRACTION](https://github.com/DuAnSYT/extract-data)

**Data:**  
👉 [Google Drive](https://drive.google.com/drive/folders/1R3PHOdPJF_YKsrv59hKj96TO2ng-GbLp)

**Model Weights / Artifacts:**  
👉 [Google Drive](https://drive.google.com/drive/folders/1mImP6UPCWiz4DFdgCY8WI1siFrCPE4tn)

---

### 5. Medical Technique / Category Extraction
**Purpose:**  
Identify and extract medical techniques, services, or technical categories mentioned in the content.

**Technique:**  
Hybrid approach combining:
- Keyword and dictionary-based matching
- Model-based classification or sequence labeling (depending on implementation)

**Repository:**  
👉 [TECHNIQUE EXTRACTOR](https://github.com/DuAnSYT/tenique_extraction_v3)

**Data:**  
👉 [Google Drive](https://drive.google.com/drive/folders/12Rv64l2uelt_VSUYujjST4v7kQZ64sKp)

**Model Weights / Artifacts:**  
👉 [Google Drive](https://drive.google.com/drive/folders/1O2r7XZDdWk29kdwJr_ihHmydo3IkGPdI)

---

## Common Notes

- Each AI module is maintained as an **independent repository**.
- Model weights and large artifacts are **not stored directly in Git** and are provided via external storage.
- ONNX inference modules represent the **deployment-ready version** of each model.
- Training and evaluation code are provided for reproducibility and further development.

---
